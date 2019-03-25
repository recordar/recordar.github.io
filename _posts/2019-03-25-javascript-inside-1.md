---
layout: article
title: 자바스크립트 개요 (1)
author: billie.jin
aside:
  toc: true
tags: JavaScript 자바스크립트
article_header:
  type: cover
  image:
    src: /assets/images/2019-03/25/javascript.png
---
## 자바스크립트란 무엇인가?
자바스크립트는 웹 브라우저에서 동작하는 스크립트 언어이다.
<br/>
<br/>
[W3C](https://www.w3.org/) 기관에서 [ECMAScript](https://www.ecma-international.org/publications/standards/Ecma-262.htm) 라는 스펙으로 언어를 정의하고 관리하고 있으며
<br/>
2019년 현재 ECMAScript2018(ES9) 명세까지 발표가 되었다.
<br/>
하지만 **E**CMA**S**cript2015(ES6)가 가장 활발히 사용되는 버전이다.
<br/><br/>
HTML, CSS와 함께 브라우저에서 실행되며, 주로 로직에 따라 [HTML DOM](https://developer.mozilla.org/ko/docs/Gecko_DOM_Reference/%EC%86%8C%EA%B0%9C)을 조작하는 일을 한다.
<br/><br/>

### 초기 자바스크립트
자바스크립트가 처음부터 웹 개발에 친숙한 언어는 아니었다.
<br/><br/>
모든 비지니스 로직은 서버에서 처리되었기 때문에 웹 브라우저에서의 자바스크립트는 사용자의 입력(이벤트)을 서버로 전달하는 역할이 전부였다.
<br/><br/>
따라서 .html 파일 내에 inline 형태로 간단한 이벤트 핸들링 자바스크립트 코드만이 포함되어 있었고, 복잡한 처리는 전부 서버에서 담당하였다.

{% highlight html linenos %}
<html>
<head>
  <script>
    function nameMyDiv() {
      document.getElementById("myDiv").innerHTML = "This div is my div";
    }
  </script>
</head>
<body onload="nameMyDiv();">
  <div id="myDiv">This div is your div</div>
</body>
</html>
{% endhighlight %}

<br/><br/>

### 모던 자바스크립트
통신 속도가 발전되고 모바일 시장이 커짐에 따라 웹 어플리케이션에 대한 수요는 폭발적으로 증가하였다.
<br/><br/>
이에 발맞추어 자바스크립트 프로그래머들에 의해 여러가지 연구가 이루어졌다. [prototype.js](http://prototypejs.org/), [jQuery](https://jquery.com/), [lodash](https://lodash.com/
), [knockout](https://knockoutjs.com/), [backbone.js](https://backbonejs.org/) 등 과 같은 주요 라이브러리들이 개발되었다.
<br/><br/>
이로인해 과거에 서버에서 담당하던 로직 계산들이 상당부분 웹 브라우저로 이동하였고, 자바스크립트는 이 변화의 중심에 서게 된다.
<br/><br/>
아래 [github.com](https://github.com) 저장소에 등록된 언어 랭킹을 보자.
<br/><br/>
![](/assets/images/2019-03/25/github-language-ranking.png)
<br/><br/>
자바스크립트가 이렇게 눈에띄는 발전을 할 수 있었던 것은 2013년 [Node.js](https://nodejs.org/ko/) 의 등장이 아니었나 싶다.
<br/><br/>
![](/assets/images/2019-03/25/github-major-languages.png)
<br/><br/>
초기 웹 플랫폼 시대때 자바스크립트는 오로지 브라우저에서만 실행될 수 있는 언어였다. 자바스크립트 엔진이 브라우저에 빌트인 되어 있었기에 자바스크립트 코드는 Chrome, Safari, IE 등 브라우저에서만 실행 해 볼 수 밖에 없었다.
<br/><br/>
하지만 2013년, 크롬 브라우저에 내장되어 있던 [V8](https://ko.wikipedia.org/wiki/%ED%81%AC%EB%A1%AC_V8) 자바스크립트 엔진이 [Node.js](https://nodejs.org/en/) 라는 이름으로 오픈소스화 되면서, 자바스크립트는 브라우저에서 자유로워 질 수 있었다.
<br/><br/>
그 말인 즉슨, 서버도 Node.js를 통해 자바스크립트 언어로 개발이 가능해졌고, 더욱 더 많은 개발자들이 자바스크립트를 사용하게 된 것이다.
<br/><br/>
Node.js 등장은 자바스크립트 생태계에 중대한 영향을 미쳤다. [npm 패키지 매니저](https://www.npmjs.com/)를 소개하고 CommonJS 모듈 형식을 대중화시켜 자바스크립트 언어 자체의 발전을 도와주었다. 개발자들은 더 혁신적은 도구를 만들고 브라우저, 서버, 그리고 기본 애플리케이션 사이의 경계를 흐리기 위한 새로운 접근법을 개발하기 시작하였다.
<br/><br/><br/>
다음 포스팅에서는 자바스크립트 언어의 활용 범위 및 특징에 대해서 살펴 보겠다.