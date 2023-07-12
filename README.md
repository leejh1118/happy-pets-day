# 팀명 : NPE 단속반

# 프로젝트 이름 : happy-pets-day

## 팀 구성

|팀장|이건희|           
|:--:|:--:| |부팀장|김대연| |팀원|박광인| |팀원|서지민| |팀원|조상수| |팀원|이정현|

## 로그인 검사 추가하는 방법

1. cofig.InterCeptorConfig.Java 에 들어가서 코드 참고해서 원하는 url추가

```java
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
//        일반 회원 세션 확인
        registry.addInterceptor(loginInterceptor)
                .addPathPatterns("/myPage/**") //해당 url로 시작하는 모든 경로
//             .addPathPatterns("/세션 검사를 할 url")
                .addPathPatterns("/stroll/write"); //검사할 페이지를 지정
```

## ERD구성

[![NPE단속반 erd구성](./src/main/resources/static/img/Spring_Erd.png)](https://dbdiagram.io/d/647f4f07722eb774947ee12c)

## 프로젝트 주제

1. ### 반려동물에 관한 여러 서비스를 제공하는 사이트
    - 반려동물 종 추천(고양이, 강아지)
    - 산책 번개모임 구하기
    - 펫 시터 연결