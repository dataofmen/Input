---
title: "나의 LLM 코드생성 워크플로우 | GeekNews"
source: "https://news.hada.io/topic?id=19312"
author:
  - "[[neo]]"
published: 2025-02-19
created: 2025-02-25
description: "tldr: 스펙을 브레인스토밍하고, 계획을 세운 다음, LLM codegen을 이용해 실행함. 개별 반복 루프. 그러면 마법이 일어남나는 LLM을 이용해 다양한 소규모 제품을 빠르게 만들고 있음. 재미있고, 유용함그러나 잘못된 접근에 빠지면 시간을 크게 낭비할 수 있음많은 개발자들이 서로 비슷한 접근 방식을 가지고 있고, 아래는 나의 워크플로우임\"지금은 잘"
tags:
  - "clippings"
---
- tldr: **스펙을 브레인스토밍하고, 계획을 세운 다음, LLM codegen을 이용해 실행함. 개별 반복 루프. 그러면 마법이 일어남**
- 나는 LLM을 이용해 다양한 소규모 제품을 빠르게 만들고 있음. 재미있고, 유용함
- 그러나 잘못된 접근에 빠지면 시간을 크게 낭비할 수 있음
- 많은 개발자들이 서로 비슷한 접근 방식을 가지고 있고, 아래는 나의 워크플로우임

> "지금은 잘 작동하고 있지만 2주 후에는 작동하지 않거나 두 배로 작동할 수 있음"
- **개발 하는 방법은 2가지가 있음**
- **그린필드 코드**: 새로운 프로젝트를 시작
- **레거시 모던 코드**: 기존 코드베이스를 개선하거나 확장

## Greenfield: 처음부터 새로 시작하기

- “처음부터 시작하는” 상황에 잘 맞는 프로세스임
- 아이디어를 브레인스토밍하고, 문서화하고, 작은 단계별 계획을 세운 뒤 코드 생성 툴을 사용해 구현하는 흐름임
- **Step 1: 아이디어 구체화**
- ChatGPT 같은 LLM에 아이디어를 설명하면서, 하나씩 질문을 유도해 구체적인 스펙으로 정제함
- 마지막에는 상세한 스펙(spec.md)을 만들어 개발자에게 넘길 수 있는 문서 형태로 정리함
- 필요하면 Deep Research 같은 툴로 아이디어에 대한 근거 자료를 얻을 수도 있음
- **Step 2: 계획 수립**
- 스펙을 기반으로, 더 강력한 “이해·추론” 모델에게 세부 단계별 청사진을 생성하도록 요청함
- TDD 방식이든 아니든, 각 단계별로 작은 작업 단위를 만들고 순서대로 정리함
- 이런 프로세스를 통해 `prompt_plan.md`와 `todo.md`를 생성함
- `prompt_plan.md`는 코드 생성에 필요한 프롬프트 설계를, `todo.md`는 체크리스트를 포함함
- 이 계획 수립은 15분 정도면 충분한 편이며, 나중에 참조하기도 쉬움
- **Step 3: 실행**
- Aider, Cursor, Claude 등 다양한 코드 생성·도움 툴을 사용해 실제 코드를 작성함
- 대표적으로 Claude와 Aider를 예로 들 수 있음
- Claude 방식
- 미리 프로젝트 구조(boilerplate 등)를 셋업한 뒤, 단계별 프롬프트를 Claude에 입력함
- 결과 코드를 IDE에 복사·붙여넣기하고 테스트를 수행함
- 문제가 생기면 `repomix` 같은 툴로 현재 코드베이스를 Claude에 전달해 디버깅함
- 워크플로우
- Repo 셋업 (boilerplate, uv init, cargo init, etc)
- Claude에 프롬프트 붙여넣기
- claude.ai 에서 IDE 로 copy & paste
- 코드 실행, 테스트 실행 등
- …
- 동작하면, 다음 프롬프트로 이동
- 동작하지 않는다면, Repomix 를 이용해서 코드베이스를 Claude에 보내 디버깅
- 이 작업을 반복(rinse repeat)
- Aider 방식
- Aider에서도 `prompt_plan.md`를 순서대로 입력해 작업함
- 자동으로 테스트를 돌려주거나, 오류를 찾고 수정하는 과정을 지원함
- 필요 시 대화형 디버깅을 통해 문제를 해결함
- Repo 셋업 (boilerplate, uv init, cargo init, etc)
- Aider 실행
- Aider에 프롬프트 붙여넣기
- Aider가 춤추는 것 보기 ♪┏(・o･)┛♪
- Aider가 테스트를 실행하거나, 앱을 실행해서 검증 가능
- 동작하면, 다음 프롬프트로 이동
- 동작하지 않으면, Aider와 Q&A 하면서 고침
- 이 작업을 반복(rinse repeat)
- 결과
- 이러한 방식으로 스크립트, Expo 앱, Rust CLI 등 여러 프로젝트를 짧은 시간 안에 구현해볼 수 있음
- 미루고 있는 크고 작은 프로젝트가 있다면 한 번 시도해 보는 것을 추천
- 새 언어나 기술을 배우며 빠르게 시도해볼 수 있다는 장점이 있음

