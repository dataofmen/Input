LGD 분석 syntax

* A1_4_E : 이전 TV 화면 사이즈
* A2_E : 최근 1년 화면 사이즈

** 인치대별로 리코딩: 40~49 -> 4, 50~59 ->5, 60~64 -> 6, 65이상 -> 7

RECODE A1_4_E A2_E (Lowest thru 49=4) (50 thru 59=5) (60 thru 64=6) (65 thru Highest=7) INTO 
    A1_4_E_ca A2_E_ca. 
VARIABLE LABELS  A1_4_E_ca '이전 TV 사이즈 range' /A2_E_ca '보유 TV 사이즈 range'. 
EXECUTE. 


** 이전 TV 사이즈와 현재 TV 사이즈 교차분석

CROSSTABS 
  /TABLES=A1_4_E_ca BY A2_E_ca 
  /FORMAT=AVALUE TABLES 
  /CELLS=COUNT 
  /COUNT ROUND CELL.


CROSSTABS 
  /TABLES=A1_4_E_ca BY A2_E_ca 
  /FORMAT=AVALUE TABLES 
  /CELLS=ROW 
  /COUNT ROUND CELL.


********************* 8K 인지도와 선호도 비교

CROSSTABS 
  /TABLES=OT6_1 OT6_2 BY OT6 
  /FORMAT=AVALUE TABLES 
  /CELLS=COUNT 
  /COUNT ROUND CELL.