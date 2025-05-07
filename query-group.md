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


 # Contare quanti corsi di laurea ci sono per ogni dipartiment