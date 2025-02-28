SPSS UHD TV 문제 증상 Syntax


USE ALL. 
COMPUTE filter_$=(S1_1=1). 
VARIABLE LABELS filter_$ 'S1_1=1 (FILTER)'. 
VALUE LABELS filter_$ 0 'Not Selected' 1 'Selected'. 
FORMATS filter_$ (f1.0). 
FILTER BY filter_$. 
EXECUTE. 
CTABLES 
  /VLABELS VARIABLES=S7_2 model_t all2_30 all2_13 DISPLAY=LABEL 
  /TABLE S7_2 [C][COUNT F40.0] BY model_t [C] > (all2_30 [C] + all2_13 [C]) 
  /CATEGORIES VARIABLES=S7_2 model_t all2_30 all2_13 ORDER=A KEY=VALUE EMPTY=INCLUDE 
  /CRITERIA CILEVEL=95.