[[ReadItLater]] [[Article]]

# [DataJourney - Design-First 오픈소스 데이터 관리 툴킷](https://news.hada.io/topic?id=18431)

-   조직이 데이터를 효과적으로 관리하고 활용할 수 있도록 오픈소스 기술의 강점을 활용하는 구조화된 접근법 제공
-   **확장 가능성**과 **재현 가능성**을 중시하며, 데이터 워크플로우를 구축하는 데 필요한 필수 단계를 안내
-   목표 설정, 도구 선택, 워크플로우 테스트 및 커스터마이징 과정을 포함한 체계적 지원
-   유연하고 모듈화된 설계를 통해 사용자 요구에 맞게 조정 가능

## 디자인 철학 : 레이어 구성

1.  **PO (기반)**: GitHub과 같은 정적 홈 역할
2.  **P1 (도구)**: 오픈소스로 구동되는 각종 도구들
3.  **P2 (유지보수 및 모니터링)**: 환경 및 자동화 관리 (Pixi 및 GHA)
4.  **P3 (추상화)**: 사용자 상호작용을 위한 CLI/작업 관리자 레이어 (Pixi)

## 현재 지원 워크플로우

-   **Python 패키징 프레임워크** 설계 원칙 구현
-   **GitHub Actions** 설정
-   **Vale.sh** PR 수준에서 구성
-   **Pre-commit hooks**로 코드 린팅/포맷팅 설정
-   [Pixi](https://prefix.dev/)를 활용한 환경 관리
-   [Intake](https://github.com/intake/intake)를 이용한 온라인 데이터 소스 읽기
-   [Dagster](https://github.com/dagster-io/dagster)를 이용한 샘플 파이프라인 구축
-   [Holoviews](https://holoviews.org/gallery/index.html) + [Panel](https://panel.holoviz.org/reference/index.html)을 사용한 대시보드 구축
-   [Mito](https://www.trymito.io/)를 활용한 탐색적 데이터 분석(EDA)
-   [Flask](https://flask.palletsprojects.com/en/3.0.x/) 기반 웹 UI 빌드
-   [FastHTML](https://docs.fastht.ml/)로 웹 UI 확장 및 재구성
-   GitHub AI 모델을 활용하여 데이터 분석 수행 ([GitHub AI models Beta](https://docs.github.com/en/github-models/prototyping-with-ai-models))