---
layout: post
cover: 'assets/images/cover7.jpg'
navigation: false
title: 1.[rails]루비기초와 구름IDE
date: 2019-10-08 10:18:00
tags: dev
subclass: 'post tag-dev'
logo: 'assets/images/ghost.png'
author: Gyutae Han
categories: abraham
---

우리 팀의 프로젝트가 레일즈프로젝트로 결정되었지만 레일즈프로젝트를 시작하기 전, 평소 자바와 자바스크립트에 익숙하던 저에겐 새로운 언어란 도전이었기 때문에 먼저 해야할 것은 루비라는 언어의 공부였습니다. 
ruby를 공부하려면 로컬에서 직접 루비를 다운로드 받아서 공부를 하던가, 가상머신을 이용하던가, 클라우드를 이용하던가 여러가지 방법이 있습니다만 저희들이 이번에 택한 건 바로 **구름IDE**였습니다.

### 구름IDE란?
>   ![Screen-Shot-2019-09-08-at-20.33.51](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-20.33.51.png)웹 기반 클라우드 코딩 서비스인 구름은, 네트워크만 연결되어 있다면 접속하는 것 만으로 별다른 설정 없이 C, C++, Java, Python, Ruby 등 다양한 언어로 프로그래밍을 하실 수 있는 환경을 제공합니다. 또한 강력한 협업 기능을 제공하여, 다른 프로그래머들과 손쉽게 동시 프로그래밍이 가능하도록 도와드립니다. 구름IDE를 통해 때와 장소를 가리지 않고 효율적인 소프트웨어 개발을 경험해보세요!
>   << 출처: 구름IDE 공식홈페이지 >>
>

위에 공식홈페이지에서 언급한 것처럼 설치, 설정이 필요없이 바로 코딩이 가능한 서비스입니다.
비슷한 서비스가 여러 곳이 있지만, 기본적으로 한국어에 에듀서비스까지 포함되어 있기 때문에 구름을 이용하였습니다.

[(참고)구름IDE, 바로 실행해보면서 배우는 ruby](https://edu.goorm.io/learn/lecture/2011/%EB%B0%94%EB%A1%9C-%EC%8B%A4%ED%96%89%ED%95%B4%EB%B3%B4%EB%A9%B4%EC%84%9C-%EB%B0%B0%EC%9A%B0%EB%8A%94-ruby/lesson/81541/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%EC%9D%B4%EB%9E%80)


### 루비(ruby)
[위키피디아](https://ko.wikipedia.org/wiki/%EB%A3%A8%EB%B9%84_(%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D_%EC%96%B8%EC%96%B4))를 보면 [마츠모토 유키히로](https://en.wikipedia.org/wiki/Yukihiro_Matsumoto)라는 사람이 개발한 **동적객체지향스크립트프로그래밍언어**라고 나와있는데 자바스크립트나 파이썬 비슷한 언어라고 생각했습니다. 하지만 공부하면서 루비만의 매력을 느꼈는데 다음 글에 모듈과 블록, 믹스를 다루면서 언급하겠습니다. 이번 편에는 간단한 변수선언방식, 문자열선언, 반복문등을 써보며 느낀점을 적으려합니다.


### 변수선언
> ![Screen-Shot-2019-09-08-at-21.20.10-1](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-21.20.10-1.png)
> ![Screen-Shot-2019-09-08-at-21.20.10-2](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-21.20.10-2.png)

기본적으로 변수 선언을 할 때는 자바나 자바스크립트처럼 변수타입을 설정할 필요가 없이, 변수명만 쓰고 할당받을 값만 선언해주면 끝입니다. 장점도 있을테고 단점이라고 생각하면 단점이라고 생각할 수도 있는 점이라고 생각합니다.


### 문자열
> ![Screen-Shot-2019-09-08-at-21.43.47](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-21.43.47.png)
> ![Screen-Shot-2019-09-08-at-21.43.50](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-21.43.50.png)

문자열 선언은 큰 따옴표와 작은 따옴표 모두 사용이 가능합니다.
기본적으로 더하기(+)연산을 이용하여 문자열 합치기, .length()이용한 길이구하기등 기본적으로 자바나 자바스크립트와 흡사합니다. 위 to_s는 숫자형을 문자열형으로 바꿔주는 메소드입니다.


### 조건문
> ![Screen-Shot-2019-09-08-at-22.00.53](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-22.00.53.png)
> ![Screen-Shot-2019-09-08-at-22.00.57](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-22.00.57.png)

조건문중 가장 대표적인 구문은 *if*문입니다. 다른 언어와 마찬가지로 기본 구조는 다음과 같습니다.

> if 조건
> &nbsp;&nbsp; code...
> end

조건문에는 자바처럼 소괄호()가 있어도 되고 없어도 되는 것을 확인하였고, 중괄호{}는 포함하니 에러가 나는 것을 확인하였습니다. 그리고 조건문이 있는 행에 코드를 적으면 에러가 발생하기 때문에 조건문이 끝나고 새로운 행에 코드를 적어야 합니다. 마지막에 end는 필수입니다.

### 반복문
> ![Screen-Shot-2019-09-08-at-22.15.10](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-22.15.10.png)
> ![Screen-Shot-2019-09-08-at-22.15.13](http://localhost/content/images/2019/09/Screen-Shot-2019-09-08-at-22.15.13.png)

반복문중에는 *for*문과 *while*문이 있습니다. 구조는 다음과 같습니다.

> for 변수 in 표현식 [do]
> &nbsp;&nbsp; code...
> end

> while 조건 [do]
> &nbsp;&nbsp; code...
> end

위 처럼 단순히 숫자를 설정하여 *0..5*를 설정하면 0부터 5까지 변수 *i*에 대입이 되고 반복문이 가능합니다. 

### 다음 장
이번 장에서는 기초적인 변수선언, 반복문, 조건문, 문자열들을 다루어 봤습니다. 다음 장에서는 모듈, 클래스, 믹스등 루비만의 특징이 잘 살려져있는 기능들을 다루어 보려고합니다. 

### 참고
* [구름IDE 공식홈페이지](https://www.goorm.io/)
* [루비: 위키피디아](https://ko.wikipedia.org/wiki/%EB%A3%A8%EB%B9%84_(%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D_%EC%96%B8%EC%96%B4))
* [마츠모토 유키히로: 위키피디아](https://en.wikipedia.org/wiki/Yukihiro_Matsumoto)