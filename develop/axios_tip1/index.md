---
layout: post
title:  "Axios 유연하게 사용하기"
subtitle: "소소한 코딩생각"
description: "nuxt axios api"
develop: true
type: JavaScript
text: true
author: "Seungho Hong"
post-header: true
date: 2019.12.07
header-img : "img/axios.png"
order: 4
---



### Axios 유연하게 사용하기.

#### 현업에서 axios로 값을 계속해서 보내야하는 상황이 생겼다.

##### ( 클릭시 포인트가 1씩 올라가게 만드는 로직을 짜야했다. )

#### 자바스크립트로 모든 api로직은 다 만들어놓은 상황이고, 이제 값이 백으로 제대로 put되면 끝난다.

#### 근데 이놈이 자꾸 parameter만 가져가고 body부분은 버리고 간다....

#### 그래서 그냥 axios에 url을 적어줬다.

#### 사실 이건 완벽한 해결책은 아니다. 그냥 낑겨 놓은 것이나 마찬가지다.

#### 다음에 시간을 내서 좀 더 찾아볼 생각이다.

#### 그전에 일단은 이렇게 처리를 해놓은 상태로 서비스가 계속될 것 같다.

<br/>
<br/>

#### 완벽한 코드를 만들지 못했다고 해서 좌절할 필요는 없다.

#### 현업에 있다보면 기간에 맞춰서 코딩을 해야하고 그러다보면 어쩔 수 없이 완성도가 떨어지는 경우도 생기기 마련이다.

#### 혹시라도 이런 고민 때문에 자괴감에 빠지는 개발자가 있다면 이 말을 해주고 싶다.

#### 코딩은 유연하게 합시다. 유연하게.