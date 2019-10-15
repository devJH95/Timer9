# update Timer9View.cpp
<br/>
<center><img src="/riverduck.jpg" width = "500px" height="300px" ></center>
<br/>

```C++
void CTimer9View::OnInitialUpdate()
{
	CView::OnInitialUpdate();

	SetTimer(1, 500, NULL);
	SetTimer(2, 1000, NULL);
	// TODO: 여기에 특수화된 코드를 추가 및/또는 기본 클래스를 호출합니다.
}


void CTimer9View::OnTimer(UINT_PTR nIDEvent)
{
	// TODO: 여기에 메시지 처리기 코드를 추가 및/또는 기본값을 호출합니다.
	CClientDC dc(this);
	CFont f;
	f.CreatePointFont(500, L"굴림");
	dc.SelectObject(&f);
	if (nIDEvent == 1) {
		static int n1;
		CString str;
		str.Format(L"%d", ++n1);
		dc.TextOut(10, 100, str);
	}
	if (nIDEvent == 2) {
		static int n2;
		CString str;
		str.Format(L"%d", ++n2);
		dc.TextOut(10, 200, str);
	}
	CView::OnTimer(nIDEvent);
}
```

