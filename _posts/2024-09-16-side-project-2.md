---
layout: post
title: "[sideproject 02] 빌드 및 데이터 연결"
date: 2024-09-16 12:00:00 +0900
categories: [post]
tags: [project]
---

#### 새 프로젝트 만들기

IntelliJ   
File -> New Project -> Spring Boot

인텔리제이에서 위 순서대로 새로운 프로젝트를 선택  우측 하단에 ```NEXT```



### 오류 기록

#### Docker Compose

> Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?

서버 실행할 때 저런 오류 메세지가 떴다. 서버 연결할 때 Docker demon이 실행되지 않아서 서버를 실행할 수 없다는 것이다. 

Docker demon이 뭔데... 

![2](https://github.com/user-attachments/assets/a7e4b6c3-9919-444a-a68d-e405d0363175)
의존성을 무슨 장바구니 담아서 쇼핑하듯이 담아 놓음. 거의 의존성 ver 도떼기시장. 프로젝트가 진행 될수록 여기서 뭘 더 

그 전에, 내가 주입해놓은 의존성들이 어떤 역할을 하는지 알아보자(내가 엎은 밥상 내가 치우기)