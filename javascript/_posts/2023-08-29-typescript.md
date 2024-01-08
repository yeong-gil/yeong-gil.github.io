---
layout: post
title: "타입스크립트(Typescript) 정리"
date: 2023-08-29 15:47:00 +0900
description: >
  Typescript 정리
lastmod: 2023-08-29 15:47:00 +0900
sitemap:
  changefreq: weekly
---

0. 
{:toc}

타입스크립트의 배경, 사용 이유와 동작 원리에 대해 정리해보겠습니다. 요즘 바닐라 자바스크립트 코드 보다 타입스크립트로 작업하는 일이 더 많이져 내가 느낀점도 첨삭하겠습니다.

# 타입스크립트(typescript)

타입스크립트는 자바스크립트에 타입을 부여하는 언어로, 마이크로소프트에서 개발, 유지보수하고 있는 자바스크립트의 확장버전 언어이다. 타입스크립트에서 원하는 타입을 정의하고 프로그래밍 하면 자바스크립트로 컴파일 되어 실행할 수 있다. 간단히 말해 자바스크립트에 타입을 정의하는 언어로 보면 될 것 같다.

[타입스크립트 홈페이지](https://www.typescriptlang.org/){:target="_blank"}<br/>
[타입스크립트 깃헙](https://github.com/Microsoft/TypeScript){:target="_blank"}
{:.note title="링크"}

# 장점

##  대규모 프로젝트 개발 시 협업에 이점이 있다.

협업 시에는 타 개발자가 작업한 코드를 볼일이 많아진다. 그런 경우 타입스크립트로 되어 있는 코드는 굉장히 빠른 이해를 돕는다. javascript에 경우 매개변수(parameter)나 리턴 타입을 주석을 달아주는 경우가 많다. 하지만 타입스크립트는 어떤 타입을 선언하고 리턴 받는지 다 정의하기 때문에 주석을 달지 않아도 구조 추론이 가능하다는 점에서 이점이 있습니다. 저 같은 경우에는 개발한지 오래된 코드는 일일이 기억 못해서, 타입스크립트를 쓰고 엄청한 편리함을 느꼈습니다.

## javascript의 단점을 보완할 수 있다.

앞서 말했듣이 타입스크립트는 자바스크립트의 확장버전 언어입니다. 우선 어떤 것들을 보완하여 나왔는지 알아보겠습니다. 

1. 자바스크립트는 `*동적 타입 언어`이다. 그러므로 타입을 정의되지 않아 값을 추론할 수 없다.<br/>
  -> 타입 정의로 보완하였다. 타입이 미리 정의하기 때문에 작업 시 생산성이 좋다.
2. 자바스크립트는 `*런타임`에서 타입이 결정되기 때문에 오류를 런타임에서 밖에 확인 할 수 없다. <br/>
  -> 컴퍼일 과정에서 오류 확인 가능하다. 이러한 타입 에러로 인한 문제점을 바로바로 확인 할 수 있어 안정성이 보장된다.

*동적 타입 언어의 자료형은 컴파일 시 정해지는 것이 아니고, 실행할 때 결정된다.

*런타임이란 구동되는 환경을 말한다. 자바스크립트의 런타임 종류로는 웹 브라우저(크롬, 엣지...), nodejs가 있다.

# 단점

## 타입 정의가 매번 좋은건 아닌거 같다...

작업 시 타입을 일일이 다 정의해줘야 하기 때문에 작업하면서 생각할게 많아진다. 그리고 타입 선언으로 인해 전체적인 코드의 양이 늘어나고 이로 인해 생산성이 낮아 질 수도 있다.
TypeError 빨간줄에 스트레스를 받는다... any를 남발하게 되면 타입스크립트를 쓰니만 못한 경우도 생긴다.

## 초기세팅

당연히 사용하기 위해서 감수해야 할일이지만 설치, 컴파일 옵션 등등 여러가지로 초기세팅 해줘야 할게 좀 있다.

## 러닝커브

자바스크립트와는 다르게 정적 타입 언어이기 때문에 러닝커브가 어느정도 높다고 볼수도 있다. 하지만 이 정도는 사람마다 다르기 때문에 누군가는 러닝커브가 굉장히 낮다고 생각할 수도 있다. 

# 마무리 

내가 느끼기에는 타입스크립트를 사용하며 얻는 장점(유지보수, vscode 여러가지 플러그인) 등등을 고려하면 사용하는게 좋다고 생각한다. 물론 경우에 따라 다를수 있지만 

글을 쓰며 더 타입스크립트를 공부하여 써볼 생각이 커졌다. 