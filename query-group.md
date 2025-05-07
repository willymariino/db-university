# Contare quanti iscritti ci sono stati ogni anno
SELECT YEAR (enrolment_date) AS anno_iscrizione, COUNT(*)
 AS totale_iscrizizioni_annuali
 FROM `db-university`.students
GROUP BY YEAR (`enrolment_date`) 
ORDER BY 'anno_iscrizione'

 # Contare gli insegnanti che hanno l'ufficio nello stesso edificio
SELECT office_address, COUNT(*) AS totale_insegnanti
FROM `db-university`.teachers
GROUP BY office_address;

 # Calcolare la media dei voti di ogni appello d'esame
SELECT exam_id, AVG(vote) AS media_esami
 FROM `db-university`.exam_student
 GROUP BY exam_id

 # Contare quanti corsi di laurea ci sono per ogni dipartiment
 SELECT department_id, COUNT(*)
FROM `db-university`.degrees
GROUP BY department_id