SPSS Syntax

*변수 생성 top2%
Recode	Q56A1	(1 2 eq 1 ) (3 4 5 eq 2) (6 7 eq 3)	into Q56A1_N.	
Recode	Q56A2	(1 2 eq 1 ) (3 4 5 eq 2) (6 7 eq 3)	into Q56A2_N.	
	
Val lab 	Q56A1_N	1"Bottom 2%" 2"Soso" 3"Top2%".	
Val lab 	Q56A2_N	1"Bottom 2%" 2"Soso" 3"Top2%".	

Var lab	Q56A1_N	"wifi 선호".	
Var lab	Q56A2_N	"wifi 필요도".	


*변수 생성 top3%
Recode	Q51A1	(1 2 3 eq 1 ) (4 eq 2) (5 6 7 eq 3)	into Q51A1_N.	
Recode	Q51A2	(1 2 3 eq 1 ) (4 eq 2) (5 6 7 eq 3)	into Q51A2_N.	

Val lab 	Q51A1_N	1"Bottom 3%" 2"Neutral" 3"Top3%".	
Val lab 	Q51A2_N	1"Bottom 3%" 2"Neutral" 3"Top3%".	

Var lab	Q51A1_N	"  Multi Watt (Watt Option) 중요도".	
Var lab	Q51A2_N	"  SkinCare 중요도".	