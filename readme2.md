1. Selezionare tutti gli studenti iscritti al corso di laurea in Economia
  SELECT * 
  FROM `degrees`
  INNER JOIN `students`
  ON `degrees`.`id` = `students`.`degree_id`
  WHERE `degrees`.`name` LIKE '%economia%'

2. Selezionare tutti i corsi di Laurea Magistrale del Dipartimento di Neuroscienze
