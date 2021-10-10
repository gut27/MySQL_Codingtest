### GROUP BY

특정 컬럼을 그룹화

자료형에 관계 없이 사용 가능

쿼리의 가장 뒤에 사용

### HAVING

특정 컬럼을 그룹화한 결과에 조건을 건다.

! WHERE은 그룹화하기 전의 조건 HAVING은 그룹화 후의 조건

SELECT 컬럼 FROM 테이블 GROUP BY 그룹화할 컬럼;

### 조건 처리 후 컬럼 그룹화

SELECT 컬럼 FROM 테이블 WHERE 조건식 GROUP BY 그룹화할 컬럼;

### 컬럼 그룹화 후에 조건 처리

SELECT 컬럼 FROM 테이블 GROUP BY 그룹화할 컬럼 HAVING 조건식;

### 조건 처리 후 그룹화 후에 조건 처리

SELECT 컬럼 FROM 테이블 WHERE 조건식 GROUP BY 그룹화할 컬럼 HAVING 조건식;

### ORDER BY가 존재하는 경우

SELECT 컬럼 FROM 테이블 WHERE 조건식 GROUP BY 그룹화할 컬럼 HAVING 조건식 **ORDER BY** 컬럼;