## Non-greenfield : 기존 코드에 대한 점진적/반복 작업

- 이미 존재하는 코드베이스에 작은 작업을 반복적으로 적용할 때 쓰는 방법임
- 전체적인 큰 계획보다, 작업 단위별로 구체적 요청과 결과를 주고받는 흐름임
- **컨텍스트 확보**
- `repomix` 같은 툴을 사용해 코드베이스를 요약해 LLM에 전달할 수 있음
- `mise` 등으로 반복 설정을 관리하며, `output.txt`라는 파일에 요약 결과를 저장함
- 너무 큰 코드베이스의 경우, 필요한 부분만 요약하도록 조절함
- **예시 워크플로우**
- `mise run LLM:generate_missing_tests` 같은 명령으로 테스트가 부족한 부분을 LLM에 파악시킴
- Claude나 Aider로 해당 제안 사항(이슈)을 적용하고, 결과를 다시 테스트함
- 이렇게 기존 코드베이스를 점진적으로 개선해 나감

## 주요 프롬프트 예시

- **Code review**  
“시니어 개발자로서 코드를 꼼꼼히 리뷰해 줄 것. 줄 번호와 맥락 포함. 허술한 리뷰 없이 깊이 있게 살펴볼 것”  
“You are a senior developer. Your job is to do a thorough code review of this code. You should write it up and output markdown. Include line numbers, and contextual info. Your code review will be passed to another teammate, so be thorough. Think deeply before writing the code review. Review every part, and don't hallucinate.“
- **GitHub Issue generation**  
“시니어 개발자로서 코드를 검토하고, 주요 이슈를 Github 이슈 형식으로 작성해 줄 것”  
“You are a senior developer. Your job is to review this code, and write out the top issues that you see with the code. It could be bugs, design choices, or code cleanliness issues. You should be specific, and be very good. Do Not Hallucinate. Think quietly to yourself, then act - write the issues. The issues will be given to a developer to executed on, so they should be in a format that is compatible with github issues“
- **Missing tests**  
“시니어 개발자로서 코드를 검토하고, 누락된 테스트나 필요한 테스트를 구체적으로 제시해 줄 것“  
“You are a senior developer. Your job is to review this code, and write out a list of missing test cases, and code tests that should exist. You should be specific, and be very good. Do Not Hallucinate. Think quietly to yourself, then act - write the issues. The issues will be given to a developer to executed on, so they should be in a format that is compatible with github issues“

## 스키 ᨒ↟ 𖠰ᨒ↟ 𖠰

- LLM을 활용해 빠른 속도로 코드를 작성하다 보면, 어느 순간 복잡성이나 문맥이 엉켜 혼란스러워짐
- 계획 단계(예: Greenfield 프로세스)의 문서를 다시 확인하거나 테스트를 체계적으로 작성해 두면 도움이 됨
- 빠르게 움직이는 만큼, 잠시 휴식을 취하거나 생각을 정리하는 과정을 가지는 것도 중요함

## 나는 매우 외로워 (｡•́︿•̀｡)

- 대부분의 LLM 기반 워크플로우가 ‘1인 모드’에 최적화된 상황임
- 팀 단위로 함께 코딩하려고 하면 충돌이나 머지 문제 등이 복잡해짐
- 여러 사람이 동시에 LLM을 활용할 수 있는 ‘멀티플레이어형’ 협업 환경이 발전하기를 바람

## 시간

- LLM을 통해 코드 작성 효율이 크게 높아졌지만, 토큰 처리 대기 시간으로 인해 생기는 ‘다운타임’이 있음
- 이 시간을 이용해 다른 프로젝트 아이디어를 구상하거나, 음악을 듣거나, 대화를 나누는 식으로 활용함
- 개인 생산성이 이전보다 크게 상승하는 경험을 하고 있음

## Haterade ╭∩╮( •̀\_•́ )╭∩╮

- 많은 친구들이 “빌어먹을 LLM, 이거 완전 쓸모없음” 같은 태도를 보이며, 나는 이런 관점을 크게 신경 쓰지는 않음
- 물론 나도 그 입장을 공유하지는 않지만, 의심의 눈초리가 필요한 건 사실임
- AI를 싫어할 이유는 무궁무진하고, 내가 가장 걱정하는 건 전력 소모와 환경적 영향임
- 그래도… "코드는 흘러야 함" 그렇지… 에휴
- 만약 더 알고 싶지만 굳이 사이보그 프로그래머가 되고 싶지 않다면, 내 추천은 “의견을 바꾸지 말고, Ethan Mollick의 ‘Co-Intelligence: Living and Working with AI’를 읽어보라”는 것임
- 이 책은 기술 무정부주의적 자본주의 스타일의 과장 없이, LLM이 주는 이점을 잘 풀어냄
- 개인적으로 크게 도움을 받았고, 이 책을 읽은 친구들과도 훨씬 깊은 대화를 나눌 수 있었음
- 적극 추천함