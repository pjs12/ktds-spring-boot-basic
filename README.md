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
  1.	Advice
    A.	언제 어디에 어떠한 기능의 공통 관심 로직을 핵심 로직에 적용할지 적용
    B.	 Before advice / After returning advice / After throwing advice / After advice / Around advice
  2.	Joinpoint
    A.	실행 시의 처리 플로우에서 Advice를 위빙하는 포인트
    B.	구체적으로는 어디서 메서드 호출이나 예외 발생이라는 포인트를 Joinpoint로 정의
  3.	Pointcut
    A.	하나 또는 복수의 Joinpoint를 하나로 묶은 것
    B.	Advice의 위빙 정의는 Pointcut을 대상으로 설정
    C.	하나의 Pointcut에는 복수 Advice를 연결할 수 있음
  4.	Advisor
    A.	Advice와 Pointcut을 하나로 묶어 다루는 것
    B.	스프링 AOP에만 있고 관점 지향에서 ‘관점’을 나타내는 개념
  5.	Aspect
    A.	여러 객체에서 공통으로 적용되는 공통 관심 사항
    B.	로깅, 트랜잭션 처리 등
  6.	Weaving
    A.	Advice를 핵심 로직 코드에 적용하는 것

- Advice, Joinpoint, Pointcut...  
- Joinpoint의 묶음 = Pointcut  
- Transactional Annotation : 데이터 변경(insert, delete, update)에 사용  
- 
