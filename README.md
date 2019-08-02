# 웹 프로젝트 회의 내용

1. 주제 정하기 - 2가지 의견

2. 역할 분담 & 기술스택

3. 공통 기능 구현

4. 다음 모임 날짜 및 할것들 정하기

## 1. 주제 정하기

#### 1. 스트리머 종사자들을 위한 커뮤니티 & 트렌드 추천 서비스

#### 주요 기능
    
   - 스트리머를 위한 커뮤니티
   
        - [트게더](https://tgd.kr)
   
   - 키워드 검색시 관련 키워드 추천
    
        - [keywordtool.io](https://keywordtool.io/youtube)     
   
   - 편집자 스트리머 매칭
      
        - [편집몬](https://editmon.com/main/index.html)

### 2. 학생들을 위한 개발자 커뮤니티 서비스 

   - 개발, 프로젝트 스터디 모집
   
        - [캠퍼스픽(스터디 모집 - 프로그래밍)](https://www.campuspick.com/study/list?category1=4&category2=407)
   
   - 학생 개발자 커뮤니티 게시판

        - [Okky (개발자 커뮤니티)](https://okky.kr/)

### 정해진 결론

   - 두 서비스를 아우르는 기능들을 먼저 개발하자       
       
## 2. 역할 분담
    
백엔드와 프론트앤드 역할 분담시 다양한 옵션 존재

### 1. 하나의 서버에서 운용

1-1 spring + jsp

**예상 이슈**

경계 모호

jsp(혹은 템플릿) 코드 구현은 누구(백엔드 or 프론트엔드)의 몫인가


1-2 spring + react & vue

**예상 이슈**

크롤러가 html 검색엔진 점수에 반영 안될 수 있음 & 스프링 서버 부담

참고 1 : [[번역] client side rendering vs server side rendering](https://jongmin92.github.io/2017/06/06/JavaScript/client-side-rendering-vs-server-side-rendering/)

참고 2 : [줌 인터넷 구현 사례](https://zuminternet.github.io/ZUM-Pilot-vuejs/)

1-3 spring + html

**예상 이슈**

html간 세션 공유 불가능 - 각 html마다 ajax로 별도 요청 필요

구현 방식은 1-2랑 같은 클라이언트 사이드 렌더링, 검색엔진 반영 안될수 있음


### 2. 프론트앤드 서버(node.js + reac & vue) , 백앤드 서버(spring) 별도 운용

프론트앤드 서버에서 server-side rendering 적용, 결과물은 역시 하나의 html페이지

**예상 이슈**

CORS 이슈 (proxy 서버 거칠지, 아니면 cors 허용할지)


### 스프링 기술스택 정하기

1. Spring mvc 선택 시

    xml 설정 vs java 설정
    
2. Spring boot vs Spring mvc 선택

    
## 3. 기능 구현

### 로그인

[참고 1 - 스프링 oauth 연동](https://www.popit.kr/spring-security-oauth2-%EC%86%8C%EC%85%9C-%EC%9D%B8%EC%A6%9D/)

[참고 2 - 스프링 firebase 토큰 검증](https://firebase.google.com/docs/auth/admin/verify-id-tokens?hl=ko)

1.외부 api 인증
    
   pop-up방식 / redirection방식 

2.일반 로그인
    
   pop-up방식 / redirection방식
   
3. 외부 api 인증 + 일반 로그인


## 4. 다음주 모임 날짜 및 회의 주제 정하기

### 모임 날짜

다음주 화요일

### 다음 모임 회의 주제

1. 기술스택 토론(1시간)

    - 역할 분담, 기술스택에 명시된 것들 미리 조사 후 의견 공유
    
2. 두 서비스를 아우르는 공통된 기능 제시 및 디자인 조사
    
    - 로그인
    
    - 게시판
    
    등등..







