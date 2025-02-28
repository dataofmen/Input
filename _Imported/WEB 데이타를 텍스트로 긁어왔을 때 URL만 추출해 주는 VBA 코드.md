# WEB 데이타를 텍스트로 긁어왔을 때 URL만 추출해 주는 VBA 코드

가끔 이럴 일이 있었는데 잘 안돼서 매번 얼마나 신경질이 났는지 모름 ㅎㅎㅎㅎ 속이 다 후련하네..

하이퍼링크 데이타만 따로 새 워크시트에 복사해 넣은다음 아래코드로 매크로 돌리면 끝남

Sub ExtractHyperLinks()
On Error Resume Next
Dim HypLnk As Hyperlink
For Each HypLnk In ActiveSheet.Hyperlinks
HypLnk.Range.Offset(0, 1).Value = HypLnk.Address
Next HypLnk
End Sub