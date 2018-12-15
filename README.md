주제: TNR 수요 예측을 통한 
1.	선정 배경
길고양이의 개체 수를 조정하는 효과적인 방법은 살처분이 아닌 TNR이다. TNR은 Trap-Neuter-Return의 약자로 길고양이를 포획한 후 중성화 수술을 진행한 뒤, 다시 자연으로 방사하는 방법이다. 고양이 보호 협회에서는 동물병원과 협약을 맺어 길고양이 TNR 사업을 진행 중이다. 하지만 협회의 재정, 병원의 가용 자원 부족 등으로 어려움을 겪고 있다. 협회의 TNR신청 데이터를 분석하여 수요를 예측하고 병원의 스케줄을 조정하여 문제를 해결하고자 한다.
2.	예상 기대
수요예측을 통해 협약을 맺은 동물병원에 중성화 수술을 부탁할 때 유연한 스케줄 조정을 지원한다.(SCM과 조금 비슷하다.)
3.	분석 과정  
i.	데이터 수집  
한국 고양이 보호협회(http://www.catcare.or.kr/) 홈페이지에서 TNR요청 게시글 정보를 웹 스크래핑한다. 게시글의 정보에는 게시글 번호, 게시글 분류, 제목, 글쓴이, 날짜, 조회수가 있다. 게시글 정보로부터 게시글 번호, 제목, 날짜, 조회수를 가져온다.  
ii.	데이터 사전 분석  
게시글의 정보를 토대로 사전분석을 실시한다. 간단한 시계열 분석, 제목을 통한 텍스트 분석 및 워드 클라우드, TNR요청과 포획실패에 따른 포획률 살펴보기 등등  
iii.	모델링  
LSTM을 통한 TNR 수요 예측.   
iv.	평가  


4.	데이터 출처 및 변수
한국 고양이 보호 협회(http://www.catcare.or.kr/index)

TNR요청 게시판(로그인을 해야 게시판에 접근 가능)  
게시글 번호: 게시글의 번호 (정수형)  
제목: 제목 (문자열)  
날짜: 게시글 작성 날짜 (년월일)  
글쓴이: 게시글을 작성한 사람의 닉네임 (문자열)  
조회수: 게시글을 조회한 수 (정수형)  

5.	관련 기관  
한국 고양이 보호 협회  
한국 고양이 보호 협회와 계약을 맺은 동물 병원들
