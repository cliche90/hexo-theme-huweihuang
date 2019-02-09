---
title: Frontend Trend
catalog: true
date: 2019-02-09 04:17:53
subtitle:
header-img:
tags:
---

## **Frontend**란 무엇을 말하는 것일까?
> 사용자와 직접적으로 상호작용하는 부분 전부를 통틀어 이르는 말

## 그렇다면 배우는 데에 어떤 문제가 있을까?
> **너무 빠른 변화 속도**

### 비교적 최근에 나온 프론트엔트 Tool  framework, library들
- React.js
- Vue.js
- Angular.js
- Backbone.js
- Ember.js
- Redux
- GraphQL
- Mobx
- Vuex
- React native
- Vue native
- Ionic2
- Babel
- Webpack
- Grunt
- Gulp
- Meteor
- Foundation
- ....

### 프론트엔트 언어(Javascript/html/css)의 파생언어 혹은 파생문법들
- Sass
- JSX
- Typescript
- ...

### JS의 ES6+ 로의 문법 변화
- class
- exports / imports
- arrow function
- ...


> 발전이 빠른게 나쁜건 아니지만 너무 두서없이 나오는 같은데...


## 그래도 선두에서 뛰는 녀석들은 있다.
> 발전이 빠르다고 한들 사람들이 사랑하는 기술은 언제나 한정된 법입니다.
>
> 비교적 최근(2018~2019)에 많은 사랑을 받은 기술들에 대해 개략적으로 소개합니다.

### React.js
- Backend만 최적화하는 줄 아나, Frontend도 최적화 가능해!

### Vue.js
- React.js 좋은것 같긴 한데 쓰기 드럽게 불편하지 않아?
- 그리고 우리는 문서도 다 한글화 해 줌 ㅎㅎ

### Angular
- 데이터를 하나만 가지고 있으면 되지, 화면에 뿌리는거랑 저장하는거랑 왜 따로 씀?

### GraphQL
- ㅋㅋㅋㅋ REST API 아직도 씀?

 

## 그럼 프론트엔드 기술의 선두주자들에 대해 알아보자

### React.js
- 브라우저에 내용 수정할때마다 하는 일이 너무 많은데, 그냥 화면만 갈아치우면 안되나?
- [영상을 봅시다!!!](https://www.youtube.com/watch?v=muc2ZF0QIO4)
- [2018년에 사랑받은 프레임워크들도 봅시다!!](https://insights.stackoverflow.com/survey/2018/#technology-most-loved-dreaded-and-wanted-frameworks-libraries-and-tools)

- 왜 쓸까?
  - 결국엔 변경사항을 확인하는 친구가 자신이 가진 Virtual DOM을 확인하고, 수정사항을 알려주어 수정부분만을 다시 그릴수 있도록 하는 것!
  - 재사용할수 있는 포인트들을 Components 단위로 관리하기 때문에 쓰면 쓸수록 재사용이 많아진다.

- 왜 쓰기 힘들다는 사람들이 많은가?
  - 특수한 문법(JSX)으로 인해, 매번 `babel` 이라는 친구를 통해 파일을 만들어주어야 한다. 그런데 이 친구도 처음엔 무슨소린지 알기 쉽지 않아..
  - babel을 가지고 매번 수정되는 내용을 화면에 import 해주는 것은 매우 귀찮으니, `babel-loader`를 통해 의존성을 확인하고 `webpack`을 통해 파일 하나로 묶어줘야 해..
  - [그럼 기본 셋팅까지의 과정을 한번 볼까?](https://github.com/cliche90/react-boilerplate)
  - 부모 컴포넌트와 자식 컴포넌트끼리만 데이터를 주고받을 수 있기 때문에 형제끼리 데이터가 오갈때는 동일한 조상이 있을때까지 거슬러 올라가야 해..
  - CRA(create-react-app)가 많이 쓸만해 졌지만, 아무튼 시작할 때 사전지식으로 알아야 될 게 너무 많아..

- 문제들에 대한 해결책들은 있어?
  - 일단 제일 문제는 부모와 자식간에만 데이터를 받는게 너무 힘들어, 그 사이에 있는 모든 컴포넌트들에 다 새로 코드를 짜 줘야 하거든..
    - 그래서 나온게 Redux랑 Mobx야!!
    - 쉽게 말하면 모든 컴포넌트들의 선생님이 있는 셈이야! 무언가 변화가 생기면 선생님에게 알려주고, 선생님이 다른 컴포넌트 친구에게 알려줄 일이 생기면 알려주는 식이지!

### Vue.js
- 역시 대륙 형들답게, React.js의 장점만 가져오고, 사용성을 좀 더 높였어!
- 대부분의 가이드가 영어로 되어있다 보니, 잘 되어있는 한글문서가 반가운 건 어쩔수 없는 사실
- 뷰(View) 부분만을 다루는 프레임워크
- html에 script를 import 하는 것만으로도도 사용 가능! 좋은건 일단 다 해놓고 보는 듯한 느낌
- React.js와 유사한 기능을 제공하는 데에 비해, React.js와는 달리 코드가 매우 간결한 것이 특징
- 디렉티브도 있음!! (난 그거 별론데.. 휴... 그래도 Angular보다는 외우기 편하긴 한것 같아, 그냥 `v-`로 시작하는 속성값들은 죄다..)

### Angular.js

### GraphQL
- Anti-REST 진영의 대표주자
- 여전히 REST를 완전히 대체하기는 어려워보임


------------------------------------------------------------------


## 브라우저 콘솔에서 쳐보면 ES6+의 문법이 작동하지 경우도 있던데?

> 번들링(Bundling)이 필요하다.

- 번들링?
  - 여러개의 js, jsx, sass, less 등의 파일들을 웹 브라우저가 해석할 수 있는 html, js, css 등으로 된 하나의 파일로 묶어주는 것
  - 그리고 이러한 것을 해주는 과정 속에서 ES6를 사용할 수 있도록 코드 변경도 함께 일어난다.

## 번들링의 대표주자들

### Webpack

### Babel

### Parcel
- 비교적 신흥강자