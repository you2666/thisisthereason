---
layout: post
permalink: /digitalmarketing/study-naver/
title: '디지털 마케팅 공부하기'
date: 2020-02-06 07:30:00 +09:00
feature: '/img/posts/002/naver-search.jpg'
background: '/img/posts/002/back-digitalmarketing.jpg'
categories:
  - digitalmarketing
tags:
  - 디지털마케팅
  - 마케팅공부
  - 서치어드바이저
  - 디지털노마드
description: 'HTML, CSS, JavaScript에 대한 아주아주 기초적인 공부를 했다. 개발자는 아니지만, 디지털 마케팅을 하기 위한 기초가 필요했기 때문인데 이 카테고리에서는 공부한 기초 지식을 사용하는 디지털 마케팅에 대해 다뤄볼 예정이며 첫 번째 글은 네이버 서치어드바이저이다.'
---

## 네이버 서치어드바이저 정리

![네이버 웹마스터도구](/img/posts/002/naver.jpg)

#### 검색엔진 최적화의 목적

웹 상에는 수 많은 웹사이트가 존재한다. 그 중 한국의 공룡 포털 네이버에는 사이트 정보를 수집하고 검색에 노출해주는 검색 로봇이 있다. 이름은 예티(Yeti). 네이버 검색 로봇은 사이트 정보를 수집해 검색에 반영한다. 웹 표준을 준수해 제작된 사이트로 신뢰할 수 있고, 많은 사람이 방문하는 곳이거나 많은 사람이 인용한다면 예티가 더 빨리 알아차릴수 있다. 하지만, 이 블로그는 쇼핑몰도 아니고 글도 아직 없어서 활성화되지 않았기 때문에 예티가 이 블로그를 알아차리는 데 많은 시간이 필요하다. 그러니까, 예티에게 사이트를 알려주자. 이 검색엔진 최적화 작업은 사이트 내 콘텐츠 정보를 검색엔진이 잘 이해할 수 있도록 정리하는 작업으로 콘텐츠의 내용을 명확하게 네이버 검색엔진에게 전달해 내 콘텐츠가 네이버의 검색 결과에 누락되지 않도록 알려줄 수 있다. 아래는 네이버에서 볼 수 있는 가이드 중 내가 기억해야할 일부를 정리한다. 원본은 [네이버 서치어드바이저](https://searchadvisor.naver.com/) 사이트에서 볼 수 있다. 



#### 1. 웹마스터도구에 내 사이트를 등록하고 소유 확인

사이트 등록은 호스트 단위만 지원하며, 소유 확인은 HTML의 meta 태그를 활용하는 방법 혹은 HTML 파일 업로드를 통해서 진행할 수 있다. 나는 head에 메타태그 삽입하는 방법으로 진행했다. 

![사이트소유확인](/img/posts/002/ownsite.jpg)

#### 2. 네이버 검색로봇이 사이트에 접근할 수 있도록 허용

사이트의 문서에 네이버 검색로봇의 접근이 가능하게 하려면 robots.txt를 아래처럼 설정해야한다. 이 블로그는 지킬을 이용했다. 그래서 내 블로그 폴더 안에 robots.txt 파일을 생성하고 아래 내용을 입력하고 저장한다. robots.txt에 대한 자세한 설명은 [robots.txt 설정하기](https://searchadvisor.naver.com/guide/seo-basic-robots)를 참고하면 된다.

![검색로봇예티](/img/posts/002/robots.jpg)

(예) 모든 검색엔진의 로봇에 대하여 접근 가능하게 설정

```javascript
User-agent: Yeti
Allow: /

Sitemap: https://thisisthereason.com/sitemap.xml
```

(예) 네이버 검색로봇만 접근 가능하게 설정

```javascript
User-agent: Yeti
Allow: /
```

#### 3. 중복된 콘텐츠가 있는지 확인

검색 노출량을 늘이기 위하여 동일한 콘텐츠로 구성된 여러 개의 사이트를 개설하는 경우 검색 노출에 불이익을 받을 수 있다. 무료 이미지 공유 사이트인 [픽사베이](https://pixabay.com/ko/)의 이미지보다 내가 폰 카메라로 대충 찍은 사진이 더 좋은 콘텐츠로 분류된다. 유일한 콘텐츠고, 중복이 아니기 때문이다. 또, 모든 페이지의 제목을 동일하게 쓰지 말라고 권고한다. 페이지의 제목은 콘텐츠 주제를 정확하게 설명할 수 있는 문구로 써야하며, 더 자세한 내용은 [HTML 마크업 가이드](https://searchadvisor.naver.com/guide/markup-intro)를 참고하면 된다. 

#### 4. 웹마스터도구에 사이트맵 및 RSS

사이트맵은 사이트 내의 수집 대상 URL 목록을 담은 XML 형식의 파일로 웹마스터도구의 "요청-사이트맵 제출" 메뉴에서 XML 형식의 사이트맵을 제출할 수 있다. 사이트 내의 최신글은 본문 전체를 포함하여 RSS 피드에 담아야 하며, 웹마스터도구의 "요청-RSS 제출" 메뉴에서 RSS 피드를 제출하면 된다. RSS 피드와 사이트 맵을 아톰에서 추가했고, 네이버에는 URL로 제출했다. 아래는 RSS 피드 예시.

#### 5. 웹마스터도구에 채널 등록 - 연관채널

채널은 네이버 블로그, 카페, 페이스북, 인스타그램 등 운영하고 있는 소셜 미디어의 계정으로 일반적으로 쇼핑몰 등의 사이트를 검색했을 때 하단에 연관채널이라고 나와 있는 부분이다. Microdata 형식과 JSON-LD 형식으로 구현할 수 있다. <head>...</head>에 넣어주면 된다. 아래는 내가 잘 이용하는 쿠팡 JSON-LD 예시. 

![쿠팡연관채널](/img/posts/002/coupang.jpg)

```html
<script type="application/ld+json">
{
 "@context": "http://schema.org",
 "@type": "Person",
 "name": "쿠팡",
 "url": "https://www.coupang.com",
 "sameAs": [
   "https://tv.naver.com/coupangtv",
   "https://www.instagram.com/coupang",
   "https://www.facebook.com/Coupang.korea"
   "https://story.kakao.com/ch/coupang"
 ]
}
```

#### 6. 네이버 검색 결과 확인

네이버의 검색로봇이 방문한 뒤 최대 1주일 이내에 사이트의 콘텐츠가 검색에 반영되며, 네이버 검색창에 사이트명을 입력해 확인할 수 있다. 추가로 웹마스터도구에서 제공하는 [콘텐츠 노출 및 클릭](https://searchadvisor.naver.com/guide/report-expose-ctr) 리포트를 활용하여 본인이 등록한 웹사이트가 네이버 검색 결과에 얼마나 노출되고 클릭 되었는지 성과를 확인해보자. 사이트의 메인 페이지가 검색 노출이 안되는 경우에는 내 사이트가 네이버 검색로봇의 접근을 허용하고 있는지 robots.txt 와 방화벽 설정을 다시 한번 확인하자. 메인 페이지의 meta 태그에 noindex 처리가 되어있다면 해제해야한다. noindex가 표기된 페이지는 검색 반영에서 제외된다.

```html
<meta name="robots" content="noindex">
```

사이트 제목과 설명은 검색엔진에서 엄격하게 관리하고 있으므로 정책에 위반되는 항목이 없는지 [HTML 마크업 가이드](https://searchadvisor.naver.com/guide/markup-intro)를 다시한번 참고하고, 사이트 메인 페이지의 정보를 HTML frame 태그로 감싸고 있는지 체크해보자. frame 태그가 일으키는 문제로 인하여 사이트 메인 페이지와 같은 중요한 페이지에는 frame 태그 대신 일반 HTML 태그를 사용하는 것을 권장한다.

#### 7. 사이트의 콘텐츠가 검색에 반영이 안된다면

페이지의 meta 태그에 noindex 처리가 되어있다면 해제. noindex가 표기된 페이지는 검색 반영에서 제외된다. 페이지 내의 모든 콘텐츠가 자바스크립트로 로딩되는 구조인지 확인해야한다. 대부분의 검색엔진은 표준 HTML 마크업을 사용하여 콘텐츠를 제공하는 것을 권장한다. 페이지 내의 모든 콘텐츠를 HTML frame 태그로 감싸고 있는지 확인하자. 페이지의 중요한 콘텐츠는 frame 태그 대신 일반 HTML 태그를 사용하는 것을 권장한다. 페이지 로딩 시 자바스크립트 사용하여 redirect 되는지 확인하자. 가급적 HTTP redirect 또는 HTML의 head 태그 내 meta refresh를 활용하는 것을 권장한다.

#### 8. 네이버 검색 결과에 반영되는 문서 수가 적다면 페이지 내 링크 확인

웹마스터도구에 제출된 사이트맵 및 RSS 가 올바르게 표기되었는지 확인하자. 특히, 제출된 사이트맵 및 RSS 내의 링크가 상대 경로로 지정되어 있는 경우, 링크의 호스트가 등록된 사이트와 일치하지 않는 경우 수집을 진행하지 않는다. 페이지의 meta 태그에 nofollow 처리가 되어있다면 해제해야한다. nofollow가 표기된 페이지의 경우 페이지 내 링크 수집을 진행하지 않는다.

```html
<meta name="robots" content="nofollow">
```

페이지들의 링크 처리 시 자바스크립트만을 사용하면, 검색로봇이 어떤 URL 인지 정확하게 파악할 수 없어서 이후의 다른 좋은 정보들을 찾아갈 수 없는 문제가 있다. 네이버의 예티에게 내 사이트 내부 페이지를 잘 알려주기 위해서는 표준에 맞는 링크 URL정보를 제공하는 것을 권장한다.

```html
<a href="http://www.A.com">Link</a>
해당 링크가 어떤 URL 인지 정확하게 확인할 수 있음
<span onClick="javascript:goto(A)">Link</span>
대상 링크가 자바스크립트 함수로만 표현되어 있어서 검색로봇은 해당 링크의 정확한 URL을 파악할
```