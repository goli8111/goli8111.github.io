---
title: Google QA 방식 리뷰
author: goli8111
date: 2020-12-15 12:00:00 +0800
categories: [Google, Dev QA, Review]
tags: [writing]
---

# Google QA 사례 조사

목차
1. Intro
2. Microsoft case
3. Review

## 1. Intro ##
- Google QA 업무 프로세스 사례 조사
- 효율적인 개발 환경 구축을 위한 기반 자료 활용

## 2. Google case ##
- 구글은 전산학과 코딩 기술을 존중한다. 
  - 테스터가 그 클럽에 동참하려면 훌륭한 전산지식과 절묘한 코딩 기술을 갖추어야 한다.
  - 그래서 모든 테스터는 코딩이 능력을 가지고 있음
- 개발자는 개발을, 테스터는 테스트를 하는 것으로 분리하는 순간에 많은 문제가 발생
  - 간단한 테스트로 수정하고 고쳐질 수 있는 부분이, 여러 단계와 컴포넌트 및 시스템의 통합을 거쳐 손실이 커짐
- 직군은 3가지로 구분
  - SWE(Software Engineer)
    - 우리가 일반적으로 생각하는 개발자
  - SET(Software Engineer in Test)
    - 테스트 인프라 구축, 개발자가 좋은 테스트를 할 수 있도록 서포트
    - SWE와 같은 수준의 코딩 능력을 가진 개발자
  - TE(Test Engineer)
    - 반은 개발자, 반은 사용자 관점의 인원
    - 개발자들이 하지 못하는 더 좋은 테스트를 하는 것
- 소형 테스트 70%, 중형 테스트 20%, 대형 테스트 10% 비율로 진행
  - 모듈간의 결합도로 테스트 구분함
  - 소형 테스트는 코드의 품질 향상
  - 중대형 테스트는 제품 품질 향상
- 자동화 될 수 있고, 사람의 지식과 직관을 필요로 하지 않는 문제는 반드시 자동화
- 테스트 인증 프로그램을 진행해서 프로젝트 참여와 조직의 테스트 스킬과 성숙도를 높여가는 방식으로 진행
- 프로젝트 시작 후 20%만 출시가 됨. 그래서 제품이 서비스하기로 결정이 나면 그때부터 테스트 가능한 환경 만들기 시작
- 테스트 백과사전에 테스트에 대한 모든 것을 기록
  - 하지만 사람을 통해서 배우거나, 본인의 실패를 통해서 배우고, 코드리뷰의 피드백을 통해서 배움
  - 구글도 메뉴얼을 잘 만들어 놓아도 개발자들이 잘 보지 않는다고 함(^^)
- 결과
  - 적은 인원으로 테스트가 가능한 환경 구축
  - TE 직군이 가장 마지막에 생겨났는데, 직군 정의가 모호하다고 함
    - 수백개가 넘는 팀에서 TE를 유동적으로 운영하고 있다고 함
    - 테스트의 부족한 부분이 팀마다 달라서 수동테스트 위주로 운영하는 팀, 자동화 테스트만 작업하는 팀이 있다고 함
    - 전통적인 테스트 방식에서 부족한 부분을 TE가 유동적이게 보완하고 있음

> **참고자료**:
책 : 구글은 소프트웨어를 어떻게 테스트하는가

## 3.Review ##
- 소형, 중형, 대형 테스트로 구분하고 앞단의 테스트 비중을 높여 테스트 전체 비용을 낮추는 형태
  - 앞 부분에서 문제를 해결하면 뒤 부분은 비용이 Zero가 됨
  - 하지만 많은 프로젝트가 테스트 비중을 반대로 가져가고 있음
- 테스터는 뒤에서 버그를 찾는 것은 가장 비효율적인 방식
  - 버그가 발생하면 그 원인을 찾고 근본적인 문제를 해결하는 것에 초점을 맞춰야 함
  - 기본 기능 테스트는 개발자가 하는 것이 Hand-Off 비용이 발생하지 않는 가장 효율적인 방법