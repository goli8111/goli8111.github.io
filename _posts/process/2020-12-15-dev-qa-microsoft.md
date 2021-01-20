---
title: Microsoft QA 방식 리뷰
author: goli8111
date: 2020-12-15 12:00:00 +0800
categories: [Microsoft, Dev QA, Review]
tags: [writing]
---

# Microsoft QA 사례 조사

목차
1. Intro
2. Microsoft case
3. Review

## 1. Intro ##
- Microsoft QA 업무 프로세스 사례 조사
- 효율적인 개발 환경 구축을 위한 기반 자료 활용

## 2. Microsoft case ##
- 1990년
  - 테스트 인력 구분
    - SDET(Software Design Engineer Test) : 자동화 테스트 구축, 테스트 인프라 담당
    - STE (Software Test Engineer) : 자동화를 수행, 수동 테스트 담당
  - 테스터는 테스트에만 집중 할 수 있는 환경이라 테스트에 깊은 전문성이 생김
  - Windows 및 Office와 같은 대형 제품을 공식적인 품질 측정을 성공적으로 진행
- 2000년
  - QA를 인력 증가로 대응 방식의 한계를 인식
    - 개발자와 테스터의 인력 비율이 1:1
  - STE 역할 제거. SDET에 테스트 개발, 자동화 실행, 유지 관리 책임 맡김
    - 조직간의 업무가 전달 되면서 발생하는 Hand-Off 비용 감소
    - 통합된 SDET 조직에 품질에 대한 책임감 부여
  - STE은 SDET로 전환을 하거나 다른 직종으로 전환하게 됨(많은 인원이 직종 전환 실패)
  - 여전히 개발팀과 단절된 상태에서는 문제가 발생
  - 개발과 연결을 위해 릴리즈 단계까지 SDET 업무 영역 확장
  - 일정이 부족한 문제를 해결하기 위해 테스트 부채를 처리하기 위해 MQ(Quality Milestone)라는 개념의 도입
    - MQ의 항상 고정된 테스트 인력이 필요하게 되는 문제 발생
    - 업무 우선순위에 대한 문제
  - 개발팀과 단절된 상태로 SDET은 개발자 코딩 속도를 따라가지 못함
- 2010년
  - 업데이트가 더 빨리 진행해야 한다는 고객의 압박
    - Window 업데이트 주기가 2년에서 6개월, 3주로 변경됨
    - 마이크로 서비스는 독립적이고 지속적인 배포를 요구
    - 서비스는 고 가용성, 다운타임 없는 배포를 요구함
  - 긴 안정화 단계는 사라짐(베타 마일스톤, 고객 유효성 검사 테스트 사라짐)
  - 효율을 높이는 방식으로 대응
- 현재
  - 구조적인 변화 없이는 한계점 도달. 접근 방식의 변경
  - 타회사 사례를 조사
  - 품질 소유권 재정의
    - Quality Ownership
      - Combined Engineering 도입(테스터 + 개발자 업무 결합)
    - Master is always shippable
      - 빠른 배포를 위한 Master 작업장은 항상 서비스 가능한 상태
    - There is no place like production
      - 기존 production 방식의 QA 방식을 버림
      - 개발자 테스트의 부족한 부분을 보완하는형태 추가
      - 고객에게서 피드백 수집
  - 개발과 테스트의 책임을 결합한 (Combined Engineering)
    - 개발자는 테스터 교육을 받아야 함
    - 테스터는 good design skill 배워야 함
    - 관리자는 두가지 업무를 매니징하는 방법 배워야 함
    - 개발자는 단위, 통합, 성능, 배포, 라이브까지 책임
    - 동료의 설계, 코드, 테스트 검토가 더 중요해 짐
- 결과
  - 하나의 개발조직에서 시작했지만 Microsoft 전사에 적용
  - 테스트 프로세스를 변경해야 한다는것을 인식이 중요함
  - 전환에 실패한 인원은 다른 일을 찾아갔음
  - 구조 변화로 커뮤니케이션 비용 감소, 책임 회피 사라짐
  - 보안, 성능, 테스트등 전문화 된 영역이 필요했음. 개발팀을 서포트해주는 역할로 TF를 만들어 진행
  - 개발자가 한명이 해야하는 업무 범위는 늘어났지만 QA인력 감소한 부분을 개발팀 인원 충원
  - 업무 퍼포먼스가 상당히 개선 됨

> **참고자료**:
https://docs.microsoft.com/en-us/azure/devops/learn/devops-at-microsoft/evolving-test-practices-microsoft

## 3.Review ##
- 전통적인 개발 방식에서 변화를 가져온 것은 "고객들의 잦은 업데이트 요구" 이 부분이 핵심적인 내용
- 빠른 업데이트를 위해 우리의 개발 프로세스도 그에 적합한 방식으로 변경이 되어야 함
