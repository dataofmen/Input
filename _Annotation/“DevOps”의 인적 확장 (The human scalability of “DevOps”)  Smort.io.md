---
doc_type: hypothesis-highlights
url: >-
  https://www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops
---

# “DevOps”의 인적 확장 (The human scalability of “DevOps”) | Smort.io

## Metadata
- Author: [smort.io]()
- Title: “DevOps”의 인적 확장 (The human scalability of “DevOps”) | Smort.io
- Reference: https://www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops
- Category: #article

## Page Notes
## Highlights
- 최근 트위터에 썼듯, 저는 요즘 꽤 많은 시간을 들여 “DevOps”의 인적 확장(human scalability)에 대해 생각하고 있습니다. (“DevOps”에다가 따옴표를 붙인 건, 이에 대해 추후 서술할 다양한 정의가 있기 때문입니다.) 그렇게 내려본 결론은, DevOps는 작은 엔지니어링 조직들에서 굉장히 잘 돌아갈 수도 있지만, 신중한 생각과 관리 없이는 큰 인적/조직적 확장(scaling) 문제를 일으킨다는 것입니다. — [Updated on 2022-06-29 14:01:42](https://hyp.is/kRe5DvdoEeyVDkNfTFXwwQ/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- DevOps는 개발자가 프로덕션 환경에서 24시간 365일 서비스가 운영되도록 책임지게 하는 방법(practice)이다. 이것은 공용 인프라 기반기술을 사용한 개발, 테스팅, 상시 장애대응, 신뢰성 엔지니어링(reliability engineering), 장애 복구, SLO 정의, 모니터링 셋업 및 알람 설정, 디버깅 및 성능 분석, 장애 근본 원인 분석(root cause analysis), 프로비저닝 및 배포 등을 포함한다. — [Updated on 2022-06-29 14:02:29](https://hyp.is/rWU-nPdoEeyTSavANKdAtw/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 그 대신, 이러한 엔지니어링 조직이 갖는 당면 과제는 ‘비즈니스 성장, 개인의 성장 및 (비즈니스/채용에 대한) 경쟁 등에 대한 극심한 압박과 시스템 신뢰성(reliability) 간의 균형을 어떻게 맞추는가’ 입니다. 이 글의 이후 부분은 저의 개인적 경험에 근거한 것으로, 맞지 않는 경우가 있을 수 있고, 특히 분기마다 한 번씩 monolithic 소프트웨어를 배포하는 천천히 움직이는 회사들이나 더 빠르고 애자일한 개발 방법을 도입하고자 하는 회사같은 경우엔 맞지 않을 수 있습니다. — [Updated on 2022-06-29 14:03:14](https://hyp.is/x_0GIvdoEeyjFIuG5ptpUQ/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 저는 개발자들이 자신이 작성한 코드에 대해 책임을 지고 장애대응을 할 때 그 시스템의 퀄리티가 향상된다고 굳게 믿는 사람입니다. 누구도 장애로 호출 받는 걸 좋아하진 않지만, 이런 피드백 루프는 더 나은 제품을 만들어냅니다. 또한 1번에서도 설명했듯 보통 초기 스타트업에서 일하는 것에 매력을 느끼는 엔지니어는 배우는 것과 운영 업무를 하는 걸 꺼리지 않는 사람들입니다. 특히 제품 신뢰성이 낮아도 큰 영향을 받지 않는 초기 스타트업의 경우에는 이런 경향이 더욱 두드러지게 나타납니다. 초기 스타트업의 경우에는 제품이 적절한 시장을 찾아 급성장할 수 있는 국면에 진입할 정도만 제품의 신뢰성이 있어도 충분하기 때문입니다. — [Updated on 2022-06-29 14:05:18](https://hyp.is/EdZTcPdpEey7qnc9fGnm9g/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 인력 증가 속도가 빠르게 늘어나며, 커뮤니케이션과 엔지니어링 효율에 심각한 부담이 오기 시작합니다. 이 주제에 대해서는 맨먼스 미신(The Mythical Man-Month) 을 꼭 읽어보길 권합니다. (거의 50여년 전 책인데도 여전히 아주 좋은 책입니다.) — [Updated on 2022-06-29 14:05:55](https://hyp.is/KDOoFvdpEeyr7gsQuEYLmQ/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- Monolithic 아키텍처에서 microservice 아키텍처로의 전환은 시스템 인프라 복잡성을 몇 배나 증가시킵니다. 네트워킹, 시스템 가시성, 배포, 라이브러리 관리, 보안 등 이전에는 그리 어렵지 않았던 수백가지 문제가 불거지고, 해결해야 할 주요 문제가 됩니다. — [Updated on 2022-06-29 14:06:12](https://hyp.is/MizrNPdpEey66WsAuhEPEA/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 동시에, 급성장으로 인해 트래픽이 증가하고 그로 인한 기술적인 확장 문제를 겪게 되며, 완전한 실패(complete failure)와 작은 사용자 경험 문제들이 생기기 시작, 점점 큰 사용자 영향이 나타납니다. — [Updated on 2022-06-29 14:06:23](https://hyp.is/OLNZcPdpEeyc1gfRPXRslg/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 공통적으로 나타나는 구조는 중앙 인프라 팀을 만들어, DevOps랑 비슷한 일을 하고 있는 다양한 제품 팀을 지원하는 구조입니다. — [Updated on 2022-07-01 09:56:29](https://hyp.is/pBXnCPjYEeymy2dnSEnLlw/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 최신의 클라우드 네이티브 기술들을 사용하긴 너무 어렵기 때문입니다. — [Updated on 2022-07-01 09:57:09](https://hyp.is/vD37mvjYEey2k9dxZgnVGw/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 클라우드 네이티브 인프라 기반기술들이 제공해주는 것 너머의 이런 대규모 엔지니어링 조직들이 갖고 있는 문제들을 해결하기 위해 중앙 인프라 팀이 탄생 — [Updated on 2022-07-01 09:57:50](https://hyp.is/1J10XvjYEeykOyPOJT74FA/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public

- 어플리케이션/제품 개발자가 비즈니스 로직에 집중할 수 있도록 가능한 많은 인프라들을 추상화하기 위함 — [Updated on 2022-07-01 09:58:09](https://hyp.is/4CtmyPjYEeymzJu4S51Ggw/www.smort.io/article?url=https:/tech.devsisters.com/posts/the-human-scalability-of-devops) — Group: #Public



