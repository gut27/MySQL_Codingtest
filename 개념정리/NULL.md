### NULL 검색

 WHERE 칼럼명 IS NULL

WHERE 칼럼명 < = > NULL

예)

SELECT ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NULL
ORDER BY ANIMAL_ID

### NULL이 아닌것을 검색

WHERE 칼럼명 IS NOT NULL

-------------------------------------------------------------------------------------
컬럼 값이 NULL 인 경우를 처리하는 함수

# IFNULL

해당 **Column의 값이 NULL을 반환할 때, 다른 값으로 출력할 수 있도록 하는 함수**이다.

- 기본 구조

```
SELECT IFNULL(Column명, "Null일 경우 대체 값") FROM 테이블명;
```

### IF()??

**Null 처리는 사실 `IF` 함수와 `IS NULL` 조건으로도 가능**하다.

- Example

```
// NAME Column이 NULL이 True인 경우 "No name"을, False인 경우는 NAME Column을 출력
SELECT IF(IS NULL(NAME), "No name", NAME) as NAME
FROM ANIMAL_INS
```

# CASE

**해당 Column 값을 조건식을 통해 True, False를 판단**하여 **조건에 맞게 Column값을 변환할 때 사용하는 함수**이다.

- 기본 구조

```
CASE
    WHEN 조건식1 THEN 식1
    WHEN 조건식2 THEN 식2
    ...
    ELSE 조건에 맞는경우가 없는 경우 실행할 식
END
```

# COALESCE

**`COALESCE`**는 **지정한 표현식들 중에 NULL이 아닌 첫 번째 값을 반환**한다.***모든 DBMS에서 사용가능***

표현식은 여러 항목 지정이 가능하고, 처음으로 만나는 NULL이 아닌 값을 출력한다.*표현식이 모두 NULL일 경우엔 결과도 NULL 반환*

**`COALESCE`**는 배타적 OR 관계 열에서 활용도가 높다.*엔터티(테이블)에서 두 개 이상의 속성(열) 중 하나의 값만 가지는 데이터 일 경우*

- 기본 구조

```
// NULL 처리 상황
SELECT COALESCE(Column명1, Column명1이 NULL인 경우 대체할 값)
FROM 테이블명

// 배타적 OR 관계 열
// Column1 ~ 4 중 NULL이 아닌 첫 번째 Column을 출력
SELECT COALESCE(Column명1, Column명2, Column명3, Column명4)
FROM 테이블명
```

출처 : [https://velog.io/@gillog/DB-MySQL-NULL-처리IFNULL-CASE-COALESCE](https://velog.io/@gillog/DB-MySQL-NULL-%EC%B2%98%EB%A6%ACIFNULL-CASE-COALESCE)
