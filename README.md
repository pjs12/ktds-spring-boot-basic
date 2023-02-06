# Spring-boot-basic

1. Boot 와 Legacy 차이  
- dependency에 starter 문구  
- main class 있음  
- 단위 테이스 가능  
- Spring Boot Application Annotation 3개  
  @SpringBootConfiguration / @EnableAutoConfiguration / @ComponentScan  
- Spring Boot Application  
- Tomcat 내장  
  
2. AOP 정의  
-	Advice  
  A.	언제 어디에 어떠한 기능의 공통 관심 로직을 핵심 로직에 적용할지 적용  
  B.	 Before advice / After returning advice / After throwing advice / After advice / Around advice  
- Joinpoint  
  A.	실행 시의 처리 플로우에서 Advice를 위빙하는 포인트  
  B.	구체적으로는 어디서 메서드 호출이나 예외 발생이라는 포인트를 Joinpoint로 정의  
-	Pointcut  
  A.	하나 또는 복수의 Joinpoint를 하나로 묶은 것  
  B.	Advice의 위빙 정의는 Pointcut을 대상으로 설정  
  C.	하나의 Pointcut에는 복수 Advice를 연결할 수 있음  
-	Advisor  
  A.	Advice와 Pointcut을 하나로 묶어 다루는 것  
  B.	스프링 AOP에만 있고 관점 지향에서 ‘관점’을 나타내는 개념  
-	Aspect  
  A.	여러 객체에서 공통으로 적용되는 공통 관심 사항  
  B.	로깅, 트랜잭션 처리 등  
-	Weaving  
  A.	Advice를 핵심 로직 코드에 적용하는 것  
  
- Advice, Joinpoint, Pointcut...  
- Joinpoint의 묶음 = Pointcut  
- Transactional Annotation  
  - 데이터 변경(insert, delete, update)에 사용  
  - 하나라도 실패 시, 자동 Rollback 됨  
  - DB에 종속적이지 않음  
  
3. Controller @ResponseBody Annotation  
- @ResponseBody 리턴 값이 데이터  
- @RestController로 대체 가능 (Controller + ResponseBody)  
  
4. GET과 POST(Restful) 방식  
- url  
  - GET : test?n=10  
  - POST : test/10  
- @PathVariable Annotation  
  - GetMapping("/test/{n}")  
    public method(@PathVariable int n)  
  
5. ORM  
- 객체 중심으로 데이터 사용  
- JPA도 마찬가지  
  
6. 특정 DB에 종속적인 쿼리 사용
- Application Property 파일에 추가
  - spring.jap.database-platform = org.hibernate.dialect.MariaDB103Dialect

7. 파일 업로드
- form 태그 수정
  - enctype="multipart/form-data" 추가해야 함

8. Interceptor / Filter
- ![image](https://user-images.githubusercontent.com/31908647/216917341-c40511b6-4b35-45ee-8d92-ac818692e6fd.png)
