SPSS Syntax


// 구매자 필터 걸기 //

USE ALL.
COMPUTE filter_$=(S14 = 1).
VARIABLE LABELS filter_$ 'S14 = 1 (FILTER)'.
VALUE LABELS filter_$ 0 'Not Selected' 1 'Selected'.
FORMATS filter_$ (f1.0).
FILTER BY filter_$.
EXECUTE.


// 성별 차이 검증 //

NPAR TESTS
  /K-W=B13_1 BY S2(1 2)
  /MISSING ANALYSIS.



// 기대용도 카테고리로 묶어서 새로운 변수 만들기 //

RECODE B20 (1 thru 4=1) (5 thru 7=2) (8 thru 9=3) (10 thru 15=4) (16 thru 17=5) (18 thru 19=6) (20
    thru 99=7) INTO B20_ca.
VARIABLE LABELS  B20_ca '기대용도 카테고리'.
EXECUTE.
FREQUENCIES VARIABLES=B20_ca
  /ORDER=ANALYSIS.


// 기대 용도 차이 검증 //

NPAR TESTS
  /K-W=B13_1 BY B20_ca(1 7)
  /MISSING ANALYSIS.


// 주 사용 용도 카테고리로 묶어서 새로운 변수 만들기 //

RECODE B21_2 (1 thru 4=1) (5 thru 7=2) (8 thru 9=3) (10 thru 15=4) (16 thru 17=5) (18 thru 19=6) (20
    thru 99=7) INTO B21_2_ca.
VARIABLE LABELS  B21_2_ca '주 사용도 카테고리'.
EXECUTE.
FREQUENCIES VARIABLES=B21_2_ca
  /ORDER=ANALYSIS.

// 주 사용 용도 차이 검증 //

NPAR TESTS
  /K-W=B13_1 BY B21_2_ca(1 7)
  /MISSING ANALYSIS.


// Segment 변수 생성하기 //

RECODE S3 (Lowest thru 49=1) (50 thru Highest=3) INTO Seg.
VARIABLE LABELS  Seg '세그먼트'.
EXECUTE.
FREQUENCIES VARIABLES=Seg
  /ORDER=ANALYSIS.

DO IF (S8_n2 >= 1 or S8_n3 >= 1).
RECODE Seg (1=2).
END IF.
EXECUTE.
FREQUENCIES VARIABLES=Seg
  /ORDER=ANALYSIS.


// 세그먼트 차이 검증 //

NPAR TESTS
  /K-W=B13_1 BY Seg(1 3)
  /MISSING ANALYSIS.


