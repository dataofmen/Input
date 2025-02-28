# SPSS Syntax - LGD TV 사이즈 범위


** TV 사이즈 변수 생
RECODE GCA3_D GCA3_1 (Lowest thru 25.9=1) (26 thru 29.9=2) (30 thru 35.9=3) (36 thru 39.9=4) (40 
    thru 45.9=5) (46 thru 49.9=6)(50 thru 52.9=7) (53 thru 55.9=8) (56 thru 60.9=9) (61 thru 65.9=10) (66 thru 75.9=11) 
    (76 thru 79.9=12) (80 thru Highest=13) INTO GCA3_D_ca GCA3_1_ca. 
VARIABLE LABELS  GCA3_D_ca 'TV구매의향 사이즈_ca' /GCA3_1_ca '가격 미고려 구매의향 사이즈'. 
EXECUTE. 



** 미국 TV % 테이블
USE ALL. 
COMPUTE filter_$=(COUNTRY = 1). 
VARIABLE LABELS filter_$ 'COUNTRY = 1 (FILTER)'. 
VALUE LABELS filter_$ 0 'Not Selected' 1 'Selected'. 
FORMATS filter_$ (f1.0). 
FILTER BY filter_$. 
EXECUTE. 
CROSSTABS 
  /TABLES=GCA3_D_ca BY GCA3_1_ca 
  /FORMAT=AVALUE TABLES 
  /CELLS=ROW 
  /COUNT ROUND CELL.

** 미국 TV n 테이
USE ALL. 
COMPUTE filter_$=(COUNTRY = 1). 
VARIABLE LABELS filter_$ 'COUNTRY = 1 (FILTER)'. 
VALUE LABELS filter_$ 0 'Not Selected' 1 'Selected'. 
FORMATS filter_$ (f1.0). 
FILTER BY filter_$. 
EXECUTE. 
CROSSTABS 
  /TABLES=GCA3_D_ca BY GCA3_1_ca 
  /FORMAT=AVALUE TABLES 
  /CELLS=COUNT 
  /COUNT ROUND CELL.