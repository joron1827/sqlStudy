문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/59404
동물 보호소에 들어온 모든 동물의 아이디와 이름, 보호 시작일을 이름 순으로 조회하는 SQL문을 작성해주세요. 단, 이름이 같은 동물 중에서는 보호를 나중에 시작한 동물을 먼저 보여줘야 합니다.

-- 코드를 입력하세요
SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME, DATETIME DESC

문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/59405
동물 보호소에 가장 먼저 들어온 동물의 이름을 조회하는 SQL 문을 작성해주세요.

-- 코드를 입력하세요
SELECT NAME 
FROM ANIMAL_INS 
WHERE DATETIME = (SELECT MIN(DATETIME) FROM ANIMAL_INS)


문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/59415
가장 최근에 들어온 동물은 언제 들어왔는지 조회하는 SQL 문을 작성해주세요.

SELECT MAX(DATETIME) FROM ANIMAL_INS