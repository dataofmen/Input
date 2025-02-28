

항상 발생하는 사태는 아니고, 가끔씩 spss 한글 데이터를 못 불러오는 경우들이 생기는데, 



abc <- read.spss(file="내 SPSS sav 데이터의 경로", reencode='utf-8', use.value.label=FALSE, to.data.frame=TRUE)

abc <- read.spss(file="D:/User_Data/Desktop/2019_5_merge.sav", reencode='utf-8', use.value.label=FALSE, to.data.frame=TRUE)


출처: https://rzummas.tistory.com/2 [알줌마의 R초보탐험]