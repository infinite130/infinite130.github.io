---
layout: post
title: "[sideproject 01] 사이드 프로젝트 시작하기"
date: 2024-09-06 10:00:00 +0900
categories: [post]
tags: [project]
---



### 사이드 프로젝트의 필요성

5개월간 Java 국비 수업을 들으면서 프로젝트를 2개 진행했지만, 개발의 전체적인 흐름을 이해하기 무리가 있었다.   

첫 번째 프로젝트는 servlet 과 JSP 를 이용해서 localhost로 서버를 띄우고 개발을 진행했다. 팀원들과 아주 기초적인 CRUD 가 가능한 홈페이지를 제작했다. 자바 코드 사용, 개발 환경에서 서버와 클라이언트가 데이터를 어떻게 주고받는지와 같은 기본적인 내용은 이해할 수 있었지만 제대로 된 개발 흐름을 이해하는데 어려움이 많았다. 그때만 해도 프레임워크와 IDE의 차이가 뭔지, API와 라이브러리는 뭔지 많은 개념들이 혼동되고 MVC 패턴으로 프로젝트를 진행했음에도 MVC 패던이 뭔지 몰랐다. 짧은 기간 동안 내가 맡은 기능을 부랴부랴 끝냈다.   
 
첫 번째 프로젝트를 마치고 대체 내가 뭘 한거지? 하는 생각을 했다.   

두 번째 프로젝트는 스프링 프레임워크를 사용해서 개발을 진행했다. 내가 맡은 기능은 위치 찾기와 후원 결제 기능이다. 두 기능 모두 API key를 발급 받아 진행하는 거라 크게 어렵지 않았다. 카카오맵 API의 경우 script 코드를 제공해주기 때문에 내가 원하는 방식으로 수정해서 사용하는 방향으로 개발을 진행했다. 결제 기능도 script 코드를 쉽게 찾을 수 있었고 API key를 발급 받고 결제 방식(나는 카카오페이를 연결했다)을 선택해서 어렵지 않게 개발을 끝냈다. 위치 검색에서 검색 기록을 데이터베이스에 저장해서 서버에 띄우는 것과, 후원 결제 기능에서 결제 정보를 데이터베이스에 저장해서 게시판에 따로 빼는 부분은 어려웠다. 데이터는 아무리 다뤄도 왜 익숙해 지지가 않고 계속 어렵기만 한 건지... 아무튼 이 두 번째(마지막) 프로젝트를 통해서 내가 데이터를 설계하고 데이터를 저장해서 서버와 클라이언트가 서로 원활하게 주고받도록 하는 부분을 제일 어려워 한다는 걸 알게 됐다.   

API 기능만 두 가지를 구현하다보니 기본적인 CRUD 만들기가 다시 어려워졌고... 기초적인 기술과 지식은 꾸준히 공부해야 한다는 것을 깨달았다.   

그리고 두 번째 프로젝트를 끝내고 현장 실습을 나갔는데 스프링보다 스프링부트를 더 많이 사용한다는 것이다. 그리고 배포에 사용하는 Docker라는 플랫폼의 중요성도 알게 됐는데 프로젝트를 두 개나 진행하면서 배포는 해본적이 없어서 슬프고 당황스러웠다. 제일 중요한것도 안했으면서 프로젝트가 끝나서 기뻐했다니....

