---
title: Frontend Trend
catalog: true
date: 2019-02-09 04:17:53
subtitle:
header-img:
tags:
---

요즘 Frontend 기술이 너무 많이 쏟아지다보니 제가 아는 범주 내에서 무엇이 있는지 정도만 알아보려 합니다.

## **Frontend**란 무엇을 말하는 것일까?
> 사용자와 직접적으로 상호작용하는 부분 전부를 통틀어 이르는 말

## 그렇다면 배우는 데에 어떤 문제가 있을까?
> **너무 빠른 변화 속도**가 우리의 발목을 잡는다

### 비교적 최근에 나온 프론트엔트 Tool, Framework, Library들
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
- Ionic native
- Ionic4
- Babel
- Webpack
- Grunt
- Gulp
- Meteor
- Foundation
- ....

### 프론트엔트 언어(Javascript/html/css)의 파생언어 혹은 파생문법들
- Sass
- Less
- JSX
- Typescript
- Nodejs
- CoffeeScript
- Elm
- ...

### JS의 ES6+ 로의 문법 변화
- class
- exports / imports
- arrow function
- ...


> 발전이 빠른게 나쁜건 아니지만 너무 빠른것 같은데...


## 그래도 선두에서 뛰는 녀석들은 있다.
> 발전이 빠르다고 한들 사람들이 사랑하는 기술은 언제나 한정된 법입니다.
>
> 비교적 최근에 많은 사랑을 받은 기술들에 대해 개략적으로 소개합니다.
>
> 좀 더 많은 내용을 알고 싶다면 [stateofjs](https://stateofjs.com/)를 추천드립니다.

### React.js
<p align="center">
    <img src="./react.png" />
</div>

- Frontend의 병목도 줄이고 싶어서 만들었어!

### Vue.js
<p align="center">
    <img src="./vuejs.png" />
</div>

- React.js 좋은것 같긴 한데 쓰기 드럽게 불편하지 않아?
- 그리고 우리는 문서도 다 한글화 해 줌 ㅎㅎ

### Angular
<p align="center">
    <img src="./angular.jpg" />
</div>

- 데이터를 하나만 가지고 있으면 되지, 화면에 뿌리는거랑 저장하는거랑 왜 따로 씀?

### GraphQL
<p align="center">
    <img src="./graphql.png" />
</div>

- ㅋㅋㅋㅋ REST API 아직도 씀?

 
## 그럼 프론트엔드 기술의 선두주자들에 대해 알아보자

### React.js
- Facebook 형들이 만들어준 Javascript Library
- 브라우저에 내용 수정할때마다 하는 일이 너무 많은데, 그냥 필요한 부분만 갈아치우면 안될까?
- [소개 영상을 봅시다!!!](https://www.youtube.com/watch?v=muc2ZF0QIO4)
- [2018년에 사랑받은 프레임워크들도 봅시다!!](https://insights.stackoverflow.com/survey/2018/#technology-most-loved-dreaded-and-wanted-frameworks-libraries-and-tools)

- 왜 쓸까요?
  - 변경사항을 확인하는 친구가 자신이 가진 Virtual DOM을 확인하고, 수정사항을 알려주어 수정부분만을 다시 그릴수 있도록 하는 것!
  - 재사용할수 있는 포인트들을 Components 단위로 관리하기 때문에 쓰면 쓸수록 재사용이 많아진다.

- 왜 쓰기 힘들다는 사람들이 많을까요?
  - 특수한 문법(JSX)으로 인해, 매번 `babel` 이라는 친구를 통해 파일을 만들어주어야 합니다. 그런데 `babel`이라는 친구도 처음엔 어떻게 사용해야하는지 알기 쉽지 않습니다.
  - `babel`을 가지고 매번 수정되는 내용을 화면에 `import` 해주는 것은 매우 귀찮으니, `babel-loader`를 통해 의존성을 확인하고 `webpack`을 통해 파일 하나로 묶어줘야 합니다.
  - [그럼 기본 셋팅까지의 과정을 한번 해볼까요?](https://github.com/cliche90/react-boilerplate)
  - 부모 컴포넌트와 자식 컴포넌트끼리만 데이터를 주고받을 수 있기 때문에 형제끼리 데이터가 오갈때는 동일한 조상이 있을때까지 거슬러 올라가야 하는 단점이 있습니다.
  - CRA(create-react-app)가 많이 쓸만해 졌지만, 아무튼 시작할 때 사전지식으로 알아야 될 게 너무 많은게 현재까지도 문제가 됩니다.

- 문제들에 대한 해결책들은 있나요?
  - 일단 제일 문제는 부모와 자식간에만 데이터를 받는게 지속적으로 App의 복잡도를 올리기도 하고, 데이터 전송을 하고자 하는 컴포넌트들의 사이에 있는 모든 컴포넌트들에 다 새로 코드를 짜 줘야 한다는 단점.
    - 그래서 나온게 Redux랑 Mobx입니다.
    - 쉽게 말하면 모든 컴포넌트들의 선생님이 있는 셈으로, 컴포넌트가 무언가 상태값의 변화가 생길 경우 선생님에게 알려주고, 선생님은 그걸 듣고 해당 상태값이 필요한 다른 컴포넌트 친구에게 알려주는 식입니다.

- 컴포넌트를 작성하고 이를 Mount 하는 방식으로 되어있습니다.
    ```javascript
    class HelloMessage extends React.Component {
        render() {
            return (
                <div>
                    Hello {this.props.name}
                </div>
            );
        }
    }

    ReactDOM.render(
        <HelloMessage name="Taylor" />,
        document.getElementById('hello-example')
    );
    ```

### Vue.js
- 역시 대륙의 형들답게, React.js의 장점만 가져오고, 사용성을 좀 더 높였습니다.
- 대부분의 가이드가 영어로 되어있다 보니, 잘 되어있는 한글문서가 반가운 것도 어쩔수 없는 사실입니다.
- 뷰(View) 부분만을 다루는 Javascript 프레임워크
- html에 script를 import 하는 것만으로도도 사용 가능합니다. 좋은건 일단 다 해놓고 보는 듯한 느낌
    ```html
    <!-- index.html -->
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>
    ```
- React.js와 유사한 기능을 제공하는 데에 비해, React.js와는 달리 코드가 매우 간결한 것이 특징
- 디렉티브도 있음습니다 (저는 별로 디렉티브를 좋아하지는 않지만, 필요할 경우에 쓸 수 있다는 것만으로도 큰 강점을 가집니다. 예를 들어 데이터 바인딩과 같은 것들이요)
- 결국 결과물을 빨리 보고 싶고 단지 경량의 App을 만드는 것이라면 `Vue`, 그보다 좀 더 대규모에 적합한 개발을 할 경우에는 `React`를 사용하는 것이 일반적입니다.
- 빠른 렌더링과 `React` 보다 작은 용량
    - 요즘에는 성능차이는 그다지 나지 않는다고 합니다.
- Template 기반의 코드 작성
    ```html
    <!-- html -->
    <div id="app">
        {{ message }}
    </div>
    ```
    ```javascript
    // javascript
    var app = new Vue({
        el: '#app',
        data: {
            message: '안녕하세요 Vue!'
        }
    })
    ```

### Angular.js
- 벌써 10살이 된 `Angular`는 현재 stable 버전 기준으로 `v7.2.4` 버전이 출시되었습니다.
- 그리고 `Angular`도 훌륭한 한국어 문서를 제공합니다. 최신버전이 `v7.2.4`인데 `v7.2.0` 버전의 한글문서를 제공하는 것을 보면 업데이트도 빨라 보입니다.
- 위에서 소개한 `React`나 `Vue`와는 달리 `typescript`를 사용합니다.
- 사용자 경쟁에서 소외되지 않기 위해 `Angular`도 `create-react-app`이나 `vue cli`와 같이 `angular cli`를 제공합니다. 그저 커맨드라인을 몇 줄 치면 프로젝트 구성이 완료됩니다.
    ```bash
    # angular cli 설치
    npm intall -g @angular/cli
    # App 기본 코드 작성하기
    ng new my-app
    cd my-app
    ng server --open
    ```
- 컴포넌트를 구성하는 요소들 중 `html`과 `typescript` 파일만 보면 아래와 같습니다.
    ```html
    <!-- src/app/app.component.html -->
    <h1>
        Welcome to {{ title }}!
    </h1>
    ```
    ```typescript
    // src/app/app.component.ts
    @Component({
        selector: 'app-root',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css']
    })
    export class AppComponent {
       title = 'My First Angular App!';
    }
    ```
- 단지 위와 같이 구성하는 것만으로 2-way data binding이 가능합니다.
- 위에서 2-way binding을 가능케 하는 것은 출시 당시 가장 큰 강점으로 손꼽히던 것은 바로 MVVM(Model-View-ViewModel) 패턴입니다.
    - 쉽게 말하면 MVC 패턴에서 Controller가 ViewModel로 바뀐 것입니다.
    - Angular 공식에서는 MVW(Model-View-Whatever)라고 하네요.
    - 결국 View에서 데이터가 수정되거나 Model에서 데이터가 수정되거나 중간에서 컨트롤러의 역할을 해 주는 ViewModel이 서로의 데이터를 갱신하도록 조정해 줍니다.

### GraphQL
- Anti-REST 진영의 대표주자
- 여전히 REST를 완전히 대체하기는 어려워보임
- 말은 Anti-Rest 지만 결국 기존의 Rest 보다 더 Restful을 지향한다고 볼 수 있음


------------------------------------------------------------------


## 브라우저 콘솔에서 쳐보면 ES6+의 문법이 작동하지 경우도 있던데?

> 번들링(Bundling)이 필요합니다.

- 번들링?
  - 여러개의 js, jsx, sass, less 등의 파일들을 웹 브라우저가 해석할 수 있는 html, js, css 등으로 된 하나의 파일로 묶어주는 것
  - 그리고 이러한 것을 해주는 과정 속에서 ES6를 사용할 수 있도록 코드 변경도 함께 일어납니다.

## 번들링의 대표주자들

### Webpack
- 불과 1년 전 정도만 하더라도 `React`의 개발환경을 구성하기가 너무 힘들었기 때문에 대부분의 개발자들은 `Webpack`을 이용해 번들링을 했습니다.

### Babel

### Parcel
- 비교적 신흥강자로 `babel`과 `webpack`이 불편함을 해소하고자 나온 것으로 보입니다.
- 아직까지는 그다지 대세라거나 트렌디하다고 보기는 어렵기 때문에, 이런게 있다고만 알아두면 될 것 같습니다.


------------------------------------------------------------------


## Frontend는 지금도 변화한다

### 모바일까지 진출한 Frontend 기술들
- 그리고 이러한 Javascript의 저변 확대에 힘입어 모바일 역시도 Javascript를 통해 개발할 수 있게 되었습니다.
- Node.js의 출시로 Frontend 개발만 하던 사람들도 비교적 쉽게 Backend의 개발을 할 수 있게 되면서 Javascript의 저변이 매우 넓어졌습니다.
- 대표적으로 `React Native`, `Vue Native`, `Ionic Native` 등이 있습니다.
- 위 기술들의 가장 큰 장점은 `Android`와 `iOS`의 구별없이 개발이 가능하다는 점입니다. 또한 `Xcode`나 `Android Studio`의 느려터진 빌드 없이도 바로 수정 결과를 거의 즉시 확인이 가능하기 때문에 생산성 측면에 있어서도 훌륭합니다.
- 다들 웹 기술에 기반해 있기 때문에 나중에 웹으로의 확장도 어렵지 않습니다.
- 그러나 장점만 있지는 않습니다. 제일 큰 것은 유지보수의 어려움입니다. 문제 발생시 이것이 어디서 난 문제인지 파악하기 어렵습니다.
- 또 당연하다면 당연하지만 `Native`에 비해 라이브러리가 턱없이 부족하며, 자체적으로 지원하는 컴포넌트들이 아니고서야 복잡한 수정사항이 발생할 경우 결국 컴파일된 `Native Code` 에 손을 대야 할 것입니다.
- 위와 같은 일이 있기 때문에 결국에는 `Native`에 대한 지식과 웹 기반 모바일 기술에 대한 지식이 모두 필요할 수 있습니다.
- 그럼에도 불구하고 기존에 비해 훨씬 빠르게 개발이 가능하다보니 기술 도입을 떠나서 사용해보고 작성해보는 것은 나쁘지 않을 것이라고 생각합니다.
- 위의 `Native` 기술들 말고도 `Hybrid App`이라는 분야가 존재하지만 개인적으는 앞으로도 계속 나올지는 모르겠습니다. 퍼포먼스가 매우 떨어지고, 개발 편의성도 다른 기술들에 비해 떨어지기 때문입니다.

