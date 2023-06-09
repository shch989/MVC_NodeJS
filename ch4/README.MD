# NodeJS Ch4

## SQL vs NoSQL

### 어떤 프로젝트에 사용하는 것이 적합할까?

| SQL                                                          | NoSQL                                                    |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| 스키마를 사용한다                                            | 스키마가 없다                                            |
| 상관관계가 있다                                              | 상관관계도 거의 혹은 아예 없다                           |
| 수많은 테이블에 분산된 뒤 상관관계를 통해 연결된다           | 존재하는 문서에 통합 내지는 중첩된 문서를 작업하게 될 때 |
| 수평 스케일링이 매우 어렵거나 불가능한 경우도 있다.          | 수평 스케일링을 쉽게 사용할 수 있다.                     |
| 매초 다수 혹은 수천 건의 쿼리를 읽고 써야 한다면 사용을 비추 | 처리량이 많은 어플리케이션에서 고성능을 발휘한다.        |

## MySQL 설정
#### https://www.mysql.com/

## MySQL 모듈 설치
```
$ npm install --save mysql2
```

## SQL 데이터베이스 연결
```
const mysql = require('mysql2')

const pool = mysql.createPool({
  host: 'localhost',
  user: '<user_name>',
  database: '<db_name>',
  password: '<db_password>',
})

module.exports = pool.promise()
```
