---
layout: post
title:  "Connection closed before full header was received 해결방법."
subtitle: "a little hack for flutter image error"
description: "flutter 플러터"
flutter: true
type: flutter
text: true
author: "Seungho Hong"
post-header: true
header-img : "img/404.jpg"
date: 2020.09.20
order: 3
---


### error log.

>  CacheManager: Failed to download file from
https://s3.ap-northeast-2.amazonaws.com/image.fitchoo/items/eichichi/eichichi_5512.gif with error:
[        ] I/flutter ( 7499): Connection closed before full header was received


### git issues.

https://github.com/flutterchina/dio/issues/694
https://github.com/Baseflow/flutter_cached_network_image/issues/336
https://github.com/flutter/flutter/issues/25107


### 해결방법

이 이슈는 케이스가 워낙 다양합니다.
크게 본다면, 서버로 부터 이미지를 불러와야 하는데, api커넥션은 끊어졌고, 그 사이에 불러와야할 이미지가 불러와 지지 못해서 생긴 문제입니다.

대부분의 flutter 개발자 분들은 http connection 라이브러리로 http / dio 이 두개를 사용하실 건데요, 이 이슈는 해당 라이브러리들과는 상관이 없는 이슈입니다.

우리가 https를 통해 이미지를 불러올때, https의 보안 프로토콜을 통과하면서 인코딩과 디코딩 과정을 거치게 됩니다. 이때, 문제가 생깁니다.

이미지를 불러오는 도중 or 아직 불러오지 못했는데 or 디코딩 하고 있는데, 커넥션이 끊어진 것입니다. 그래서 다 불러오지 못하고 `Connection closed before full header was received ` 해당 메시지와 함께 에러가 리턴됩니다. 

이때, 대처법은 케이스 별로 여러가지가 있습니다. 


1. https - http <br/> 제가 사용한 방법입니다. 이것저것 다해보고 안되서 `https://github.com/flutter/flutter/issues/25107#issuecomment-655655719` <br/> 해당 코멘트를 보고 작은 방법이라 길래 혹해서 해봤습니다. 사실 이 방법은 별로 신뢰가 가지 않았습니다. 설마 플러터가 여러 이미지의 https 디코딩을 이렇게 부실하게 만들었을까 싶었던 거죠... <br/> 근데 이게 해결방법이었습니다. 네. 바꾸니까 아무런 문제가 없어지더군요... 


2. ConnectionPerHost 최댓값 지정 <br/> 

`class MyHttpOverrides extends HttpOverrides {
  @override
  HttpClient createHttpClient(SecurityContext context) {
    return super.createHttpClient(context)
        ..maxConnectionsPerHost = 5;
  }
}

void main() {
  HttpOverrides.global = MyHttpOverrides();
  runApp(MyApp());
}`

이 코드는 해당 이슈를 서버의 문제로 인식하고 서버의 부담을 덜어주는 방법입니다.
하나의 방법이 될 수 있습니다.

