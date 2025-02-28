# 센터코드 분석 syntax


temp.
sel if(coun2=3501 and prod=1 and test_br=2).
CTAB
  /FORMAT EMPTY=BLANK MISSING='.' /SMISSING VARIABLE
  /VLABELS VARIABLES=PROD MANU
    DISPLAY=DEFAULT 
  /TABLE ((d_total[VALIDN paren3.0 '사례수']+d_total[MEAN f3.0 '평균']+d0[MEAN f3.0 '평균']+d_dimen[MEAN f3.0 '평균']
+d1[MEAN f3.0 '평균']+d2[MEAN f3.0 '평균']+d3[MEAN f3.0 '평균']+d4[MEAN f3.0 '평균']+d5[MEAN f3.0 '평균']
+d6[MEAN f3.0 '평균']+d8[MEAN f3.0 '평균']+d9[MEAN f3.0 '평균']+T1_1[MEAN f3.1 '평균']+all2_20[C][COLPCT.COUNT PCT40.0]
- [x] t1_1_edit[C][COLPCT.COUNT PCT40.0]+t4_1_edit[C][COLPCT.COUNT PCT40.0]+all2_30[C][COLPCT.COUNT PCT40.0]

+all2_36[C][COLPCT.COUNT PCT40.0]+all2_13[C][COLPCT.COUNT PCT40.0])) 
BY region[c]>(center_type[c]>center_code[c])
  /CATEGORIES VARIABLES=prod coun2 region center_type center_code ORDER =A KEY=VALUE EMPTY=Exclude
  /SLABELS POSITION=ROW
/tit title='17년 KPI Summary' .