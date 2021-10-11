# JOIN
출처 : [http://tcpschool.com/mysql/mysql_multipleTable_join](http://tcpschool.com/mysql/mysql_multipleTable_join)

JOIN은 데이터베이스 내의 여러 테이블에서 가져온 레코드를 조합하여 하나의 테이블이나 결과 집합으로 표현해 준다.

### INNER JOIN

INNER JOIN은 ON 절과 함께 사용되며, ON 절의 조건을 만족하는 데이터만을 가져온다.

첫번째테이블이름 INNER JOIN 두번째테이블이름 ON 조건

첫번째테이블이름 JOIN 두번째테이블이름 ON 조건

예)

SELECT *

FROM Reservation

INNER JOIN Customer

ON **Reservation**.**Name** = **Customer**.**Name**;

### LEFT JOIN

LEFT JOIN은 첫 번째 테이블을 기준으로, 두 번째 테이블을 조합하는 JOIN입니다.

! 이때 ON 절의 조건을 만족하지 않는 경우에는 첫 번째 테이블의 필드 값은 그대로 가져옵니다.

하지만 해당 레코드의 두 번째 테이블의 필드 값은 모두 NULL로 표시됩니다.

첫번째테이블이름 LEFT JOIN 두번째테이블이름 ON 조건

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/83b99f75-af98-4398-85a3-34a628fdf565/Untitled.png)

### RIGHT JOIN

RIGHT JOIN은 LEFT 조인과는 반대로 두 번째 테이블을 기준으로, 첫 번째 테이블을 조합하는 JOIN입니다.

이때 ON 절의 조건을 만족하지 않는 경우에는 두 번째 테이블의 필드 값은 그대로 가져옵니다.

하지만 해당 레코드의 첫 번째 테이블의 필드 값은 모두 NULL로 표시됩니다.

첫번째테이블이름 LEFT JOIN 두번째테이블이름 ON 조건

