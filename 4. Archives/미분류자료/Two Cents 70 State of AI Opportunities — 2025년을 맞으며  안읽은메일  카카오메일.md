---
title: "[Two Cents #70] State of AI Opportunities — 2025년을 맞으며 | 안읽은메일 | 카카오메일"
source: "https://mail.kakao.com/top/UNREAD/0000000000008QT"
author:
published:
created: 2025-01-09
description:
tags:
  - "clippings"
---
2024년을 마무리하는 시점에서 지난 한 해를 돌아 보면, 여전히 AI 시장은 엄청난 속도로 변화하고 있다.

지금 당장 시장에서 일어나는 일 뿐 아니라, 짧게는 2-5년 길게는 7-10년 단위로 시장의 흐름을 예측해야 하는 초기 투자자로서는 (웨인 그레츠키의 표현대로) “where the puck is going to be” 지점을 예상, 추정해 보는 것이 일상이다.

이 시각에서 앞으로 어떻게 AI 시장에 진화해 갈 지에 대한 생각을 주기적으로 정리한 것을 공유해 본다.

시장의 흐름을 이해하려는 의도이기 때문에 가능하면 특정한 기술, 제품에 대하여 깊이 들여다 보기 보다는 전반적인 시장 흐름에 더 집중한다.

개략적으로, 전체 시장 흐름의 시작점이 되는 미국 시장에서의 기술과 시장 흐름을 훑어 보고, 이를 기반으로 국내에서의 시장 기회를 살펴 보기 위하여 중국에서의 사례와 국내 시장 흐름을 간단하게 정리한다.

이를 기반으로 현재 HRZ에서 집중하여 보고 있는 AI 투자 thesis들에 대해서는 추후 별도 포스팅으로 정리해 보려고 한다.

생성 AI에서 LLM은 그 기반 위의 모든 것을 가능/불가능하게 하는 기반 기술/플랫폼이기 때문에 이 흐름에 대한 이해가 기반이 되어야 한다고 본다.

**SOTA LLM hitting the “data wall”?**

예상대로 올해에는 GPT-5라고 할만 한 GPT-4를 훌쩍 뛰어 넘는 SOTA LLM 모델은 발표되지 않았다.

