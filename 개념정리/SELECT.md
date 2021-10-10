## SELECT

테이블의 레코드를 선택할 수 있다.

SELECT 필드이름 FROM 테이블 이름 [WHERE 조건];

### 모든 필드 선택

SELECT * FROM 테이블 이름;

### 특정 조건의 레코드 선택

WHERE 절은 테이블의 크기가 매우 크거나, 특정 조건에 맞는 레코드 만을 선택하고 싶을때 유용

예)

- 조건이 하나

SELECT * FROM 테이블 이름 WHERE Name = '홍길동';

- 조건이 여러개

SELECT * FROM 테이블 이름 WHERE ID ≤ 3 AND DATE > '2016-02-01';

 

### 특정 필드만 선택

SELECT 다음에 필드이름을 명시

SELECT Name, Date FROM 테이블이름

### 중복되는 값 제거

DISTINCT 이쿼드를 사용해 값이 한번만 선택되도록 함

SELECT DISTINCT Name FROM 테이블이름

### 정렬

ORDER BY절 기본 설정은 오름차순이다.

SELECT * FROM 테이블이름 ORDER BY Name

- 내림차순일 시

SELECT * FROM 테이블이름 ORDER BY NAME DESC

- 여러개 정렬

SELECT * FROM 테이블이름 ORDER BY NAME DESC, DATE ASC;
