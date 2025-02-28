LGD 분석 syntax 2


*** 미국, 1인가구, 태블릿 구매 가격

Use all.

temp.
sel if (SQ0 = 1 and DQ2 = 1 and (used_tablet = 0 and buy_tablet = 1)).

DESCRIPTIVES VARIABLES=D2_G
  /STATISTICS=MEAN STDDEV MIN MAX.


*** 미국, 2인가구, TV 구매 가격

Use all.

temp.
sel if (SQ0 = 1 and DQ2 = 4 and (used_tv = 0 and buy_tv = 1)).

DESCRIPTIVES VARIABLES=A2_G_n2 A2_E
  /STATISTICS=MEAN STDDEV MIN MAX.
