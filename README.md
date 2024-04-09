# 09-04



--QUATIDADE DE FUNCIONÁRIOS

SELECT * FROM `SALARIOS` WHERE PROFISSÃO LIKE 'P%';
SELECT * FROM `SALARIOS` WHERE PROFISSÃO LIKE 'M%';
SELECT * FROM `SALARIOS` WHERE PROFISSÃO LIKE 'A%';
SELECT * FROM `SALARIOS` WHERE PROFISSÃO LIKE 'T%';
SELECT * FROM `SALARIOS` WHERE PROFISSÃO LIKE 'J%';

--SOMA SALÁRIOS

SELECT SUM(SALÁRIO) AS SOMASAL_PROF FROM `SALARIOS`WHERE PROFISSÃO = 'PROFESSOR';

--MÉDIA

SELECT AVG(SALÁRIO) AS MEDIA_SALARIOS FROM `SALARIOS`WHERE PROFISSÃO = 'PROFESSOR';

--MÁXIMO

SELECT MAX(SALÁRIO) AS MAIOR-SALARIO FROM `SALARIOS`WHERE PROFISSÃO = 'PROFESSOR';

--MÍNIMO

SELECT MIN(SALÁRIO) AS MENOS_SALARIO FROM `SALARIOS`WHERE PROFISSÃO = 'PROFESSOR';

--DESAFIO 1

SELECT MAX(SALÁRIO) AS MAIOR_SALARIO FROM SALARIOS WHERE PROFISSÃO IN ('ATOR', 'MÚSICO');

--DESAFIO 2

SELECT MAX(SALÁRIO) AS MAIOR_SALARIO FROM SALARIOS WHERE PROFISSÃO IN ('ATOR', 'MÚSICO', 'JODADOR DE FUTEBOL');
