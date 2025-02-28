---
doc_type: hypothesis-highlights
url: 'https://medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433'
---

# 마이리얼트립 웹사이트 성능 측정 및 최적화 Part 1. 리소스 로딩

## Metadata
- Author: [medium.com]()
- Title: 마이리얼트립 웹사이트 성능 측정 및 최적화 Part 1. 리소스 로딩
- Reference: https://medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433
- Category: #article

## Page Notes
## Highlights
- 하지만 여행에 대한 부푼 마음을 갖고 방문한 페이지의 로딩이 답답할 정도로 느리다면 어떤 기분이 들까요? 관광 명소에 입장하기 위해 예약 내역 페이지를 확인하는데 몇십초가 걸린다면 어떨까요? 상품 상세 정보를 보려고 페이지를 내릴 때 스크롤이 버벅인다면 어떨까요? — [Updated on 2021-05-25 19:26:23](https://hyp.is/p30zFL1DEeu8FtfY_nph5A/medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433) — Group: #Public

- 마이리얼트립 이용 시 속도 면에서 가장 답답함을 느낄 여행자 환경은 어떤 것일까요? 아래와 같은 항목들이 떠올랐습니다.모바일, 해외 로밍 (제한된 네트워크 대역폭)최초 방문자 (브라우저나 서버의 캐시를 제공받을 수 없는 환경)즉, 여행지에서 해외 로밍을 이용 중이고, 모바일로 웹페이지에 처음 접속하는 여행자가 됩니다. — [Updated on 2021-05-25 19:27:14](https://hyp.is/xjTaMr1DEeupNz8ijhLgBw/medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433) — Group: #Public

- 콘텐츠가 눈에 보이지만 클릭이 되지 않거나 스크롤이 더디게 움직이는 경험이 한번쯤은 있으실텐데요. 이는 브라우저의 상호 작용이 원활하지 않음을 뜻하고, 아직 TTI(Time to Interactive)에 이르지 못한 상태를 말합니다. 이 상태가 길어진다면 여행자의 체감 속도도 비례하여 떨어질 것입니다. — [Updated on 2021-05-25 19:27:29](https://hyp.is/zrmk-L1DEeu2No-cpxYGwg/medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433) — Group: #Public

- 콘텐츠의 우선 순위 (Hero element) — [Updated on 2021-05-25 19:27:45](https://hyp.is/2KRTeL1DEeu6Mv9uwbrkgw/medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433) — Group: #Public

- Javascript: 가장 먼저 Part 1의 데모와 같이 자바스크립트로 스타일을 변경하는 구문이 있는지 확인한 뒤 해당되는 DOM 요소에 CSS class 또는 inline 스타일로 반영합니다.Style: 현재 버전의 CSS를 어떤 DOM 요소에 적용해야 할지 계산합니다.Layout: 각 요소의 너비나 위치를 갱신에 화면 상에 배치합니다.Paint: 각 요소에 배경색, 글자 색과 같이 픽셀을 채우는 과정입니다.Composite: 이전 과정에서 생성된 레이어를 병합합니다. — [Updated on 2021-05-25 19:32:35](https://hyp.is/hSEzMr1EEeupOP8xhxiRqQ/medium.com/myrealtrip-product/fe-website-perf-part1-6ae5b10e3433) — Group: #Public



