# LGD Syntax 기타


Use All.
Temp.
Sel if(SQ0=1).
DESCRIPTIVES VARIABLES=A2_G_n2 B2_G C2_G D2_G E2_G F2_G G2_G 
  /STATISTICS=MEAN STDDEV MIN MAX.


Temp.
Sel if(SQ0=1 & A1_2 = 2015).
freq A1.


DESCRIPTIVES VARIABLES=A2_G_n2  
  /STATISTICS=MEAN STDDEV MIN MAX.

Temp.
Sel if(SQ0=2 & GCA3_G < 12001).
DESCRIPTIVES VARIABLES=GCA3_G 
  /STATISTICS=MEAN STDDEV MIN MAX.

Temp.
Sel if(SQ0=1 & A2_G_n2 > 5000).
freq A2_A A2_D A2_E.

====================

temp.
sel if (COUNTRY = 1).
freq A1_4_A.


temp.
sel if (COUNTRY = 1 & (A1_4_A = 3)).
DESCRIPTIVES    VARIABLES    = ADD1
    /STATISTICS    = MEAN.

=======================

temp.
sel if (SQ0 = 1 & A1_4_A =1).
DESCRIPTIVES    VARIABLES    = ADD1
    /STATISTICS    = MEAN.


temp.
sel if (SQ0 = 1 & A1_4_A =2).
DESCRIPTIVES    VARIABLES    = ADD1
    /STATISTICS    = MEAN.


temp.
sel if (SQ0 = 1 & A1_4_A =3).
DESCRIPTIVES    VARIABLES    = ADD1
    /STATISTICS    = MEAN.

temp.
sel if (SQ0 = 1 & A1_4_A =4).
DESCRIPTIVES    VARIABLES    = ADD1
    /STATISTICS    = MEAN.




temp.
sel if (SQ0 = 1 & A1_4_A =3).
freq A1_2.
