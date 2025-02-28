SCSI 신택스 - 시간 만족도 BP 


sel if(test_type=2 and test_br=2 and test_reg=2 and test_is=2 and test_prod=2 ).
CTAB
  /FORMAT EMPTY=BLANK MISSING='.'  /SMISSING VARIABLE
  /VLABELS VARIABLES=PROD MANU
    DISPLAY=DEFAULT 
  /TABLE (coun2[c]>(d_total[VALIDN paren3.0 '사례수']+d5[MEAN f3.0 '평균'])) 
BY t1_1[c]
  /CATEGORIES VARIABLES=prod coun2 t1_1 region center_type center_code ORDER =A KEY=VALUE EMPTY=Exclude
  /SLABELS POSITION=ROW
/tit title='17년 KPI Summary' .
