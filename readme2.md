1. Selezionare tutti gli studenti iscritti al corso di laurea in Economia
  SELECT * 
  FROM `degrees`
  INNER JOIN `students`
  ON `degrees`.`id` = `students`.`degree_id`
  WHERE `degrees`.`name` LIKE '%economia%'

2. Selezionare tutti i corsi di Laurea Magistrale del Dipartimento di Neuroscienze
  SELECT * 
  FROM `degrees` 
  INNER JOIN `departments`
  ON `degrees`.`department_id` = `departments`.`id`
  WHERE `degrees`.`name` LIKE '%magistrale%'
  AND `departments`.`name` LIKE '%neuroscienze%'

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
  SELECT * 
  FROM `courses` 
  INNER JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
  INNER JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`
  WHERE `teachers`.`name` = 'Fulvio' AND `teachers`.`surname` = 'Amato'

4. Selezionare tutti gli studenti con i dati relativi al corso di laure a cui sono iscritti e il relativo dipartimento, in ordine per cognome e nome
  SELECT * 
  FROM `students`
  INNER JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
  INNER JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
  ORDER BY `students`.`surname` DESC

5. Selezionare tutti i corsi di alurea con i realtivi corsi e insegnanti
  SELECT * 
  FROM `degrees` 
  INNER JOIN `courses` ON `degrees`.`id` = `courses`.`degree_id`
  INNER JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
  INNER JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`

6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica
  SELECT * 
  FROM `teachers`
  INNER JOIN `course_teacher` ON `teachers`.`id` = `course_teacher`.`teacher_id`
  INNER JOIN `courses` ON `courses`.`id` = `course_teacher`.`course_id`
  INNER JOIN `degrees` ON `courses`.`degree_id` = `degrees`.`id`
  INNER JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
  WHERE `departments`.`name` LIKE '%matematica%'
  