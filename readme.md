1. Selezionare tutti gli studenti nati nel 1990
  SELECT * FROM `students` WHERE `date_of_birth` LIKE '1990%'

2. Selezionare tutti i corsi che valgono piu di 10 crediti
  SELECT * FROM `courses` WHERE `cfu` > 10