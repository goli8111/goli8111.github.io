---
title: Facebook QA 방식 리뷰
author: goli8111
date: 2020-12-15 12:00:00 +0800
categories: [Facebook, Dev QA, Review]
tags: [writing]
---

# Facebook QA 사례 조사

목차
1. Intro
2. Facebook case
3. Review

## 1. Intro ##
- Facebook QA 업무 프로세스 사례 조사
- 효율적인 개발 환경 구축을 위한 기반 자료 활용

## 2. Facebook case ##
- 테스터 직군이 존재하지 않음
- 입사때부터 개발자에게 테스트가 작업에 일부임을 명확히 함
- 고객 관점의 테스트는 사내 베타 테스트 운영으로 피드백을 받음(Dog-Fooding 프로그램)
- 자동 테스트를 안착 시키기 위한 노력을 많이 진행
- 코드 업데이트 시 테스트 결과를 같이 첨부하는 방식으로 진행
- 테스터 없이 운영할 수 있는 이유는 무책임하게 사이트에 변경을 하는 것을 부끄럽게 여기는 문화에 있음

> **참고자료**:
Never Send a Human to do a Machine’s Job: How Facebook uses bots to manage tests
https://docs.google.com/presentation/d/1FobpyXuNHK4-2yPrBGAlHnhJll3xFl84_OyP0HVqvKc/edit#slide=id.g3f5cc2519_6148(PPT가 워낙 부실해서 영상과 같이 보는 것을 추천)

## 3.Review ##
- 개발자는 최고의 테스터
- 개발자에게 테스트를 시키는 것이 가장 효율이 높은 방식이라고 판단함
  - 개발 스펙을 테스터에게 전달하고, 이해시키고 하는 부분은 비용이 매우 큰 부분
  - 이렇게 하고 싶지만 현실은 개발자 인력 수급이 쉽지 않은 부분이 문제