# Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT courses.*, degrees.name
FROM courses
INNER JOIN degrees ON degrees.id = courses.degree_id
WHERE degrees.name = "corso di laurea in economia"

 # Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

 SELECT degrees.* FROM `db-university`.degrees
INNER JOIN departments
 ON departments.id = degrees.department_id
WHERE degrees.level = "magistrale"
AND departments.name = "neuroscienze";

non funziona

# Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
SELECT * FROM `db-university`.course_teacher
INNER JOIN courses
ON courses.id = course_teacher.course_id
WHERE teacher_id = 44

 # Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

 # Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

 # Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

 # BONUS: Selezionare per ogni studente il numero di tentativi sostenutiper ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18