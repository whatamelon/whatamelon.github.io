---
layout: post
title:  "세번째 프로젝트 후기 Prj_Niffler"
subtitle: "개발 신생아의 개발 일기3"
develop: true
type: Project
text: true
author: "Seungho Hong"
post-header: true
header-img : "img/prj_niffler.jpg"
date: 2019.08.13
order: 3
---


## 프로젝트 기간

  

  

#### 서비스 구상 및 기획 기간 | 19.03.26 ~ 19.06.13 ( 약 3달 )

  

  

#### 전체 개발 기간 | 18.12.17 ~ 18.12.20 ( 4일 )

  

  

-  ***개발 환경 세팅*** - 14일

  

-  ***UI 및 프론트엔드 개발*** - 30일

  

-  ***백엔드*** - 30일

  

-  ***DB*** - 14일

  

~~프로젝트 기간동안 여러 분야를 왔다갔다하면서 개발해서 개발 날짜가 정확하지 않을 수 있음.~~

  

  

## IDE

  

  

- Eclipse Oxygen 3.0

  

- Visual Studio Code

  

- MySQL WorkBench 8.0 CE

  

- Raspberry PI B+

  

  

## 프로젝트 후기

  
본격적으로 개발에 의욕이 생겨서 빡시게 개발했던 프로젝트이다.
3월에 Vue.js를 접한 후로 내 미래가 여기 있다며 미친척하고 개발을 시작했다.
Spring Boot + Vue.js로 개발환경 세팅하는 데만 2주가 걸렸다.
~~이 때 진짜 때려칠까 생각도 많이 했다.~~

결국은 하긴 했다...
고생도 많이 했고, 레퍼런스 1도 없는 API도 사용하면서 실력도 엄청 상승한 프로젝트다.
집에 못 간 날도 많아서 슬펐지만, 그래도 결과물은 매우 만족스럽다.
  
Aamzon EC2 와 Raspberry PI 를 사용해보았다는 점이 매우 만족스러운 점이다.  
  

## 개발후기

> UI 디자인

처음에 Apache Zeplin을 사용해볼까싶었다.
기웃기웃하다가 그냥 Oven으로 빨리 하고 끝내자라는 마음에 그냥 Oven으로 프로토타입 디자인을 끝냈다.
~~Zeplin을 써봤으면 어땠을까라는 아쉬움이 있다...~~

  

> Front-end

오기가 생겨서 처음부터 하나씩 전부 내 코드로 빌드했다.
웹 개발자라면 한 번쯤은 내 코드로만 반응형을 만들 수 있어야한다고 생각했고, 큰 오판이었다...[^1]
[Vuetify](https://vuetifyjs.com/ko/components/api-explorer)를 기반으로 천천히 빌드를 시작했고, 전체 UI를 완성하는데만 일주일이 넘게 걸렸다...

API도 나를 많이 고생시켰다.

OpenWeatherMap 같은 레퍼런스가 많은 API는 나를 즐겁게 해주었다. `짱짱맨`
반면에, [네이버 트렌드 API](https://developers.naver.com/products/datalab/)같은 경우는 정말 구글에도 자바스크립트 레퍼런스가 단 한개도 없다.
덕분에, 2주동안 밤새면서 개발했다. `감사합니다. 네이버....`
  
  프로젝트 검사 하루 전에 교수님께 디자인이 예쁘지 않다고 검사하지 않겠다는 이야기를 들었고, 하루남기고 밤새면서 디자인을 수정하는 소중한 기억을 간직할 수 있었당 ㅎㅎㅎ
  ~~교수님 사랑합니다~~

  

> Back-end

Spring Boot와 Vue.js를 연동하는 과정에서 꽤 고생했다.
레퍼런스도 한정적인 덕분에 API를 만들어서 Spring Boot로 보내는 작업을 반복했다.
상태관리하랴 router체크하랴 API체크하랴 많이 고생했다.

결국에는 Spring Boot 는 DB와 연결해주는 최소한의 기능만 담당했다.


> DB

MySQL을 사용했다.

DB를 연동하는 과정에서 Mybatis가 호환이 잘 안되서 고생한 기억이 있다.
특히, Amazon과 Raspberry PI 사용과정에서 DB 연동 ID를 계속 바꾸는 바람에 거의 2주동안은 DB만 할 수 있었다.
~~교수님 사랑합니다 222~~
  

  

## 마무리

  

정말 많이 성장한 프로젝트이다.

다시 한 번 하라고 하면 절대 안할 프로젝트이다.

Vue.js는 사랑이다.

~~교수님 사랑합니다 333~~

  
  
  

## 참조

  

>  [Git Repository](https://github.com/whatamelon/prj_niffler_spring)

> [Youtube](https://www.youtube.com/watch?v=0bLGl_kwjww&t=67s)

>[Oven](https://ovenapp.io/project/opX4bzJWcs0ijXOOqdjrUMAI2rdhadK7)

  
  
  

[^1]:  ... Stay!!!!
