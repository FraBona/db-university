1. Selezionare tutti gli studenti nati nel 1990
  SELECT * FROM `students` WHERE `date_of_birth` LIKE '1990%'

2. Selezionare tutti i corsi che valgono piu di 10 crediti
  SELECT * FROM `courses` WHERE `cfu` > 10

3. Selezionare tutti gli studenti che hanno piu di 30 anni
  SELECT * FROM `students` WHERE `date_of_birth` < '1993%'

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea
  SELECT * FROM `courses` WHERE `period` = 'I semestre' AND `year` = 1

5. Selezionare tutti gli appelli d'esame che avvengano nel pomeriggio (dopo le 14) del 20/06/2020
  SELECT * FROM `exams` WHERE `hour` > '14:00:00' AND `date` = '2020/06/20'