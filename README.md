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










--Soma idade de todos os alunos
SELECT SUM(Idade) AS SOMA_IDADE
FROM Alunos

--Faz a média de idade de todos os alunos
SELECT AVG(Idade) AS MEDIA_IDADE
FROM Alunos

--COloca o sexo feminino
UPDATE Alunos
SET Sexo = 'F' 
WHERE ID IN (1, 3, 4, 5, 6, 8, 9, 11, 12, 14, 16, 17, 18, 19, 21, 22, 25, 32, 33); 


--Coloca o sexo masculino
UPDATE Alunos
SET Sexo = 'M' 
WHERE ID IN (2, 7, 10, 13, 15, 20, 23, 24, 26, 27, 28, 29, 30, 31);


--Média idade Feminino
SELECT AVG(Idade) AS MEDIA_IDADE
FROM Alunos 
WHERE SEXO = 'F';

--Média idade Masculino
SELECT AVG(Idade) AS MEDIA_IDADE
FROM Alunos 
WHERE SEXO = 'M';

--Soma idade Feminino
SELECT SUM(Idade) AS SOMA_IDADE
FROM Alunos 
WHERE SEXO = 'F';


--Soma idade Masculino
SELECT SUM(Idade) AS SOMA_IDADE
FROM Alunos 
WHERE SEXO = 'M';









--Média idade dos alunos que têm a letra "b" no nome
SELECT AVG(idade) AS media_idade
FROM alunos
WHERE nome LIKE '%b%';


--Soma das idades das alunas e alunos que têm a letra "s" no nome
SELECT SUM(idade) AS soma_idades
FROM alunos
WHERE nome LIKE '%s%';


--Média idade das alunas com nomes iniciados em "i"
SELECT AVG(idade) AS media_idade
FROM alunos
WHERE sexo = 'F' AND nome LIKE 'i%';


--Média idade dos alunos com nomes iniciados em "g"
SELECT AVG(idade) AS media_idade
FROM alunos
WHERE sexo = 'M' AND nome LIKE 'g%';


--Soma das idades das alunas que têm "a" no nome e soma das idades dos alunos que têm "f" no nome
SELECT 
  SUM(CASE WHEN sexo = 'F' THEN idade ELSE 0 END) AS soma_idades_alunas,
  SUM(CASE WHEN sexo = 'M' THEN idade ELSE 0 END) AS soma_idades_alunos
FROM alunos
WHERE nome LIKE '%a%' OR nome LIKE '%f%';

















--Idade máxima do sexo masculino que tem a letra "c" no nome
SELECT MAX(idade) AS idade_maxima
FROM alunos
WHERE sexo = 'M' AND nome LIKE '%c%' AND nome NOT LIKE 'ALICE%';


--Idade mínima do sexo feminino e do sexo masculino que têm a letra "f" no nome
SELECT MIN(idade) AS idade_minima
FROM alunos
WHERE (sexo = 'F' OR sexo = 'M') AND nome LIKE '%f%' AND nome NOT LIKE 'ALICE%';


--dade máxima do sexo feminino (F) com nomes iniciados em "g"
SELECT MAX(idade) AS idade_maxima
FROM alunos
WHERE sexo = 'F' AND nome LIKE 'g%' AND nome NOT LIKE 'ALICE%';


--Idade mínima dos sexo masculino com nomes iniciados em "r"
SELECT MIN(idade) AS idade_minima
FROM alunos
WHERE sexo = 'M' AND nome LIKE 'r%' AND nome NOT LIKE 'ALICE%';

--Soma das idades máxima e mínima
SELECT MAX(idade) + MIN(idade) AS soma_idades
FROM alunos
WHERE nome NOT LIKE 'ALICE';

--Do sexo feminino que têm "a" no nome
SELECT *
FROM alunos
WHERE sexo = 'F' AND nome LIKE '%a%' AND nome NOT LI
