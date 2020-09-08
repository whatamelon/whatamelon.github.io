---
layout: post
title:  "nuxt transition"
subtitle: "네이티브인 척 하기"
description: "nuxt javascript 자바스크립트"
develop: true
type: Nuxt
text: true
author: "Seungho Hong"
post-header: true
header-img : "img/doors.jpg"
date: 2019.01.16
order: 5
---



## Nuxt Transition

#### nuxt transition 이란?
 페이지 이동시 자연스럽게 이어주는 트렌지션이다.
 마치 네이티브에서 페이지 이동이 일어나듯이 자연스러운 UI와 뛰어난 성능을 보여준다.
 이러한 장점과 함께 사용자에게 마치 네이티브인 것 마냥 자연스러운 UX를 제공한다.
 ( native같은 web이 있다? 뿌슝빠슝 )


#### 왜 Nuxt Transition인가?
[FITCHOO](https://fitchoo.kr/) 에서는 서비스상의 뎁스가 추가될 때마다 옆으로 넘어가는 UI를 제공한다.
이를 위해 웹상에서 구현할 수 있는 여러가지 방법들을 찾아보았다.
처음에는 [OnsenUI](https://onsen.io/vue/)가 대두되었지만, 곧 nuxt 프로젝트 내에 페이지간 이동시 트렌지션을 제공한다는 사실을 알게 되었고, 프론트엔드메인스택이 [NUXT.js](https://ko.nuxtjs.org/) 였기 때문에, **nuxt transition**을 사용하기로한다.

#### 어떻게 사용해야할까?
사실 nuxt transition은 관련 레퍼런스가 거의 없다.
아무래도 nuxt라는 프레임워크의 사용자가 vue에 비해 적을뿐더러, nuxt transition을 사용하는 더 적기 때문일 것이다.
그렇지만 어떻게든 해야만 했다.

공식 문서에는 `String`, `Object`, `Funtion` 이 3가지 방법을 제시한다.

처음에는 String 방식으로 사용했다.
하지만, 이는 여러 페이지간에 이동이 많고, 이동하는 경우의 수가 많은 FITCHOO서비스에 적합하지 못했다.
따라서 Function 방식을 사용하기로 한다.

#### Function transition

 1. .vue 파일 내에 template 내부에 transition 엘리먼트 삽입.
>      <template>
>     	<transition>
>     	</transition>
>     </template>


 2.  main.css 파일 내부에 transition css 코드 작성.

	enter-active, leave-active는 페이지의 라이프사이클이다.
	각각 페이지 진입 활성화와, 페이지 진출 활성화를 뜻한다. 

	.slideLeft-enter-active
		{
			animation: slide-left-in .3s;
		}
	.slideLeft-leave-active 
		{
			animation: slide-right-out .3s;
		}
	@keyframes  slide-left-in {
		0% { transform: translateX(-100vw); }
		10% { transform: translateX(-75vw); }
		20% { transform: translateX(-55vw); }
		30% { transform: translateX(-40vw); }
		40% { transform: translateX(-30vw); }
		50% { transform: translateX(-22vw); }
		60% { transform: translateX(-16vw); }
		70% { transform: translateX(-12vw); }
		80% { transform: translateX(-8vw); }
		90% { transform: translateX(-4vw); }
		100% { transform: translateX(0vw); }
	}
	@keyframes  slide-right-out {
		0% { transform: translateX(0); }
		10% { transform: translateX(25vw); }
		20% { transform: translateX(45vw); }
		30% { transform: translateX(60vw); }
		40% { transform: translateX(70vw); }
		50% { transform: translateX(78vw); }
		60% { transform: translateX(84vw); }
		70% { transform: translateX(88vw); }
		80% { transform: translateX(92vw); }
		90% { transform: translateX(96vw); }
		100% { transform: translateX(100vw); }
	}

이런식으로 작성해주었다.

3. .vue 파일 script 내부에 transition fuction 작성.

> 	transition (to) { 		
> if (localStorage.getItem("backButton")){
> 			return  'slideLeft' 		
> } 	
> else  if (to.name == "model-id" ||
> 			to.name == "product-id" || 			
> to.name == "exhibition-id") {
> 			return  'slideRight' 		
> } 		else  if(to.name == "model" ||
> 			to.name == "modellow" || 			
		> to.name == "modelmean" || 			to.name ==
		> "modelhigh" || 			
>  ) 		return  "nothing" 		} 	
>  },

이런식으로 분기를 태운 후 retrun을 통해 main.css에 작성한 코드의 이름을 가져온다.

 
#### 개인적으로 조금은 어려웠던 프로그래밍중 하나다. 레퍼런스가 많지 않아서 nuxt team에 컨택을 해봤지만, 이메일 회신도 없고, 질문에 답도 달아주지 않았다...ㅠ
#### 결국 한 땀 한 땀 해서 완성은 했지만, 쉽지 않았다ㅠㅠ

#### 공식 문서에는 네이티브와 같은 UI를 보여준다고 하지만, 아래 gif를 보면 알 수 있듯이, 성능은 완벽하지는 않다. 

![image](img/nuxtTransition.gif)

#### 하지만 웹앱을 구현하는 프로젝트나, 페이지간 트렌지션이 필요한 서비스에는 충분히 좋은 대안이라고 생각한다.

#### 모쪼록 이 포스팅이 nuxt transition을 사용하시는 개발자분에게 도움이 되었으면 좋겠습니다.

#### 포스팅을 보고 이해가지 않으시는 부분이 있으시거나, nuxt transition관련해서 질문이 있으시다면 hsh0617@naver.com으로 메일주시면 성실하게 답변해드리겠습니다 XD