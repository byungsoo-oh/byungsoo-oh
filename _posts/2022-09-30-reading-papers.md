---
layout: post
title: How to Read a Paper (번역 및 요약)
tags: [research]
comments: false
---

["How to Read a Paper"](http://ccr.sigcomm.org/online/files/p83-keshavA.pdf) (Srinivasan Keshav) 내용 정리

- 논문을 읽는 것에도 방법 / 기술이 필요 (처음부터 끝까지 무작정 흐름을 따라가면서 읽는 것은 비효율적일 수 있음)
- 3단계에 걸쳐 효과적으로 논문을 읽는 방법 소개 &rarr; 각 단계에서의 목적을 생각하고 정리하면서 읽으면 생산성 높일 수 있음

각 단계에 대해 요약하면 다음과 같음

## 1단계
- 논문을 high-level 관점에서 훑어보는 단계
- 5~10분 정도 소요
- 다음 순서대로 훑어보기:
  1. Title, abstract, introduction 주의깊게 읽기
  2. Section 및 sub-section headings 읽기 (*그 외 나머지는 무시*)
  3. Conclusion 읽기
  4. Reference 훑어보면서 읽은 논문 있는지 가볍게 확인해보기
- 이 단계의 목표: 다음 5가지 파악 &rarr; 2단계로 넘어갈 것인지 결정
  1. Category
  2. Context: 어떤 연구와 관련 있나? 문제 분석을 위한 바탕?
  3. Correctness: 논문이 가정하는 문제 상황이 타당한가?
  4. **Contributions**: main contributions?
  5. Clarity: 잘 작성된 논문인가? 
- 논문을 제출하는 입장에서 이 부분을 생각해 보기: 많은 리뷰어들이 이러한 짧은 scan을 통해 논문의 1차적 reject 여부를 결정할 수 있음. 이 단계에서 핵심을 이해하기 어렵게 글이 작성되어 있으면 본문의 디테일한 연구 내용과 무관하게 1차적 관문을 통과하지 못하게 될 수 있음 &rarr; 간결하고 명확하게 abstract 및 intro 작성하고 section 및 sub-section 제목도 쉽게 납득할 수 있게 명확한 흐름으로 작성하는 것이 1차적으로 매우 중요함

## 2단계
- 1단계에 비해 보다 구체적인 내용 정리함으로써 논문의 주요 내용 이해할 수 있어야 됨 &rarr; 다른 사람에게 논문의 핵심 및 근거 요약해서 설명할 수 있을 정도로 정리가 되어야 하는 단계 (남에게 충분히 논리적으로 설명할 수 있을 정도로 이해하고 있는가? 스스로 점검하면서 읽어야 되는 단계)
  - 핵심 포인트 적고 논문 여백에 코멘트 정리하면서 읽는게 도움 될 수 있음
  - Figures, diagrams 등 주의 깊게 보기
  - 아직 읽어보지 못한 references 표시해두기
- 최대 1시간 정도 소요

## 3단계
- **온전히** 논문을 이해하기 위해서는 논문을 **virtually re-implement** 해볼 수 있어야 됨: 해당 논문의 저자와 동일한 문제 상황을 가정하고 re-create를 해보기 &rarr; 그러고 나서 실제 논문의 접근과 비교해보기
  - **논문의 innovation 뿐만 아니라 hidden failings / assumptions 등도 파악할 수 있음**
- 디테일에 집중이 필요한 단계임: 모든 statement들의 가정을 파악하고 challenge 해봐야 됨
- Beginner: 4~5시간 / Experienced reader: 1시간 정도 걸릴 수 있는 작업
- 논문의 흐름을 일방적으로 따라가는 것이 아니라, 비판적으로 동일한 문제 상황에서 스스로 생각을 구체화시켜보면 보다 객관적으로 논문의 장단점을 파악할 수 있음
- 논문의 이해도를 높이는 데 좋은 방법인 만큼 내 연구 역량을 기르는 데에도 도움이 될 수 있는 방식인 것 같음

## 요약
- 논문 읽는 데에도 기술 필요함 &rarr; 3단계로 나눠서 차근차근 접근
- 1단계: 핵심 기여 파악 및 논문을 더 자세히 읽을지 여부 파악하기 위한 단계
- 2단계: 주요 주장 및 근거를 이해하기 위한 단계
- 3단계: 논문을 비판적으로 virtually re-implement 해보기

## Reference
S. Keshav, "How to Read a Paper" http://ccr.sigcomm.org/online/files/p83-keshavA.pdf
