# cabinet

## JPA
[JPA 레퍼런스 번역](http://arahansa.github.io/docs_spring/jpa.html)

* JPA 오류 해결
** jpa로 update querlDsl 사용할 경우 
*** 에러 로그 : org.hibernate.hql.internal.QueryExecutionRequestException: Not supported for DML operations
`@Transactional, @Modifying 어노테이션 붙여줘야 실행 가능`
