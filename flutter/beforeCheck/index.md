---
layout: post
title:  "Flutter 개발 하기전 체크사항!"
subtitle: "꼭 플러터로 하이브리드앱을 개발해야하는가?"
description: "flutter 플러터"
flutter: true
type: flutter
text: true
author: "Seungho Hong"
post-header: true
header-img : "img/question.jpg"
date: 2020.09.08
order: 1
---



## 플러터 개발자가 쓰는 플린이들을 위한 주의사항

#### 이 글은 여러분들이 충분히 플러터가 뭔지 검색을 하고 읽으신다는 전제하에 작성하는 글입니다.
#### 또한 이 글은 네이티브와 플러터를 비교하는 글입니다. 같은 하이브리드 프레임워크인 리엑트 네이티브와는 상관없습니다.
#### 철저하게 주관적이니 에이 쓰레기네라고 생각하시는 분들은 네 맞습니다! 쓰레기 글입니당

## Question1

### 네이티브 코드 어렵던데 플러터로 하면 네이티브 코드 작성안해도 되겠지?ㅎㅎ
 네 아닙니다! 네이티브는 설정 세팅이든 푸시 노티든 네이티브 기능이던 간에 무조건 한번은 꼭 작성하셔야되고 꾸준히 유지보수를 하셔야합니다. 
 플러터는 기본적으로 네이티브 위에서 돌아가는 플래시 or 캔버스 입니다. 전제 조건이 네이티브인 기술입니다. 
 그러니 좋든 싫든 네이티브에 관해서 꾸준히 리서치 하셔야되고 안드로이드나 ios의 최신 동향을 항상 살펴주시는게 좋습니다.



## Question2

### 플러터 성능 좋다던데 개꿀아닌가? 네이티브 왜함?
 플러터의 성능은 엄청나게 좋지 않습니다. 간혹 구글링을 하면 나오는 자료들이 있습니다. 
 플러터는 스위프트보다 좋고 자바와 비슷하다 는 식의 자료와 그래프 차트를 보실 수 있습니다. 
 안타깝게도 일정 조건이 충족된 상황에서는 플러터의 성능이 좋을 수도 있지만 늘 그렇지 않습니다.
 대부분의 경우에 플러터가 항상 성능이 떨어지고 사용자가 앱을 오래써서 부하가 생기거나 네이티브 기능을 자주사용한다면 퍼포먼스 저하는 배가 됩니다. 
 뛰어난 퍼포먼스를 원하신다면 네이티브를 고려해주셔요ㅎㅎ


 
## Question3

### 플러터로 개발하면 엄청 빠르다던데 개꿀아님? ㅎㅎ
맞습니다 엄청빠릅니다 개꿀이죠. 근데 이건 어디까지나 기본적인 코드에 관해서 입니다.
ui를 그리는데 있어서는 플러터의 능력은 정말 놀라울 정도 입니다. 하지만 여기까지 입니다. 
여러분 개발을 하는데 정말 중요하고 시간을 할애해야할 부분은 ui가 아니라 내부 로직이라고 생각합니다. 
내부적으로 함수를 구현하고 생명주기를 맞추는것은 네이티브나 플러터나 똑같습니다 이건 순전히 개발자의 능력이라고 생각합니다. 

그리고 이건 네이티브가 더 유리합니다. 

덧붙여서 유려한 ui를 개발하는것은 플러터도 똑같이 어렵습니다. 저도 플러터로 말도안되는 ui를 구현할 때가 있습니다. 
이런경우에는 네이티브의 레퍼런스가 정말 많기 때문에 네이티브가 훨씬 유리한경우가 많고 

### 사실 이건 개발자의 능력차이라고 봅니다.

<br/>
<br/>

#### 본 글이 플러터로 앱 개발을 시작하시려는 분들께 결정적으로 시작하지 않는 글로 작동할 수도 있습니다.
#### 분명한 것은 플러터는 어디까지나 근본이 하이브리드에 있지 네이티브에 있지 않다는 것입니다.
#### 하이브리드 생태계에서는 각광받는 프레임워크일지라도 아직 네이티브와의 비교는 힘들다고 생각합니다. 
#### 여러분의 선택에 도움이 되었기를 바랍니다.