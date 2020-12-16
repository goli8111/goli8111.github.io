---
title: Game Dev QA 전략
author: goli8111
date: 2020-12-14 12:00:00 +0800
categories: [Blogging, Dev QA]
tags: [writing]
---

# 효과적인 Game Dev QA 전략

효율을 높이기 위한 Game Dev QA 프로세스

목차
1. 현황
2. 사례
    * MS
    * Google
    * FaceBook
3. 전략 

## 1. 현황 ##

- 서비스 업데이트 사이클이 짧아 지면서 테스트는 병목 현상이 발생하고, 품질은 떨어지고 있음
- 고객은 더 빠른 대응을 원하는데 개발 구조의 변화가 없다면 더 빠르게 움직여야 함

## 2. 사례 ##

- 다른 IT 회사들은 어떻게 대응하고 있을까?

### Microsoft ###
- 1990년대
  - PM, Dev, QA 인원 비율이 0.5:1:1
  - 테스트 인력 구분
    - SDET(Software Design Engineer Test) 자동화, 테스트 인프라 담당
    - STE (Software Test Engineer) 자동화를 실행, 수동 테스트 담당
  - Windows 및 Office와 같은 대형 제품을 공식적인 품질 측정함. 성공적이었음.
  - 문제를 보이기 시작했지만 제품의 상업적 성공으로 인해 다소 가려졌음
- 1990년대 후반
  - 개발된 코드를 SDET 전달, SDET는 자동화 테스트를 STE 위임
  - STE는 외주 업체를 늘리는 형태로 인력으로 대응
  - 테스트 병목으로 업데이트 지연
- 2000년 초반(변환의 시작)
  - 인력대응 방식은 한계를 인식하게 됨
  - STE 역할 제거. SDET에 테스트 개발, 자동화 실행, 유지 관리 책임 맡김.
  - STE에게 고통스러운 시간(대부분 직종 전환 실패)
  - 개발팀과 단절된 상태로 SDET은 개발 속도를 따라가지 못함
  - 개발과 연결을 위해 릴리즈 단계까지 SDET 업무 영역 확장
  - 테스트 부채를 처리하기 위해 MQ(Quality Milestone)라는 개념의 도입해서 테스트 부채를 처리하는 단계 설정
    - MQ의 고정된 인력이 필요
    - 업무 우선순위에 대한 문제
    - 실제로 제대로 동작하지 않았음
- 2000년대 중반
  - 클라우드로 인해 상황이 반전 됨
  - 개발 사이클이 더 빨리 진행해야 한다는 압박
  - 긴 안정화 단계는 사라짐(베타 마일스톤, 고객 유효성 검사 테스트 사라짐)
  - 마이크로 서비스는 독립적이고 지속적인 배포
  - 서비스는 고 가용성, 다운타임 없는 배포 지원
  - 초기 대응은 우리가 하던일을 더 빠르게 하는 것
  - 빠른 대응은 한계점에 도달
- 현재
  - 클라우드 주기에서의 품질에 대한 접근 방식 변경
  - 품질 소유권 재정의(개발 의존도 높임)
  - 자주 배포하기 위해 master 브랜치가 항상 서비스 할 수 있는 단계가 되어야 함
  - 테스트를 앞단, 뒷단으로 배치하고, 중간 단계는 대부분 제거
  - 개발과 테스트의 책임을 결합한 (combined engineering)
    - 개발자는 테스터 교육을 받고
    - 테스터는 good design skill 배움
    - 관리자는 두가지를 매니징하는 방법 배움
  - 엔지니어는 단위, 통합, 성능, 배포, 라이브까지 책임
  - 동료의 설계, 코드, 테스트 검토가 더 중요해 짐
  - 별도의 개발, 테스트팀이 없음
- 결과
  - 하나의 개발조직에서 시작했지만 이제는 전사에 적용
  - 테스트 방식을 변경해야 한다는것을 인식이 중요함(shift-left, shift-right)
  - 전환에 실패한 인원은 다른 일을 찾아갔음
  - 핸드 오프 제거로 커뮤니케이션, 책임 회피 사라짐
  - 보안, 성능, 테스트등 전문화 된 영역이 필요했음. 개발팀을 서포트해주는 역할로 TF를 만들어 진행
  - 개발자가 한명이 해야하는 업무 범위는 늘어났지만 사실 개발팀 인원이 더 늘어 났음.
  - combined engineering 전환 비용이 들지만 핸드오프 감소, 테스트 효율 상승응로 퍼포먼스 상승됨

> **참고자료**:
https://docs.microsoft.com/en-us/azure/devops/learn/devops-at-microsoft/evolving-test-practices-microsoft

## 3.전략 ##



```yaml
---
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [TAG]     # TAG names should always be lowercase
---
```

> **Note**: The posts' ***layout*** has been set to `post` by default, so there is no need to add the variable ***layout*** in Front Matter block.

## Learn More

