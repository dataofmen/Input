[R] 네트워크분석 - 근접 중심성

# 근접 중심성
# 각 노드 간의 거리를 근거로 중심성을 측정하는 방법으로, 직접적으로 연결된 노드뿐 아니라
# 간접적으로 연결된 모든 노드 간의 거리를 합산해 중심성을 측정
# ex : A는 집단의 모든 사람을 알지는 못하지만 A가 아는 사람들을 거쳐서 가면 모든 사람을 알 수 있다.
#      이때 가장 짧은 경로로 모든 사람을 알게 되는 것이 근접 중심성
clo<-closeness(g)  # 근접중심성
clo.score<-round((clo-min(clo))*length(clo)/max(clo))+1  
# clo를 실행해보면, 소수이기 때문에, 자연수로 점수를 주었습니다. ( 1을 더하는 이유는 min 근접중심성은 0이 되기때
# 문에, 자연수로 만들어 주기 위해)
clo.colors<-rev(heat.colors(max(clo.score)))
# heat.colors는 따뜻한 색으로 n개 변환 ( 옅은색 -> 진한색 순서)
# rev는 벡터의 순서를 거꾸로(reverse) 해줌 : 중심성이 높을수록 진한색으로 할당
V(g)$color<-clo.colors[clo.score]
plot(g)
