---
title: "Deepseek V3와 엔비디아 코스모스: 합성 데이터의 위력"
source: "https://thecore.media/deepseeknvidiacosmos/"
author:
  - "[[강정수]]"
published: 2025-01-12
created: 2025-01-13
description: "오늘 글을 시작하면서 베단트 미스라(Vedant Misra)의 1월 7일 X 포스트를 소개합니다. 베단트 미스라는 OpenAI에서 일했었고 현재 DeepMind에서 AI 연구자로 활동하고 있습니다. 샘 알트만(Sam Altman)는 1월 6일 자신의 블로그에서 “AGI를 구축하는 방법을 알고 있다고 확신”한다고 주장합니다. 이 블로그 포스트에 대해 베단트 미스라는 아래와 같이 코멘트하고 있습니다."
tags:
  - "clippings"
---
오늘 글을 시작하면서 베단트 미스라(Vedant Misra)의 [1월 7일 X 포스트](https://x.com/vedantmisra/status/1876327518157807990)를 소개합니다. 베단트 미스라는 OpenAI에서 일했었고 현재 DeepMind에서 AI 연구자로 활동하고 있습니다. 샘 알트만(Sam Altman)는 [1월 6일 자신의 블로그](https://blog.samaltman.com/reflections)에서 “AGI를 구축하는 방법을 알고 있다고 확신”한다고 주장합니다. 이 블로그 포스트에 대해 베단트 미스라는 아래와 같이 코멘트하고 있습니다.

“앞으로 다가올 미래를 본능적으로 이해하는 사람은 전 세계에 수백 명에 불과합니다. 그들 대부분은 딥마인드, 오픈AI, 안트로픽, x.AI에 있지만 일부는 외부에 있습니다. 미래를 이해하기 위해서는 다음의 개별 효과가 만들어 낼 수 있는 총체적 효과를 이해할 수 있어야 합니다: ① 빠른 알고리즘 개선, ② 반복적인 자기 개선을 맡고 있는 강화학습(RL)에 대한 공격적인 투자, ③ 그리고 이미 데이터센터 건설에 투입된 수백억 달러! **우리 모두 틀렸거나 아니면 모든 것이 곧 바뀔 겁니다**.  
(There are maybe a few hundred people in the world who viscerally understand what's coming. Most are at DeepMind / OpenAI / Anthropic / X but some are on the outside. You have to be able to forecast the aggregate effect of rapid algorithmic improvement, aggressive investment in building RL environments for iterative self-improvement, and many tens of billions already committed to building data centers. **Either we're all wrong, or everything is about to change**.)”

“우리 모두가 틀렸거나 아니면 모든 것이 곧 바뀔 겁니다!” 멋진 표현입니다. The Core에서는 2024년 AI 거품에 대한 다양한 의견을 소개했습니다. 그러나 저는 이 논쟁이 타당하다고 생각하지 않습니다. 우리는 매우 강력한 기술이 전속력으로 개발되고 있고 동시에 차별화되고 있으며 동시에 가장 낮은 수준의 AI 모델에서도 큰 도약이 계속되고 있는 현실을 목격하고 있습니다.

곳곳에서 AI가 이야기되다보니, 이제 AI 주제에 짜증이 나는 분도 계실 겁니다. 진심으로 이해합니다. 그러나 AI 주제는 우리 시대의 가장 큰 기술 진보에 대한 것입니다. 인터넷보다 더 큰 규모입니다. 인터넷과 데이터는 어쩌면 인공지능의 첫 번째 발전 단계를 위한 전제 조건일 뿐이었습니다. 인터넷은 콘텐츠, 재화 및 서비스 유통을 디지털화했습니다. 이제 AI는 거의 모든 것을 단계적으로 디지털화할 것입니다. AI 혁신은 이제 시작일 뿐입니다.

- OpenAI의 o1과 o3는 추론 시간에 엄청난 잠재력이 있다는 것을 보여주고 있습니다.
- AI 기술 역량이 생성 AI에서 AI 에이전트로 천천히 이동하고 있으며, AI 에이전트는 업무 자율성의 증가를 의미합니다(참조: [AI 에이전트 시대, 경제의 주인이 바뀐다](https://product.kyobobook.co.kr/detail/S000214736966)).
- 컴퓨팅 및 데이터센터에 대한 투자는 기록적인 속도로 확장되고 있습니다. 2025년 [마이크로소프트는 AI 관련 데이터센터에 800억 달러를 투자](https://www.cnbc.com/2025/01/03/microsoft-expects-to-spend-80-billion-on-ai-data-centers-in-fy-2025.html)할 계획입니다.
- 엔비디아는 월드 모델에 진심입니다. 과도한 자신감과 야망으로 인해 결국 파멸을 초래하는 현상인 이카로스 증후군(Icarus Syndrome)이 떠오릅니다. 그러나 엔비디아는 태양과 바다 사이에서 적절한 거리를 유지하며 크레타섬을 탈출할 수도 있습니다. 이 때 세상은 자율주행과 로봇 산업에서 큰 변화를 경험하게 될 것입니다. 월드 모델에 대해서는 지난 글 [AI 브라우저, 웹과 앱의 새로운 권력 투쟁](https://thecore.media/aibrowser/)을 참조하세요.
- 이번 글의 주제는 Deepseek와 엔비디아 코스모스에 사용된 '합성 데이터'입니다. Deepseek는 AI의 테무(Temu)입니다. 아래에서 그 이유를 설명하겠습니다.

Deepkeek에서 우리가 배워야할 점이 무엇인지를 설명하기에 앞서 한국 기업에게 하고 싶은 말이 있습니다. 자체 AI 모델 개발에 투자하는데 더욱 신중해야 합니다. 보다 나은 AI 모델이 ‘기성품’으로 진화하고 있습니다. GPT, 제미나이, 클로드, 라마 등 프론티어 모델, 미세 조정(fine tuning) 및 추가 커스터마이징 그리고 RAG에 집중하는 것으로도 충분합니다. 현재 AI 모델 생태계에서 1년은 영원과 같습니다. 우리가 ChatGPT 순간을 경험하기 시작한지도 이미 2년이 넘었습니다. 기업이 자체 서비스 로드맵과 전략을 세울 때 AI 모델이 오늘 할 수 없는 일을 내일 할 수 있다는 명제를 중심에 두어야 합니다. 그 때 우리 기업의 부가가치는 어떻게 될 것인지 지금부터 고려해야 합니다.

### Deekseek: AI 세계의 테무(Temu)

중국의 새로운 AI 모델 Deekseek V3는 AI 개발의 전환점이 될 것입니다. 품질 면에서 GPT-4와 경쟁하지만 이용 가격은 훨씬 저렴합니다. 또한 Deekseek는 제한된 자원으로도 강력한 AI 모델이 가능하다는 것을 보여주고 있습니다.

아래 그림에서 확인할 수 있는 것처럼 Deekseek V3는 비교 테스트에서 OpenAI의 주력 제품인 GPT-4o보다 나은 품질을 달성하고 있습니다.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXelm1hxOk_e9RyQox_bxn-7NdzlcBXk9QDd_TjOmFndaBkzcOWtXaSG_kYFHzpJqpbawr9O4utq8QeFBLKT8FyLSrCSxfR7ExoAbQXNan6vxDPCnhejPQo_TWYCFUNzmmUC1V5qoA?key=Mr1tFaOBXiH_28b8rkm2A7XO)

출처: [wandb.ai](https://wandb.ai/byyoung3/ml-news/reports/DeepSeek-V3-Training-671-Billion-Parameters-with-a-6-Million-dollar-Budget--VmlldzoxMDczNTI2Ng)

그런데 Deekseek V3의 파라미터의 수는 6,710억 개에 불과하며 모델 훈련 비용에는 600만 달러가 투자되었을 뿐입니다.

![](https://cdn.wandb.ai/production/9b16c7dc3/favicon.png)

Deekseek 모델을 제작한 곳은 2023년 5월에 설립된 Deekseek라는 중국 기업입니다. 이 Deekseek라는 신생 기업을 소유한 곳은 2015년 중국 절강대학교 출신 엔지니어 3명이 설립한 [High-Flyer Capital Management](https://www.highflyercapital.com/)라는 헤지펀드 기업입니다. [High-Flyer 설명](https://www.high-flyer.cn/en/fund/)에 따르면, 이 헤지펀드는 머신러닝과 딥러닝 기술을 사용하여 투자 전략을 운영합니다. 현재 약 80억 달러의 자산을 관리하고 있습니다. High-Flyer는 이 자산을 더 효과적으로 관리하기 위해 2021년 엔비디아 A100 GPU 10,000개 이상으로 구성된 데이터센터를 건설합니다. 여기에 든 비용은 1억 3,700만 달러입니다. 다시말해 High-Flyer는 헤지펀드 기업이자 동시에 AI 기업입니다. Deepseek 모델 학습이 이 데이터센터가 활용되었을 것으로 추측할 수 있습니다.

엔비디아 A100 GPU는 2020년 출시된 제품이지만 2022년 출시된 H100과 비교하면 AI 모델 학습 속도는 6배가 느립니다. High-Flyer는 엔비디아 H800 GPU를 2,048개를 Deepseek에 공급하여 모델 Deepseek V3 학습을 지원했다고 합니다. 다시말해 미국 OpenAI, 구글, 앤트로픽의 경쟁 모델과 비교하면 Deepseek V3의 학습 컴퓨팅 자원은 형편없는 수준입니다. The Core의 2024년 10월 ‘[중국 생성 AI, 위기를 기회로 바꾸다](https://thecore.media/aibriefing241006/)’에서 소개한 것처럼, 중국 AI 연구자들은 미국 행정부의 수출 금지 조치로 인해 하이엔드 칩에 대한 접근이 제한되면서 실리콘벨리 경쟁자보다 더 효율적인 컴퓨팅 운영 능력을 갖추게 되었습니다. 그 결과, 훨씬 더 작은 학습 비용으로 훨씬 더 저렴한 가격의 거대언어모델을 출시한 것입니다.

여기서 주목할 것은 Deepseek V3은 전문가 혼합(MoE) 방법을 사용하고 있다는 점입니다. MoE 기반 모델은, 모든 질문에 전체 AI 모델이 작동하면서 답변을 생성하지 않습니다. 예를 들면 MoE에서는 모든 질문에 모든 전문가가 답변을 함께 작성하는 것이 아니라 관리자-이를 라우터라 부릅니다-가 개별 질문을 각각 관련 전문가에게 전달하여 답변을 생성하게 합니다. 이는 모든 전문가를 계속 바쁘게 하는 것보다 효율적일 뿐 아니라 비용도 절감할 수 있습니다. 이것이 전문가 혼합(Mixture of Experts: MoE)의 큰 장점입니다. [공개된 관련 논문](https://arxiv.org/abs/2412.19437)에 따르면, Deepseek V3 모델 학습에 들어간 비용은 550만 달러에 불과합니다. 비교하면, 엔트로픽 대표 다리오 아모데이(Dario Amodei)는 2024년 8월 [다음 AI 모델 학습에 최대 10억 달러, 그리고 그 다음에는 100억 달러가 필요](https://www.businessinsider.com/anthropic-ceo-cost-10-billion-train-ai-years-language-model-2024-4)할 수 있다고 말하고 있습니다. Deepseek는 학습 비용이 저렴한 그러나 강력한 MoE 모델이 충분히 가능하다는 것을 입증하고 있습니다. AI 전문가 안드레이 카르파티(Andrej Karpathy)는 미국에서 Deepseek V3 수준의 모델을 만드는데 필요한 GPU 수는 16,000개라고 평가하면서 Deepseek V3가 단지 2,048개로 이러한 성과를 낸 것에 [놀라움을 표현](https://x.com/karpathy/status/1872362712958906460)하고 있습니다.

### 합성 데이터의 중요성 증대

제가 최근에 읽은 글 중 매우 훌륭한 글은 [Scaling Laws – O1 Pro Architecture, Reasoning Training Infrastructure, Orion and Claude 3.5 Opus “Failures”](https://semianalysis.com/2024/12/11/scaling-laws-o1-pro-architecture-reasoning-training-infrastructure-orion-and-claude-3-5-opus-failures/)입니다. 이 글의 요지는 다음 기회에 소개하겠습니다. 이 글에서 발견한 놀라운 점은 Deepseek V3에 학습 데이터에서 이용한 것은 OpenAI의 GPT-4o가 생성한 합성 데이터(synthetic data)라는 점입니다.

- Deepseek만 합성 데이터로 학습한 것이 아닙니다. 물론 이것이 사실이라면 Deepseek는 OpenAI의 이용 약관을 위반한 것입니다.
- 앤트로픽은 클로드 3.5 오푸스를 서비스로 제공하지 않습니다. 클로드 3.5 오푸스가 생성하는 합성 데이터는 클로드 3.5 소네트를 개선하는데 학습 데이터로 사용되었습니다.
- 엔비디아의 월드모델 코스모스도 합성 데이터로 학습한 모델입니다.

![](https://i0.wp.com/semianalysis.com/wp-content/uploads/2024/11/cropped-Logo2-02-1.png?fit=192%2C192&ssl=1)

합성 데이터로 AI 모델 학습하는 것에 대한 비판이 많습니다. 합스부르크 질병(Habsburg Disease)에 대한 우려때문입니다. 중세 유럽의 합스부르크 가문은 가까운 혈족 간의 혼인을 반복한 결과 유전적 질병이 축적되었습니다. 그러나 AI 모델 학습에서 이러한 현상은 아직 증명되지 않고 있습니다. 오히려 반대 현상이 발생하고 있습니다. 더 나은 AI 모델은 질적으로 더 높은 품질의 합성 데이터를 생성하기 때문에 더 나은 AI 모델을 만들 수 있습니다. 이른바 데이터 네트워크 효과가 발생하고 있습니다. AI 연구진은 합성 데이터의 사용에서 더 나은 모델을 더 빨리 개발하는 데 도움이 [되는 여러가지 작은 확장 법칙을 발견](https://semianalysis.com/2024/12/11/scaling-laws-o1-pro-architecture-reasoning-training-infrastructure-orion-and-claude-3-5-opus-failures/)했기 때문입니다. 이로써 AI 모델 학습에서 데이터 병목 현상이 해결되고 있습니다. 거대언어모델은 최고 수준의 합성 데이터를 효과적으로 생성하여 다른 모델을 학습시키는데 사용될 수 있습니다. 대형 모델은 교수진이고 학습할 모델은 학생입니다.

Deepseek V3처럼 합성 데이터로 학습한 모델이 엔비디아가 공개한 코스모스입니다. 코스모스는 인류 역사상 가장 큰 산업인 휴머노이드 로봇의 기초 지능이 되고자 합니다. 이렇게 2025년 새로운 AI 경제가 시작되고 있습니다.

오래된 노래로 이 글을 맺으려 합니다. 1970년 발표된 카펜터스(The Carpenters)의 곡 중에 "We've Only Just Begun"라는 곡이 있습니다.

![](https://www.youtube.com/watch?v=__VQX2Xn7tI)

아래는 가사 중 일부입니다.

Before the rising sun, we fly  
So many roads to choose  
We‘ll start out walking and learn to run  
And yes, we've just begun  
떠오르는 태양이 뜨기 전에 우리는 날아  
선택해야 할 길이 너무 많아  
우리는 걷기 시작하고 달리는 법을 배울거야  
그래, 우리는 이제 막 시작했어