![jonathan](https://github.com/user-attachments/assets/6b52deba-02aa-4f0b-b9d7-3bdedda534c9)   

아무튼 이번 실습 기간에 자습할 수 있는 시간이 많이 주어져서 나는 이 기간에 실습 회사에서 주는 과제와 더불어서 기획부터 배포까지 모두 혼자 경험해보는 사이드 프로젝트를 진행해보기로 했다.   

...하려고 했으나! 계속 새로운 프로젝트를 하는 것보다는 내가 했던 기존의 프로젝트를 디벨롭하고 개념을 확장하는 부분이 더 나을거라는 판단이 들었다. 일단 기초가 탄탄해야 건물을 쌓아올릴 수 있으니 말이다.


그래서 마지막으로 진행한 SML 프로젝트를 react+spring boot 버전으로 디벨롭 하기로 결정했다.


### 사이드 프로젝트 주제

직전에 진행한 팀 프로젝트 [SML](https://github.com/SML-SpringInMyLife/SML)은 Spring In My Life의 줄임말로 웹사이트 이용 고객과 우리 팀 모두에게 인생에 봄이 오기를 바라는 마음으로 정한 타이틀이다. 노인 지원 프로그램을 만들었는데, 노인들에게 다양한 교육 서비스를 제공하는 게 주 목적이고 그 외에 공지사항/커뮤니티/위치찾기/후원 등의 기능이 있다. 

하지만 이렇게 디벨롭 하는 과정에서 그럼 이전에 사용한 기술은 별로라는 말이야? 남들이 많이 쓰는 게 무조건 좋다는 말인가? 하는 의문이 들 수 있다. 

나조차도 채용 공고를 찾아 보다가 요즘은 다 Spring 이 아니라 Spring Boot를 쓰잖아? MyBatis 가 아니라 JPA를 쓰잖아? 라는 생각으로 사이드 프로젝트를 시작하게 됐으니 말이다. 

그래서 이렇게 기술 스택을 바꾸는 과정에서 왜 기술들을 바꾸어 가면서 기능을 수정하게 됐는지 고찰해보기로 했다.

### 기술 스택 수정 이유

기술 분류 별로 기술 수정 이유를 상세하게 나열해보자.

변경 : 기존에 사용하던 기술에서 다른 기술로 변경함
유지 : 기존에 사용하던 기술을 그대로 사용함
new : 이전에 사용해보지 않았던 기술을 새롭게 사용함

#### 프레임워크 (변경)

#### IDE (변경)

#### 빌드 도구 (변경)

#### ORM (변경)

#### 웹 서버 (유지)

#### 프론트엔드 (new)

#### 데이터베이스 (변경)

#### 테스트 (유지)

#### 보안 (추가)

#### CI/CD (new)

#### 배포 (new)

#### API 문서화 (new)

#### 클라우드 및 인프라 (new)


### 기술 스택 (계획)

마이그레이션을 진행할 프로젝트(SML)의 개발 환경은 다음과 같다.

> Java11
> eclipse
> Spring Framework 5.3.9
> Tomcat 9.0
> Maven
> HikariCP
> MyBatis
> Oracle sqldeveloper
> Junit
> JSP

요약한 기술 스택은 아래와 같다    

| 분류               | 기술                             |
|-------------------|---------------------------------|
| 프로그래밍 언어    | Java, JavaScript                |
| 백엔드 프레임워크  | Spring, Spring Boot             |
| IDE    | IntelliJ                |
| 빌드 도구          | Gradle                   |
| ORM               | JPA                              |
| 웹 서버            | Spring Boot 내장 Tomcat                           |
| 프론트엔드 라이브러리 | React                        |
| 데이터베이스        | MySQL                            |
| 테스트             | JUnit                            |
| 보안              | JWT, Spring Security             |
| CI/CD             |         Jenkins, GitLab                         |
| 배포               | Docker, Kubernetes              |
| API 문서화         | Swagger                          |
| 클라우드 및 인프라  | AWS                             |
| 버전관리  | GitHub                             |


### 기간 설정

사이드 프로젝트를 시작하자고 마음먹은 건 24-09-06 이지만 이 글이 마무리 된 시점은 24-09-16이다.

프로젝트 주제 선정 : 24.09.06~24.09.16
프로젝트 시작 및 마감 : 24.09.16~24.09.22


### 프로젝트 요약

| 항목               | 내용                             |
|-------------------|---------------------------------|
| 프로젝트 소개      |              팀 프로젝트의 내 기능 디벨롭                   |
| 기간/인원           |       24.09.06~24.09.22 / 1명                          |
| 기술 및 개발 환경   |                                 |
| 시스템 아키텍처     |                                 |
| ERD               |                                 |
| API 설계 구조      |                                 |




### 참고
[소프트웨어 개발 수명 주기(SDLC)란 무엇인가요?](https://aws.amazon.com/ko/what-is/sdlc/)   
[애자일 방법론](https://simsimjae.medium.com/%EC%95%A0%EC%9E%90%EC%9D%BC-%EB%B0%A9%EB%B2%95%EB%A1%A0-753368aa3058)   
[애자일(Agile) 방법론과 프로토타입의 등장](https://ebbnflow.tistory.com/103)   