Llama-4는 2025년에 출시될 것이라 이미 발표가 되었고, GPT-5 진행 과정에 대하여 [아주 부정적인 언론 보도](https://substack.com/redirect/3fec06df-4d08-446c-9096-90275ca38215?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)도 나왔고, 최근에는 Data Wall 이슈가 화두인 만큼이나 2025년 GPT-5 급 모델 출시에 대한 기대가 크지만, 현실적으로 2025년에도 GPT-5라고 할만한 (GPT-4 대비 성능이 크게 발전한) SOTA 모델이 나올 가능성은 상대적으로 낮아 보인다.

이에 대한 몇 가지 생각을 정리해 보면:

> Base model에 최대한 많은 학습 데이터 기반의 pre-training으로 Generative Space를 구축하고, 이 기반으로 zero shot, few shot으로 원하는 답이 바로 나오기를 기대하는 현재의 monolithic 모델 기반 구조가 더 이상 유효하지 않을 것이라고 본다. 이는 1T parameter 모델 대비 10x 이상 규모의 모델 학습에 필요한 가용 학습 데이터 더 이상 충분하지 않기 때문에 이 방식의 scaling이 더 이상 가능하지 않다고 보기 때문이다. (”Data Wall 이슈”)
> 
> [Llama 3.3](https://substack.com/redirect/94de6667-bd4a-456c-a9bc-5d593737ec4a?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), [Qwen 2.5](https://substack.com/redirect/32a410bb-bb70-4ed0-b6d9-95a791805c2e?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) 등 2024년의 많은 mid-sized LLM에서 보여 주었듯이, 기존의 scaling law에 따르지 않고 15T 내외 토큰으로 상대적으로 작은 모델을 학습하면 (scaling law에 따른 최적화가 되지 않지만) 모델에 내재하는 ‘지능’은 학습 데이터 규모에 따라 (그 증가 속도는 점차 체감하지만) 더 좋아지는 현상을 통해 볼 때, (실제 현업 적용될 떄의 inference cost까지 고려하면) 모델 규모 자체를 무한정 키우기 보다는 상대적으로 작은 규모의 모델에 더 많은 학습 데이터를 투입하는 추세가 더 많아질 것으로 예상된다. 마침 [FineWeb dataset](https://substack.com/redirect/6ba2af1b-bb4c-4c4b-888f-33420b68734e?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)도 그 정도 규모의 학습 데이터를 오픈소스로 공개되었고.
> 
> GPT-4에서 기존의 monolithic 구조에서 MoE 구조로 변화한 것이 (동시에 동작하는 parameter 수를 줄임으로써) inference cost를 줄이는 방안에 대한 고려때문이기는 하지만, 결과적으로 GPT-4 수준의 intelligence를 얻기 위하여 굳이 1T+ 규모의 monolithic model이 필요한 것은 아니라는 것을 검증하였기 때문에, 자연스레 다음 단계의 진화 방향은 상대적으로 작은 (Expert 당 1T 이하?) 규모의 expert model들의 네트워크/그래프 형태로 전체 시스템 구조 확장이 가능하다는 것을 확인한 셈이다. 그러면, 각 expert model이 최대 1T 규모 (가용 학습 데이터 양, 필요한 domain knowledge 수준을 고려하면 expert model당 500B를 크게 넘어설 필요성/가능성은 낮아 보인다), 전체 규모 최대 5T~10T 규모의 MoE 내지는 유사한 방식의 (예: MoA) 네트워크 구조가 다음 단계 SOTA 모델이 되지 않을까 추정해 본다. 그리고, 이 것이 (GPT-3.5에서 GPT-4로의 jump와 같은) order of magnitude 성능 개선의 마지막 단계가 되지 않을까 한다.

이러한 배경에서, o1, o3에서 보여 준 inference 단계 reasoning 기반 방식이 소위 AGI에 더 가까운 지능 수준을 보여 주었다는 점에서, 학습 단계보다 inference 단계에서 더 많은 작업을 통해 원하는 지능 수준을 얻어 내는 (소위 “test time compute”) 방식이 앞으로 더 보편화될 것으로 예상된다. (학습 단계에 GPU compute 자원을 최대한 투자하고 zero/few-shot inference를 하는 기존 방식 대비 pre-training에 GPU compute 자원을 상대적으로 적게 투자하고 inference 단계에 더 많은 compute 자원을 투여하는 방식이, TCO 측면에서는 (즉 전체 compute 자원 수요 측면에서는) 훨~씬 더 커질 것이다. 장기적은 운영 측면에서 어느 방식어 더 효과/효율적일지는 향후 실제 use case의 비중에 따라 전체 추세가 한 쪽을 기울어질 것으로/선호할 것이다.)

이에 대한 시장에서의 implication는, 이제 ($10b 규모의 모험 투자가 가능한) 미국 시장만이 아니라 다른 시장에서도 SOTA 수준의 모델 구축이 가능하게 되면서, 점차 (몇 년간에 걸쳐) SOTA LLM에 대한 시장 평준화로 수렴할 것으로 예샹된다. (최근 중국 스타트업 [DeepSeek-V3 모델](https://substack.com/redirect/7118b5dc-ce5d-42b8-bc72-0e417c0d5b97?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) 및 V2 기반 reasoning model [DeepSeek-r1](https://substack.com/redirect/33b046fb-0753-417f-a309-0e14c27b3ded?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) 을 참고해 보자) 물론 모든 시장에서 그런 일이 일어난다기 보다는, 몇 억 달러 규모의 모험 자본, 정부 자금 투자가 가능한 10개 이내의 시장에서 그렇게 될 것으로 본다는 의미이다. (진심으로 한국이 이 그룹에 참여할 수 있으면 좋겠다)

**Mid-market as the “[$600B](https://substack.com/redirect/a699743a-e927-4db9-b311-ffb15ac3b7d8?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)” main battlefield**

(자본과 기술의 경합 현장인) SOTA 모델 경쟁과는 별도로, 실제 비즈니스 현장에 적용되는 LLM은 mid-market, multi-modal, coding, reasoning 등의 각 측면에서 치열한 경쟁이 일어나고 있다.

Mid-market에서는 Meta Llama, Anthropic, Mistral 뿐 아니라 중국, UAE 등 많은 시장에서 경쟁적으로 70B~400B 규모의 LLM을 경쟁적으로 발표하고 있고, 각각에 대한 open-source equivalent도 대개 1-3개월 이내에 발표되고 있다.

Reasoning 모델도, o1 발표 몇 개월도 안 되어서 Alibaba Qwen/QwQ, DeepSeek r1 외에도 OSS 버젼 ([OpenR](https://substack.com/redirect/94b3e41f-8393-4090-af47-0744f49884e1?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)) 까지 발표되었고,

첫 번째 horizontal killer app이 되고 있는 coding 분야도 (Llama, Mistran, Qwen 등) mid-sized LLM 거의 대부분이 coding variant를 같이 발표하고 있는 등,

이제 이 시장에서의 edge는 LLM 존재 여부 및 성능 경쟁이 큰 의미가 없어지고, 이 기반으로 어떤 vertical/segment에서 어떤 value proposition을 만들지, 이를 위하여 어떻게 특화하고 어떤 biz use case를 만들지 등의 비즈니스 측면이 촛점이 되고 있다.

지난 번 글에서 언급한 AI21, Landing AI와 같이, SOTA 모델이 아닌 mid-sized model 기반으로 enterprise use case를 만드는 것에 집중하는 경우가 향후 몇 년간 가장 큰 비즈니스 가치를 drive할 것으로 보인다. (새로운 LLM/기능 중심의 신기술/제품 보도에서는 크게 다루어지지 않고 있지만)

**Multi-modal for Creatives**

Multi-modal 생성 분야에서는, 2023년이 이미지 생성 모델의 경쟁이었다면, 2024년은 동영상 생성 모델 경쟁의 해가 된 듯 하다.

OpenAI Sora의 일반 공개, Google Veo 2 외에도 중국 Kuaishou Kling, Bytedance등의 shorts 생성 모델 등이 숨가쁘게 공개되었고, (이미지 생성 분야에서 2023년 말 MIdjourney이 $200m 규모의 ARR에 도달한 이후) 2024년 후반에는 동영상 생성 분야에서 Runway가 $100m에 가까운 ARR에 도달하였다.

이 규모의 매출의 성격이 B2C인지 B2B인지 명확히 구분되지 않지만, multi-modal 생성 LLM의 응용 분야는 (문서 작업이 많은 지식 노동자, 광고 업계, 크리에이터, 오픈마켓 판매자 등) 대개 B2B 분야에서의 사용이 주된 것으로 추정된다.

Multi-modal 분야에서의 경쟁은, 이제 오디오 (기존의 STT 응용을 넘어서, TTS 오디오 생성 및 real-time API에 의한 음성 대화 중심으로), 음악 (이해, 생성), 3D 모델 (3D 모델, 모델 동작 생성)을 넘어서, 3D 월드의 실시간 생성 ([Google Genie 2](https://substack.com/redirect/7c8ec451-f90f-4fab-8f15-1cfe7def97a6?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), [World Labs](https://substack.com/redirect/431dddf8-cc38-47b8-9117-0dbb4701c4f0?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk))으로 그 범위를 확장해 가고 있다.

Language Model에 의한 자료의 요약, 분석, 생성 등에 의한 생산성 증대 효과가 10x 규모라고 보면, multi-modal 생성은 100x 내지 그 이상의 효과가 있기 때문에 이 생성 결과를 필요로 하는 분야에서의 생산성 향상 효과는 훨씬 더 클 것이다.

특히 3D world의 실시간 생성과 같은 새로운 modality는 게임, (이제는 죽어 가는 키워드가 되었지만) 메타버스 등 이제까지 상상하지 못하였던 새로운 가능성까지 제시하고 있어, 이러한 다양한 방향으로의 multi-modal 확장은 앞으로 2-3년간 완전히 새로운 기회가 될 것으로 예상된다.

당초에는 이러한 creative를 위한 multi-modal LLM이 단순히 하나의 feature로서 다른 플랫폼의 하나의 기능으로 수렴할 것으로 예상했었는데, multi-modal 분야 use case의 value proposition이 기존 방식 대비 100x 정도의 효과가 있기 때문에, (B2C인가 B2B인가에 상관없이) 당분간 의미있는 규모의 시장이 될 것으로 본다.

물론 (게임 개발 툴, 실시간 3D virtual space 생성 등) 다른 영역의 새로운 use case의 핵심 부분으로서도 계속 성장할 것이고 장기적으로 이 시장에서의 기회가 훨씬 더 커질 것이라고 보지만.

**SLM**

예상치 않게 SLM 분야가 2024년 가장 치열한 경쟁이 보였던 분야라고 판단된다.

SLM 발표 타임라인에서 보듯이, 2024년에는 대부분의 Big Tech에서 SLM이 발표되었고,

![](https://substackcdn.com/image/fetch/w_2420,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2847e03-8f96-4d44-af03-cf1ab4bfb3e8_1210x686.png)

최근에는 (Ph-4에서 보듯이) 10B 규모를 넘어서기 시작하면서 mid-market LLM과 중복되기 시작하였다.

당초 SLM의 주된 응용분야를 스마트폰의 on-device AI로 보고 “5년이내 on-device AI가 내장된 스마트폰 10억대가 보급”되는 것이 어쩌면 [“생성 AI의 Netscape moment”](https://substack.com/redirect/236e1bf1-33a1-438d-a780-5a64e634343e?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)가 될 수도 있다고 보았는데,

SLM의 새로운 응용 분야로서 랩탑/데스크탑 기반으로 “개인용/소규모기업용 생산성 도구”등 기업 내부에서의 niche market에서 활용될 가능성도 충분히 보인다. 기업의 LLM 도입 형태와 구성이 복잡 다양해지면서 “SLM 기반으로 RAG/fine-tuning된 in-house LLM”을 개인/소규모 기업 단위로 운영하는 것등이 use case가 등장할 수도 있겠다는 생각이다. 특히 비용효율성이 가장 중요한 요소가 되는 환경에서.

**Non-language Models as New Frontiers**

텍스트, 일반적인 multi-modal 이외의 영역으로 생성 AI가 확장되는 것은, 아주 넓은 새로운 영역에서 새로운 기회를 만들 수 있을 것이며 그 대상 시장에 따라 아주 큰 규모의 새로운 시장 가능성이 열릴 수 있을 것으로 본다.

Multi-modal 영역에서 이제 막 등장하기 시작한 3D 모델/동작 생성 및 3D 월드의 실시간 생성은, 게임 생성/플레이 외에도 virtual world 기반의 완전히 새로운 양식의 interaction/엔터테인먼트 기회도 가능할 것으로 보이며,

로봇 분야는 이미 다양한 유형의 로봇 (biped 휴머노이드, quadruped robot dog, 양팔 로봇/상체 휴머노이드 등)이 개발되고 있으며, 무엇보다 그 동작을 위한 VLA (vision-language-action) 모델 분야도 2023년 말 Google RT-2 이후 [Physical Intelligence](https://substack.com/redirect/e2605b45-bc47-4f97-a32f-a2b1529dae33?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), [Skild](https://substack.com/redirect/14315be4-4747-48d1-893c-2600adba31dc?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)등 수억 달러 규모 펀딩을 받는 스타트업들이 본격 등장하면서 2024년 이 분야의 시장 경쟁이 본격화된 것으로 보인다.

로봇 분야는, 현재 기술 수준에서 이미 제조업 분야에서 보편적으로 사용하고 있는 [산업용 로봇](https://substack.com/redirect/1165583e-3c6c-415b-aad9-1d0aecfbb3d2?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)뿐 아니라, 그보다 더 큰 규모로 더 빠르게 성장하는 [전문 분야](https://substack.com/redirect/96f8fe79-004e-4232-ae89-bc8485663b7b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) 및 일상 생활 분야의 [서비스 로봇](https://substack.com/redirect/1bfe3f5a-0290-41a8-99d7-d3e21ac35d13?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)까지 다양한 vertical/활용분야에 적용되고 있으며, 생성 AI 기술과 결합하면서 (기존 로봇 프로그래밍의 정형화된 움직임을 넘어서는) 훨씬 더 광범위한 분야에 적용이 가능해지면서 직간접 노동력 대체 효과가 본격적으로 일어날 수 있을 것으로 본다. (이는 아래에서 언급할 Langauge Model에 기반한 지식노동자의 노동력 대체 효과와 비견할만 한 것으로 보인다.)

바이오, 제약 분야도 이에 못지 않은 규모의 시장에서 큰 변화가 진행되고 있다. DeepMind 자회사 [Isomorphic Labs가 Norvatis, Eli Lilly와 $3b 규모의 R&D 프로젝트](https://substack.com/redirect/f3a0bc5d-aff8-4339-8c7c-6b5c9c97961d?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)를 진행하는 것에서 볼 수 있듯이, 이 분야의 시장 규모는 통상 IT 분야와 단위가 다른 규모로 진행된다. DeepMind의 AlphaFold, AlphaProteo 외에는 아직 주목할만 한 프로젝트가 보이지 않지만, 이 분야는 장기적 투자에 의한 R&D가 그 기반이 될 것이라고 본다. (국내에서 이 분야에 주목할만한 결과를 만들 수 있을지에 대해서는 아직 잘 판단이 안된다)

**“AI Picks & Shovels”**

예상대로 (기업 규모와 관계없이) 기업의 AI Transformation 추세는 예상보다 빨리 진행되고 있다. 절대적으로 많은 수의 기업에 적용된다기 보다는, 예상보다 다양한 유형의 use case에 빠르게 적용/적응한다는 의미에서. 국내에서도 마찬가지로.

자연스럽게 기업의 AI 도입을 위한 도구 (MLOps/LLMOps 툴 및 관련 tech stack의 tool layer. LLM도 포함)들이 가장 먼저 다양한 구조의 시장을 만들고 있다. 그 전반적인 흐름은 [Menlo Ventures의 2024년 시장 상황 보고서](https://substack.com/redirect/a4de67a8-c2c8-4a9f-882f-e27e1ce0a0a2?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), [Enterprise AI stack](https://substack.com/redirect/a0bfff20-acac-4639-acaf-89e9ba0a099f?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), [Navigating the LLMops landscape](https://substack.com/redirect/1b7fd793-bb75-49f8-9d13-35f79590003b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) 등을 참고하면 좋을 듯 하다.

이 흐름에 대한 몇 가지 관찰을 공유하자면:

- 초기의 기업 도입은 RAG 기반 방법론이 대세를 이루고, 이와 관련된 orchestration layer (LangChain, LlamaIndex 등), vector DB (PineCone 등), evaluation/observability, security 등의 tool layer는 빠르게 성장하면서, 점차 빼곡하게 채워지고 있고, 동시에 (기술, 방법론의 진화를 따라) 다양하게 진화하고 있다. (예: Graph RAG, multi-agent 등)
- 이러한 tool layer에서 치열한 경쟁 환경 하에서, Glean (기업내 검색 horizontal tool), LangChain (orchestration layer)등 몇몇 선발/선두 주자 외에는 아직 뚜렷한 winner가 많이 보이지는 않고, 시장 전반적으로도 아직 foggy한 상태
- 또 하나 특이한 점은, (이전 다른 tech cycle과는 좀 다르게) 새로운 기술로 무장한 후발 스타트업 대비, 기존 incumbent player의 시장 장악 효과가 상당히 큰 것으로 보인다. 특히 LLM/AI app 기저에 기업내 데이터에 대한 접근과 가공이 필요한만큼, Databricks, Snowflake 등이 기업내 데이터 레이어에 대한 접근을 이미 장악하고 있는 점에서 AI Transformation 시장을 먼저 차지하는데 아주 유리해 보인다. 기업내의 workflow을 선점하고 있는 Salesforce의 AgentForce 플랫폼이 multi-agent 기반 기업용 AI app/workflow에도 더 유리해 보이고. (TMI이기는 하지만, 미국 현지에서는 전략 측면에서 앞서 가고 있는 Databrick를 Snowflake가 조금 힘겹게 따라 가는 듯 느낌) VectorDB 분야도 PineCone 등이 먼저 시작하였지만, incumbent DB player가 자연스레 vector DB를 통합하면서 시장의 주도는 incumbent player 측으로 넘어가고 있는 듯 한 것과 마찬가지로.
- 이 과정은 좀 더 지켜보아야 할 듯 하다. 만일 이 구도가 계속 유지된다면, 신생 Enterprise AI 스타트업들은 ‘플랫폼화’ 과정을 거치기 전에 (MS/Google/AWS 등 포함하여) 이들 incumbent에 의한 M&A가 주된 exit path가 될 듯 하며, 그렇다면 이 분야에서 ‘플랫폼이 되는’ ‘venture-scale return’이 가능한 초기 투자 기회는 생각보다 많지 않을 수도 있겠다는 생각.
- 현재까지는, 기업의 내부 데이터, 구조에 맞는 custom AI apps를 직접 개발, 공급, 서비스하는 System Integrator 들이 첫 번째 wave의 가장 큰 수혜자가 될 것으로 보이는데, 이 플레이어들이 이 단계의 다양한 프로젝트 기반으로 ‘SaaS’ 등 형태의 ‘플랫폼화’ 단계로 진화할 것으로 예상된다.
- 이 사업/비즈니스 구조의 진화 과정은 지난 30년간 SaaS 비즈니스의 구조가 진화해 온 것과 (똑같은 형태는 아니지만) ‘비슷한 운율’을 띌 것으로 예상된다.
- 이를 좀 더 설명하자면: 현재의 ‘SaaS 플랫폼’ 유형을 구분해 보면, (vertival 별, 기업 규모별) 기업군 대상의 horizontal tools (예: SalesForce), (vertival 별, 기업 규모별) 기업군 대상 vertical tools (예: vertical trade 대상의 ServiceTitan), 특정 vertical 대상 integrated (예: Toast. 식당 대상. 핀테크까지 통합) 등 몇 가지 유형으로 나누어진다. 기업용 AI apps도 초기의 단순 co-pilot 툴에서, (RAG 기반) customized biz app 단계를 지나고, 이후 (더 큰 규모로 성장하기 위한) 플랫폼화 과정에서 이와 비슷한 몇 가지의 비즈니스 구조/value prop을 가지는 유형으로 플랫폼화 과정을 거칠 것으로 예상된다.
- 물론, 그 방식이 SaaS에서는 (기존의 기업 워크플로우가 유지되면서) 그 워크플로우를 위한 (외생의) tool로 남았던 것과 비교해서, AI app은 좀 더 워크플로우 자체를 변화 시키고 이를 실행하는 인력 조직 구조의 변화/대체까지 진행될 것이기 때문에, 기업의 조직 및 워크플로우에 대한 AI apps의 영향은 더 깊은 수준까지 미치겠지만. (아래에서 더 설명할 “Service as Software” “Sell work, not tools” 패러다임의 영향을 많이 받을 것이라는 의미에서)
- 이 진화 과정을 거쳐서 ‘플랫폼화’되어 sustainable moat를 구축할지 여부는 각 기업의 역량에 따라 달라질 것이며, 이 ‘플랫폼화’ 진화를 하지 못하면 장기적으로 얼마나 큰 venture-scale return을 만들 수 있을지는 의문이 있다. (90년대 후반의 ‘웹 에이전시’의 선례를 보면)

**Coding**

Coding은 가장 먼저 use case와 adoption을 찾은, 가장 시장 효과가 큰 horizontal area가 되었다.

Github co-pilot은 가장 먼저 상용화한 이후 2024년6월 기준 [Annualized ARR $200m~300m로 추정](https://substack.com/redirect/e7832c05-071f-42ce-9e65-fa2e6a5a4593?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)되며, 이는 [Midjourney의 2023년 말 ARR $200m](https://substack.com/redirect/f151b94b-5b7b-47ed-925f-3943bb139f68?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)과 비교될만 한 규모로, 특정 niche 시장으로서는 유독 빠른 매출 성장을 보이고 있다.

이러한 가능성에 따라 이 시장은 수많은 스타트업이 등장하고 있으며 (Devin, Cursor 등), 오픈소스 (SWE-Agent)의 경쟁 뿐 아니라, 수많은 LLM도 coding 전용 모델을 별도 출시하고, 기본 LLM 자체의 경쟁 (o1/o3, Gemini 2)도 상당히 빠른 속도로 성장하는 등, 가장 치열한 전장이 되고 있다.

최근 Cursor의 부상이 보여 주듯이, (기존 치열한 경쟁에서 생존, 성장한 SaaS 툴들이 그랫듯이) 결국 사용자 워크플로우에 가장 잘 맞는 ‘좋은 제품’ 몇 개가 (선발 incumbent인 Github copilot과 함께) 시장을 나누어 가질 것으로 보인다.

이 시장에서의 경쟁과정과 winner를 보면, 앞으로 등장할 horizontal tool 시장에서의 AI product가 (기능, 가격, 툴 통합 등) 어떤 경쟁 우위를 통하여 시장을 선점하고, (기능 확장 및 인접 통합 등) 수평적 확장 및 개별 vertical market으로의 침투를 어떻게 만들어 갈 지에 대한 시금석이 될 듯 하다.

(최근 주목하며 열심히 사용하고 있는 ‘회의록 작성 툴’ [Granola](https://substack.com/redirect/91bd26db-713c-42f4-a99c-e26c05680605?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)를 보면서도 비슷하게 느끼고 있다)

**Agents: 2025년 Enterprise AI 시장의 main battlefield**

2024년 하반기 시장에서 가장 빠르게 떠오른 키워드가 multi-agent 혹은 Agent 이다.

2023년 AutoGPT, BabyAGI의 첫 prototype 이후, 2024년 들어 [‘스스로 진화하는’ 모델](https://substack.com/redirect/ce1b7da9-f05f-4a45-931e-b37c70710f6c?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)등 다양한 실험도 등장하고, 이를 기반으로 한 상용 AI app 개발을 위한 tools이 다양하게 등장하면서 (LangChain, Microsoft, IBM, AgentOps, Dust 등) 기업 환경에 Agent 방식을 적용하기 위한 툴 환경은 지속적으로 좋아졌다.

시장에서 이보다 더 중요한 것은, Agent 방식을 적용하여 (기존의 SaaS 패러다임에 버금가는, 규모로는 그보다 10x~100x 더 큰) 비즈니스 use case를 만들 수 있다는 새로운 비즈니스 패러다임이 만들어지고 있다는 점이다. (아래 Y Combinator의 [Vertial AI Agent](https://substack.com/redirect/bfdbb067-fec4-4ac1-8027-cdec89dc4a16?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk) thesis 참고)

기존의 SaaS 툴을 대체하는 AI Agent 방식으로 (Vertical AI Agent), 기업의 기존 워크플로우 혹은 노동력/조직 단위를 바꾸고/대체하는 (Services as Software, Sell work not tools) 과정에서 기존 SaaS 대비 (tool 시장으로만 보면) 10x 내지 (tool 시장이 아닌, 노동력을 대체하는 시장으로 보면) 100x 규모의 시장 기회가 만들어질 것으로 본다.

(이런 hype이 시장에서 늘 옳았던 것만은 아니지만) 2025년의 Enterprise AI 시장의 가장 큰 패러다임, 새로운 기회, 어쩌면 아주 거대한 새로운 wave의 시작점이 Agent 기반의 Enterprise AI 시장이 될 것이라고 본다.

(“Enterprise AI 시장에서 Agent의 기회”에 대하여 따로 자세하게 생각을 정리해 보아야 할 듯)

**그 외 몇 개의 키워드들**

- Graph RAG, MoA (Mixture of Agents: RAG 기반 기업용 AI app을 더 효율적으로 만들기 위한 다양한 특화/optimization 툴
- Knowledge workspace (Google NotebookLM, OpenAI Canvas, Claude Artifacts): 어쩌면 개인 지식 노동자의 일상적인 생산성 툴은 이러한 workspace tool 기반으로 될 수 있을 듯. 기존 Office365 혹은 Notion 등 지식노동자의 업무 결과물을 다루고 저장하는 기반 툴을 대체하는
- Computer Use (Anthropic, Google): 지난 수십년동안 쌓인 기존 기업용 앱의 사용에 AI Agent를 적용할 수 있는 기반 기술이 될 수 있는, 엄청난 규모의 시장 가능성에 대하여 주목할 필요 있음. 미국 시장에서는 당연히 수십년간 쌓인 기업용 앱이 상당한 규모의 시장을 만들겠지만, 국내에서도 은행 내부 계정계, 물류/제조업 등의 전통 기업 내부 전산시스템 앱 등에서 큰 기회가 있을 수 있을 것으로 봄
- Sub-quadratic model (SSM/Mamba, Liquid Model): (아직 100B 이상 규모에서는 검증이 되지 않았지만) 지속적으로 inference optimization을 위한 sub-quadratic model에 대한 실험 지속 중

Enterprise에서의 AI 도입/Transformation은 [크게 3단계의 과정을 거칠 것이라고 보며](https://substack.com/redirect/4dc75e70-c2ce-486f-9b9f-19c7f58a7893?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), 현재는 그 초기 co-pilot 단계, 즉 단순한 툴로서의 도입 단계를 막 지나고 있다고 본다.

**1단계**: co-pilot (현재 단계)

- 기존 툴에 AI 기술을 접목/통합하여 생산성의 incremental 증대
- 예: RAG 기반 기업 업무 app
- 예: Office, Slack, Notion 툴 + AI, Github Co-pilot

**2단계**: 워크플로우 +AI (이제 막 진입하려는 단계)

- AI가 기업 워크플로우와 밀접하게 통합되고, 다음 단계로 워크플로우 및 관련 인력/조직에 변화를 가져 옴
- 예: 2025년 대규모로 예상되는 AI Agent 기반 툴?

**3단계**: AI로 인하여 기업 내부/외부의 완전히 새로운 behavior 등장

**변화의 양태에 대한 생각**

AI가 enterprise의 business app에 적용되는 과정이 기존 소프트웨어, SaaS 툴과 질적으로 구조적으로 다른 몇 가지 특징이 있고, 이 “질적으로/구조적으로 다른 몇 가지 특징”이 Enterprise AI 비즈니스가 향후에 어떻게 전개될 지에 큰 영향을 미칠 것이라 본다.

- 기존 SaaS 툴을 개발하는 것과 비교하여, AI 기술로 비슷한 역할을 하는 SaaS 툴을 개발/운영하는 비용이 order of magnitude 적어진다. 이러한 변화는 기존에는 “규모의 경제” 논리에 의하여 가능하지 않았던 niche 분야의 툴을 “경제적으로” 만들어 내는 것이 가능해졌다는 의미가 된다.
- 기존 워크플로우를 그대로 두고 그 효율을 어느 정도 (30%~100%) 높이는 것에 머무르지 않고, 그 워크플로우 자체를 변화시키며, 많은 경우 워크플로우를 담당하고 있는 인력/조직 구조를 일부/전체 대체하는 형태로까지 진행될 수 있다. 이 과정에서 AI app/툴은 단순히 툴에 그치지 않고 (인력/조직 구조의 변화를 통하여) “지식노동자 노동력을 대체”하는 형태로 고객 기업에 영향을 미치게 된다.
- 이것의 의미는 “(기존의 워크플로우를 있는 그대로 두고 이를 더 효율적으로 만들어 주는) 새로운 기술 기반의 툴을 도입하는 것”이 아니라, “AI 기반의 새로운 방식이 비즈니스 워크플로우에 적용되면서 워크플로우 자체 및 이를 운용하는 인력/조직 구조까지 변화하게끔 만드는 새로운 패러다임”을 의미한다.
- 비유하자면, 20세기 초반 완전히 새로운 방식의 대량생산 구조를 새로 만든 포드 자동차의 생산방식 [Fordism](https://substack.com/redirect/c73c9b4b-0ea7-41c1-8fcb-361566590162?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)에 비견할만 한 변화라고 본다.

이러한 몇 가지 특징에 기반한 추정으로서, 2024년에 관찰한 향후 Enterprise AI 패러다임의 변화는 아래 3개의 키워드로 정리해 볼 수 있다.

**"AI-ification of SaaS" into "verticalization of everything”**

AI 툴은, 현재의 horizontal SaaS 및 vertical SaaS 툴의 효율을 빠르게 높이는 형태로 시장에 먼저 진입하겠지만, 시간이 지나면서 현재 형태의 SaaS 툴 구조 그대로 단순히 그 효율을 높이는 형태에 그치지 않고 다른 형태로의 변화를 시작할 것으로 본다.

AI 툴의 도입으로, 초기 효율화 과정을 거치면서 기업의 워크플로우 자체의 변화 및 관련 인력/조직의 변화/대체에 대응하여, AI 툴 자체도 그 coverage, 제공 형태, pricing model 등이 상당히 바뀔 것이다.

그 변화의 방향, 형태는 AI 툴의 기능, 대상 고객 기업 규모, 고객 기업에의 정량적/정성적 변화의 형태에 따라 아주 다양한 형태로 나타나겠지만, 예상되는 몇 가지 특징을 살펴 보면:

- 제공되는 AI 툴의 target coverage가 대상 vertical, 필요로 하는 기능/역할에 따라 아주 세분화되어 제공 가능해질 것이다. (기존의 SaaS는 개발 비용때문에 가능하면 넓은 고객 군을 타겟으로 하는, 특정 vertical 전체, 혹은 모든 vertical에서 공통으로 필요로 하는 horizontal function 전체를 제공하는 플랫홈 화 추세를 띄어 왔다. 이와 비교해서, AI 툴은 특정 vertical의 특정 function을 대상으로 하는 툴을 만들어서, 더 효율적인 매출, 비용 구조 기반으로 서비스가 제공 가능할 것으로 예상된다. 이에 따라, AI 툴 시장은 기존 SaaS 대비 아주 많이 세분화되어 제공되는 형태도 가능할 것으로 예상된다.
- 고객이 얻게 되는 value proposition이 단순히 특정 기능 관련 비용을 30-50% 줄이는 것이 아니라, 상당한 규모의 labor cost 절감이 가능해지고 그 과정에서 기존의 per-seat, per-usage 기반의 pricing 보다(outcome-based, 절감되는 비용/노동력에 비례하는 가격 등) 아주 다른 유형의 pricing이 등장할 수 있다.
- 아주 단순하게 예를 들어 보면, 여러 계약서를 비교 검토하는 변호사의 업무를 보조하는 AI 툴은 기본적으로 변호사의 생산성을 10배 이상 높여줄 수 있다. 이 경우, 변호사가 기존의 hourly charge 방식을 유지하여 기존 방식 대비 1/10의 비용을 청구하면 변호사 입장에서는 AI 툴 도입의 가치를 누릴 수 없다. 또 AI 툴 공급사 입장에서는 점차 이 툴을 사용하는 변호사의 수와 그 사용량이 모두 줄어들 것이다. 이를 해결하기 위하여서는, 도입 고객 (변호사)가 먼저 (AI 툴을 통해 몇 배 좋아진 생산성 기반으로) 기존 서비스의 가격 구조/방식을 바꾸어야 할 것이고, 이러한 툴을 공급하는 AI 업체도 이에 맞는 새로운 pricing 방식이 필요할 것이다. 여기에서 한 단계 더 나아사면, AI 툴을 공급하는 업체가 굳이 단순한 툴 공급 업체로 남아야 할 이유도 없을 것이다. 자신이 직접 first-party가 되어 직접 변호사 서비스를 제공하면서, (AI 툴을 활용하여) 기존 경쟁사 대비 몇 배 더 효율적인 서비스를 제공하는 형태의 변화도 가능할 것이며, 실제로 이러한 형태의 변화도 [생각보다 빨리 이미 일어나고 있다](https://substack.com/redirect/6961095d-c635-4c42-99da-13ce037e525b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk).
- 하지만, 그럼에도 AI 툴을 제공하는 공급사의 구조는, 구조적으로 scalability를 지향하면서 기존의 SaaS 플랫폼이 타겟 시장과 value proposition을 나누어 갔던 것과 유사한 과정/구조를 거칠 것으로 예상된다. 정확히 똑같은 구조로 나누어진다기 보다는, 그 패턴이 유사하게 펼쳐지지 않을까 한다. 같은 과정이 “반복”되는 것이 아니라, 비슷한 패턴으로 “rhyme”되는. (위 AI Picks & Shovels에서 설명하였듯이) 현재의 ‘SaaS 플랫폼’ 유형을 구분해 보면, (vertival 별, 기업 규모별) 기업군 대상의 horizontal tools (예: SalesForce), (vertival 별, 기업 규모별) 기업군 대상 vertical tools (예: vertical trade 대상의 ServiceTitan), 특정 vertical 대상 integrated (예: Toast. 식당 대상. 핀테크까지 통합) 등 몇 가지 유형으로 나누어진 것과 비슷한 패턴으로.

이와 관련한 생각은 아래 몇 개의 글에서 더 자세히 살펴 볼 수 있다.

[The Verticalization of Everything - NfX](https://substack.com/redirect/cddbc04d-ac6f-482d-9217-00e57c6b909e?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

> Possibly, in the form of “unbundling” of major SaaS categories, like ERP, CRM, into verticalized, AI-powered, workflow-optimized solutions for each vertical

[Vertical SaaS: Now with AI Inside | a16z](https://substack.com/redirect/d0b0ce16-99a0-40a2-8216-2fc9698f569f?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

["AI Inside" Opens New Markets for Vertical SaaS | a16z](https://substack.com/redirect/78d0191b-2ac6-49d2-bc95-9f4411647d4f?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[Part I: The future of AI is vertical - Bessemer Venture](https://substack.com/redirect/198a173f-a553-4c6d-998a-2bfdff75ee6f?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

**“Service as Software” “Sell work, not tools” "digital/AI labor" emerging (rapidly)**

지금까지의 SaaS 툴과 달리 AI app/툴은:

- “기존 워크플로우를 그대로 두고 그 효율을 어느 정도 (30%~100%) 높이는 것에 머무르지 않고, 그 워크플로우 자체를 변화시키며, 많은 경우 워크플로우를 담당하고 있는 인력/조직 구조를 일부/전체 대체하는 형태로까지 진행될 수 있다. 이 과정에서 AI app/툴은 단순히 툴에 그치지 않고 (인력/조직 구조의 변화를 통하여) “지식노동자 노동력을 대체”하는 형태로 고객 기업에 영향을 미치게 된다.
- 이것의 의미는 “(기존의 워크플로우를 있는 그대로 두고 이를 더 효율적으로 만들어 주는) 새로운 기술 기반의 툴을 도입하는 것”이 아니라, “AI 기반의 새로운 방식이 비즈니스 워크플로우에 적용되면서 워크플로우 자체 및 이를 운용하는 인력/조직 구조까지 변화하게끔 만드는 새로운 패러다임”을 의미한다.

이러한 차이의 가장 큰 효과는, 그 타겟 시장이 기존의 소프트웨어 SaaS 시장이 아니라, 기업에서 지식 노동자가 담당하였던 노동력 시장으로 확대된다는 점이다. 기존 소프트웨어 SaaS 시장 및 IT 서비스/인프라 시장 TAM은 각각 $600b 내지는 $1.5조/$4조 규모인데 비하여, 지식노동자의 노동력 시장 TAM은 지식 노동 아웃소싱 시장 $4.6조 내지 글로벌 지식노동자 GDP $20조 규모로 확대된다는 의미이다.

이에 따라, 기업의 워크플로우를 위한 AI app/툴의 개발은 이러한 기업의 AI adoption 방식의 변화를 염두에 두고/반영하여, 기존 SaaS 툴과는 방식의 가치 창출 (value proposition) 목표, 가격 체계 등을 만들고, 고객 기업 대상의 영업 방식 (대상, 프로세스, sales pitch)도 변화를 가져와야 할 것이라고 본다.

이와 관련한 생각은 아래 몇 개의 글에서 더 자세히 살펴 볼 수 있다.

[AI leads a service-as-software paradigm shift - Foundation Capital](https://substack.com/redirect/79d85255-7566-4bea-b5ac-fc3977878e88?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[AI 시대의 SaaS: Service-as-a-Software | 매쉬업벤처스](https://substack.com/redirect/0596769b-5493-414e-b862-7c943d0741bc?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[AI Is Driving A Shift Towards Outcome-Based Pricing | a16z](https://substack.com/redirect/5d68e752-ca80-4e0b-8e04-1a4702c1fa7a?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[AI startups: Sell work, not software - Sarah Tavel](https://substack.com/redirect/4edab155-3a1a-425c-805c-0e31bdeff93c?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[A few "Sell Work, Not Software" updated thoughts - Sarah Tavel](https://substack.com/redirect/1ffb2e15-9ec0-490a-98ea-121d1553fba1?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

**“AI-native businesses” emerging**

어쩌면 AI 기반으로 이제까지 우리가 경험하였던 것과는 전혀 다른 유형/방식의 기업 형태, 가치 창출이 가능해질 듯 하다.

- AI를 도입 활용하는 기업은 해당 툴을 사용하는 업무의 효율을 단순히 30~100% 정도 증대하는 것에 그치지 않고, 이러한 워크플로우 변화 및 인력/조직 구조의 변화를 통하여 몇 배의 비용 절감(과 그에 따라 몇 배 수준의 이익률 개선)이 가능해질 수 있다.
- 간단히 예를 들어 설명해 보면, 매출 100억, G/M 50%, 영업이익률 10% 규모의 기업은 매출의 40%를 비용 (opex)으로 지출한다. 이 비용을 (AI를 통하여) 절반으로 줄이면 영업이익률이 10%에서 30%로 ‘급증’한다.실제로는 비용을 절반 이하로 더 줄일 가능성도 있고, ‘매출 원가’도 더 절감하여 G/M 자체를 더 높일 수도 있다. 예를 들어, 광고 크리에이티브 제작, 물류 센터의 pick&pack 비용 등은 통상 ‘매출 원가’로 계상되며, 이러한 유형의 비용은 AI로 절감이 가능하다.
- 이러한 방식으로, 기존에는 통상 수십 명의 팀이 연간 100억 매출에 영업이익률 10% 정도로 운영되는 중소기업이, 10명 이내 혹은 극단적으로는 1-2명 인력으로 같은 100억 규모 매출에 영업이익율 50% 이상의 super-profitable SMB가 가능해질 수 있다. Sam Altman이 이미 “[1인 $1B 기업](https://substack.com/redirect/a4024e17-e46c-4f26-a9e5-70f2b0e5483a?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)”이 [가능하다고 주장](https://substack.com/redirect/c496cc08-6c98-48ae-90bd-1108a17998ef?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)하기도 하였지만, 현실적으로 보아도 “100명 인력 $1B 매출” 기업도 충분히 가능할 수 있다고 본다.
- 이렇게 super-profitable SMB가 가능해지면, 이제까지의 방식과 아주 다른 VC/PE playbook도 등장할 수 있다. 이 방식이 가능하다는 것이 확인되면, 수많은 기업이 이 playbook에 따라 만들어질 것이고, 그 중 많은 기업은 그 자체로 (즉, 상당한 이익을 내는 100억 매출 규모의 기업으로) 남아 있을 것이고, 일부 기업은 (아마 PE 자본의 투입으로 이런 방식의 구조 변화가 가능한 미국에서 이런 사례가 많이 나타날 것으로 예상되는데) 이러한 “AI 기반 높은 수익성”으로 무장한 신생 기업이 오래된 기존 전통 기업을 (LBO 등의 방식으로) 인수하고, 이후 “AI 구조 조정”을 통하여 “기존 전통 기업의 큰 규모 매출과 distribution 기반으로, AI로 가능해진 높은 수익성”을 확보한 새로운 유형의 기업으로 등장할 수 있다. 우리 예상과 달리, 미국에서는 이미 [그러한 사례](https://substack.com/redirect/6961095d-c635-4c42-99da-13ce037e525b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)가 생겨났다. (이 방식은 전형적인 PE playbook에 적합한 기업 구조가 될 것이다). 현실적으로 “1인 100억 매출” 기업은 VC의 투자 대상이 되기 어렵지만, 이러한 기회를 활용한 새로운 PE playbook가 큰 기회로 등장할 수도 있다.

이와 관련한 생각은 아래 몇 개의 글에서 더 자세히 살펴 볼 수 있다.

[sam lessin on X: "The SaaS Era is Over; Software is a Business Tool not a Business Model](https://substack.com/redirect/f4ad71fc-34a5-4206-a37d-65cebe167779?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)" / X

**이 3가지의 결합으로서의 Virtual AI Agent thesis, 그리고 우리의 과제**

이제 Enterprise 시장 대상의 AI app/툴/서비스를 만들기 위해서는, 이러한 완전히 새로운 패러다임에 의한 변화가 가능할 것이라는 전제 하에 이러한 변화에 맞는 가치 창출 (value propositon)이 가능한 비즈니스 기회를 찾아야 할 것이다.

위의 변화 양태 및 키워드만 하더라도 이제까지와는 전혀 다른 방식의 생각이 필요할 것이며, 이후에 새로운 발견, 깨달음에 기반한 더 큰 변화도 가능할 것이다. 이러한 (상당히 abstract한) 키워드를 기반으로, 지금 단계에서 현실적으로 적용 가능한 비즈니스 모델을 만들어 내는 것이 필요하며, 이 것이 기존의 제품, 비즈니스 모델을 만드는 과정과는 상당히 다른 방식의 생각이 필요하기 때문에 쉽지 않을 것이다.

하지만, 이 기회를 먼저 인지하고 그 기회를 선점할 수 있다면, (지금까지 여러번의 tech cycle에서 증명되었듯이) 새로운 큰 기회를 먼저 잡을 수 있을 것이라고 본다.

그 한 예로서 Y Combinator의 Virtual AI Agent thesis를 참고하면 좋을 듯 하다.

YC의 Vertical AI Agent thesis는, “verticalization of everything”, “Service as software” 키워드가 결합하여 가능해진 비즈니스 구조이며, 기술적으로 multi-agent 기반으로 실현될 수 있는 큰 기회라고 본다.

[Vertical AI Agents Could Be 10X Bigger Than SaaS | Y Combinator](https://substack.com/redirect/bfdbb067-fec4-4ac1-8027-cdec89dc4a16?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

![](https://substackcdn.com/image/fetch/w_2912,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac91b533-4b6f-4463-aa55-2a3271e9fd9f_1474x1846.png)

Consumer 시장에서는 아직 눈에 띌만한 움직임이 보이지는 않는다.

몇몇 이미지, 동영상 생성 툴은 이미 $1~3억 이상 규모의 ARR을 만들고 있는데, 그 매출은 (B2C라기 보다는) 지식노동자들이 자신의 업무 툴로 사용하는 사실상의 B2B 용도가 대부분이라고 추정되며,

컨텐츠 생성 + AI Companion + 소셜 서비스 등이 결합한 [몇 몇 실험](https://substack.com/redirect/1a3258fe-5c20-4cd6-88af-2d4ce8a1ca8e?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)이 등장하고 있기는 하지만, B2C 챗봇 분야에서, Character.ai가 의미있는 규모의 성과에도 불구하고 (어떠면, 그 성과 덕분에) 예상보다 빨리 acq-hire 된 경우 외에는 아직 눈에 띌만한 Consumer를 위한 AI 서비스가 없다.

어쩌면 Consumer AI 서비스는 미국보다는 한국, 중국 등의 동아시아 시장에서 먼저 몇 가지 killer app이 등장하지 않을까 하는 기대를 하고 있다. (90년대 말 웹 시대에 먼저 한국 시장에서 이미 경험하였고, 2010년대 Tik Tok이 보여 주었듯이) 물론 그 이후에 이를 구조화하고 글로벌 규모로 성장시키는 것은 (페이스북의 예에서 보았듯이) 미국 기업의 역할이 될 가능성이 크지만.

현재 AI 분야에서 미국과 가장 비슷한 수준으로 비교할 수 있는 곳이 중국이라고 본다. 아주 간단하게 요약하자면:

**LLM 시장:**

- (1T 이상 규모까지는 아니지만) 거의 모든 LLM 분야에서 최대 2-3개월 이내의 시차를 두고 미국과 비교할만한 수준의 LLM을 발표하고 있다. 1T 이하 규모의 SOTA/mid-market LLM, (o1에 필적하는) reasoning LLM, multi-modal LLM (이미지, 동영상), Code 생성 LLM 포함 모든 분야에서.
- (몇 가지 사족: SLM 분야에서는 미국 대비 상대적으로 activity가 적은 편으로 보이지만, 1T 규모의 LLM도 R&D 수준에서는 GPT-4보다 먼저 실험이 이루어졌지만 상용 출시는 하지 않았고, 가장 최근 1T 규모의 상용 LLM이 발표되기도 하였다)
- 중국의 Big Tech는 모두 자체 LLM을 갖추고, API, 챗봇, 기업용 생산성 툴 등 다양한 서비스를 제공하고 있다. 하지만, 그 범위는 대부분 Big Tech 사이에 비슷한 수준이며, 각 기업의 AI 매출 규모 및 기업 고객 수가 아주 많은 편인데 (예: Alibaba 고객 수: Qwen model 90,000, Dingtalk+Qwen 2.2m, Baidu 고객 수: Earnie bot: 200m, 기업 고객 수: 85,000) 추정으로는 대부분 기존 클라우드 기반 기업용 툴에 AI 기능을 추가한 후, 기존 고객을 모두 “AI 고객”으로 분류하고 있는 것이 아닌가 싶다.
- 그럼에도, 아래에 설명하듯이 중국 시장 특성에 맞는 아주 다양한 B2C, B2B AI app이 시도되고 있고, (각 회사가 주장하는 만큼은 아니어도) 몇 천만 내지 1-2억 규모의 상당히 많은 실 사용자가 있을 것으로 추정된다. (OpenAI 사용자 수에 비추어 볼 때)

**LLM 플레이어:**

- 중국 LLM 개발 회사는 크게 3가지로 구분된다. Big Tech, “AI Tiger”라 부르는 스타트업, “AI Little Dragon”이라 부르는 중견 규모 AI 회사

- Big Tech: Baidu, Alibaba, Tencent, Bytedance
- “AI Tiger”: [01.ai](https://substack.com/redirect/31d95788-1bde-4564-bf7d-eecbf396951f?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), Zhipu, Moonshot, Baichuan, MInimax, DeepSeek
- “AI Dragon”: SenseTime, Megvii, Yitu, CloudWalk
- Big Tech, 스타트업 모두 미국의 SOTA 수준과 비견할만 한 수준의 1T 이하 규모의 LLM을 자체 개발하였으며, reasoning model도 Alibaba Qwen/QwQ, DeepSeek V.2 r1, Zhipu GLM-Zero 등 o1 수준의 모델을 o1 대비 3개월 이내에 발표하는 수준이다.
- “AI Tiger”라 부르는 신생 AI 스타트업은, 대개 3억~10억 달러 규모의 펀딩을 받아서 자체 모델을 개발하고 있으며, 특이하게 DeepSeek은 외부 펀딩 없이 자체 펀딩으로 개발하고 있다.
- 주요 LLM 스타트업과 투자자

![](https://substackcdn.com/image/fetch/w_2000,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c65307c-3f40-46b5-b1b8-26867544a3e1_1000x1036.png)

**AI app:**

- 아주 다양한 현실적인 app 실험이 진행되고 있는 편이다. 전반적으로 아주 다양한, 특히 B2C 분야의 app이 등장하는데, 미국에서 등장하는 AI app들과는 아래에서 보듯이 약간 다른 양상을 보인다.
- B2C 분야: 커머스, 숏츠 제작 등 중국에서 활발한 분야. 뉴스 요약/분석 (참고: Zhipu의 reasoning model GLM-Zero-Preview에 대한 [Baidu 챗봇](https://substack.com/redirect/fadb2140-ab19-48ac-a0be-8982f828d7d5?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk), Baidu Apollo platform에 대한 [n.cn 뉴스 분석 서비스](https://substack.com/redirect/b19c423c-3439-467a-b26c-e0f29bfbf839?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)), WeChat mini-app + AI, AI 아바타
- B2B 분야: 개인 생산성 도구 (docs, 뉴스 분석 chatbot), 라이브커머스 + AI 챗봇
- 특이한 점은, AI 아바타 서비스가 특히 B2B 분야 (예: 라이브 커머스, 키오스크 등)에 많이 적용되어 실험되고 있다. (Gen AI 붐 직전인 [2020년 Microsoft China에서 spin-out한 Xiaoice (小冰)](https://substack.com/redirect/9dc705f4-673f-4e19-aa12-237b474065af?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)는 AI Avatar의 대표주자였다)
- 자연스럽게, 스마트폰에 AI Assistant를 내장하는 시도는 (미국보다 먼저) 다양하게 시도하고 있다

![](https://substackcdn.com/image/fetch/w_2000,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F783e66ab-0d05-4893-b231-514817c32810_1000x562.png)

**AI 규제:**

- (당연하게 예상할 수 있는 일이지만) AI 관련 중국 정부의 규제는 인터넷 시대의 컨텐츠 규제와 비슷한 규제를 적용 받는다. 즉, 중국 정부의 지침, 기준과 다른 컨텐츠 생성이 금지되어 있다.
- 중국에서 게임 서비스를 출시하려면 ‘판호’를 받아야 하는 것과 비슷하게, LLM 서비스를 출시하려면 별도의 ‘판호’를 받아야 하며, [2024년6월 기준 40개의 LLM이 판호를 받았고 240개 LLM의 판호가 심사 중](https://substack.com/redirect/549b9462-127f-4a10-8937-43111aa9317b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)이다.

**중국 AI 시장에 대한 전반적인 평가:**

- LLM 측면에서는 유일하게 미국과 비견할만한 경쟁력을 가지고 있지만, 미국을 앞서는 수준은 아니고 앞으로도 미국을 앞서는 수준이 되지는 않을 것으로 예상된다.
- B2C, B2B에서 다양한 (미국과도 다른) app/서비스를 시도하고 있지만, 대부분 기존 서비스에 AI를 접목하여 효율화 맟 새로운 방식 서비스의 시도 (예: AI 아바타)
- (과거 인터넷 & 모바일 시대에 그랬듯이) 이 기반으로 중국 환경의 독특한 앱/서비스 (예: WeChat mini-app, Tik Tok, 라이브 커머스 등)이 보편화될 가능성이 높지만, multi-agent와 같이 패러다임 자체를 바꾸는 수준의 새로운 방식이 중국에서 만들어지지는 않을 것으로 보인다.
- 다만, Consumer AI 서비스의 다양한 시도는 미국에서보다 중국에서 훨씬 빠르게 다양하게 이루어질 것으로 예상되기 때문에, Consumer AI 서비스에 대한 실험은 (미국보다) 중국 시장을 관찰하는 것이 효과가 더 높을 것으로 보인다.

아직까지는 이 이상의 자세한, 깊이있는 자료에 대한 접근이 어려워서 더 깊은 수준의 시장 흐름의 분석을 하지는 못 하였다.

중국 AI 시장 현황을 개괄해 볼 수 있는 몇 가지 자료:

[2024 China Generative AI LLM Application Ecosystem Research Report - QuestMobile](https://substack.com/redirect/917a8017-7d30-4525-b484-8278c4e39f81?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[Decoding China's Top Ten Generative AI Models: Established Tech Old Guards Lead the Charge in the GenAI Era – China Money Network](https://substack.com/redirect/d8372b20-e7b9-4468-b3f1-82df030bfd13?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

[China’s Generative AI Ecosystem in 2024: Rising Investment and Expectations | The National Bureau of Asian Research (NBR)](https://substack.com/redirect/549b9462-127f-4a10-8937-43111aa9317b?j=eyJ1IjoieWVjNWwifQ.BuyEaNo4bPEgcgbZRIYdrDQ5FEDVTd65ZzHO1r3cmZk)

한국 시장에 대해서는 이미 국내 플레이어에 대한 정보가 많기 때문에, 그 내용을 자세하게 설명하기 보다는 개략적인 시장 흐름에 대한 assessment를 요약하는 수준으로 정리한다.

**몇 가지 관찰:**

- 사용자 수, 매출 측면에서 주목할만한 플레이어가 몇몇 등장: 업스테이지 (기업용 RAG 플레이어), 뤼튼, 라이너 (개인 생산성 툴)
- 국내 Big Tech에서 나와 창업한 회사가 몇 있으나, 아직 시장에 결과가 나오지는 않은 상태: Open Research, 숨빗AI (Kakao), TrillionLabs (Naver)
- 3-5년 전 (소위 Gen AI 직전 시대) 창업한 AI 스타트업이 몇몇 있음. 이 중 아주 성공적으로 Gen AI 흐름에 적응한 경우도 있고 (스캐터랩 등), (아마 같은 기술 기반으로) 빠르게 기업 대상 비즈니스를 만들면서 성장하는 곳도 있고 (리턴제로 등), 바뀐 Gen AI 환경에 적응하고 있는 곳도 다수 있음
- 그 외에는, 2024년에 새로 창업한 시드 단계 AI 스타트업이 대략 50-100개 정도 되는 것으로 추정됨
- 기존 스타트업 중 Gen AI를 적극 도입하면서 사업 전략을 빠르게 수정하는 회사도 다수 있는데 (매스프레소 등) 그 전환 결과는 좀 더 지켜 보아야 할 듯

**LLM & AI app:**

- 아직 네이버 CLOVA가 API 기준으로는 public 공개되지 않았고, 몇 개의 fine-tuned 모델 (LG ExaOne, 업스테이지 Solar), 개발 중인 모델 (KT, Moreh, TrillionLabs 등)이 있는데,
- AI app/서비스 개발하는 회사가 이용할 수 있는 한글 기능이 충분히 강화된 LLM는 아주 제한된 편임
- RAG 기반 기업용 AI app을 위해서는 대부분 미국, 중국의 SOTA, mid-sized 오픈소스 LLM을 이용하고 있는데, RAG app 수준에서는 (약간 참고) 쓸 수 있는 수준이 되는 것으로 보임
- 하지만, 일반 개인 생산성 툴, 내지 B2C 서비스 용으로는 충분한 수준이 되지 못한다고 판단됨. 이 것이 아주 다양한 B2C 서비스, 개인 생산성 툴이 등장하는데 상당한 제약이 된다고 봄
- 기업 대상 AI-powered SaaS 서비스가 등장하기 시작하였지만, 아직은 기존 SaaS 툴에 AI를 접목하여 더 효율화, (텍스트 요약 등의) 기본 기능을 접목한 기초적인 수준으로 보이며 (”AI-ification of SaaS”), (워크플로우 + AI, “Services as software” 등의) 그 다음 단계로 진화하지는 못하고 있다고 판단됨
- 하지만, 웹툰 제작, 게임 개발 툴로서의 활용, 단순한 고객 지원 챗봇 수준의 기업 활용은 예상보다 빠르게 확산 되고 있음. 이로 인한 내부 인력 축소가 가시적으로 보일 정도.
- 한국 환경에 특화된 분야에서 새로운 AI 스타트업이 등장하기 시작한 것은 고무적: 웹툰, 3D, robotics, (교육?)
- 그럼에도, 미국, 중국 등의 시장과 비교하면, 국내 AI 스타트업 시장은 “아직 너무 적은 수의 AI 스타트업”, “너무 단순한 유형의/적은 수의 AI app/서비스”라고 요약할 수 있을 듯

현재 HRZ에서 집중하고 있는 AI thesis 키워드:

- AI Picks and Shovels
- Vertical (agentic) AI
- AI for Creatives
- Hard problems in real world — robotics
- AI + 게임/소셜/컨텐츠/엔터테인먼트
- Next-gen Agents (long-shot)

이 AI thesis 키워드는 주기적으로 내부 리뷰를 통하여 지속적으로 수정하고 있으며, 그 내용에 대해서 다음 글에서 좀 더 자세히 설명해 보려고 한다.

이러한 생각들이 새로운 기회를 열심히 찾고 있는 창업자들에게 조금이라도 도움이 되기를 기대한다.

Bon Voyage!