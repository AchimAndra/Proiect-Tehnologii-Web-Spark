# Proiect-Tehnologii-Web-Spark
# Continuous Feedback App

## Obiectiv
Realizarea unei aplicații web care să permită acordarea de punctaje anonime de către un juriu anonim de studenți pentru proiectul altor studenți.

## Tehnologii Folosite
- Frontend (SPA): React.js  
- Backend (API): Node.js + Express.js  
- Bază de Date: PostgreSQL  
- ORM: Sequelize  
- Comunicare Live: WebSockets  
- Versionare: Git  



## Funcționalități Cheie

### Profesor
- Autentificare și gestionare profil  
- Definire activități și livrabile  
- Gestionare coduri de acces  
- Dashboard & status activități  
- Feedback continuu (LIVE)  
- Vizualizare date istorice (grafice și cronologie)

### Student
- Acces rapid la activități  
- Interfață pentru acordarea feedback-ului  
- Păstrarea anonimatului evaluatorului  

---

## Flux de evaluare proiect

1. **Student MP** adaugă proiect și livrabile, atașând link sau video demonstrativ.  
2. Sistemul selectează **aleatoriu membri ai juriului** pentru fiecare livrabil.  
3. **Evaluatorii** acordă note anonime (1-10, cu până la 2 zecimale) doar în perioada permisă.  
4. **Profesorul** vizualizează media finală și graficele, fără a vedea identitatea evaluatorilor.  
5. Media finală este calculată **omitând nota cea mai mare și cea mai mică**.  

---

## Modelul de Date

### profil
- `profil_id` (PK)  
- `nume_utilizator`  
- `tip` (student/profesor)  
- `email`  
- `parola`  

### cod
- `cod_id` (PK)  
- `continut`  
- `profesor_id` (FK)  
- `este_aleatoriu`  

### activitate
- `activitate_id` (PK)  
- `profesor_id` (FK)  
- `cod_id` (FK)  
- `titlu`  
- `descriere`  
- `ora_inceput`  
- `ora_sfarsit`  
- `accesibil_de_la`  
- `accesibil_pana_la`  

### feedback
- `feedback_id` (PK)  
- `activitate_id` (FK)  
- `creata_la`  
- `emoticon`  

## Modelul de Date
- Profil
- Cod
- Activitate
- Feedback

## Obiectiv
Realizarea unei aplicații web care să permită acordarea de punctaje anonime de către un juriu anonim de studenți pentru proiectul altor studenți.


