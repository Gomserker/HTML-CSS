## Playlist 껍데기만 만들어보기  
![](https://github.com/Gomserker/HTML-CSS/blob/main/SelfStudy/Playlist/structure.png)  
구조는 대략 이렇습니다.  


### 1. 레이아웃  
레이아웃은 flex만 사용했고, 세부적인 위치는 margin과 padding으로 조절했습니다.  

### 2. 아이콘  
아이콘은 Font Awesome에서 가져왔습니다. 정말 좋아요 꼭 쓰세요.  

### 3. 그래서 Table은 어디로 가고 flex라는걸 썼냐?  
개인적으로 table 레이아웃을 정말 싫어합니다. 너무 제약도 많고 쓰기도 어렵고 코드도 지저분해요. 언제 tr,td 계산해가며 넣고 앉았음;;  
flex에 대한 설명은 [여기](https://studiomeal.com/archives/197) 블로그에서 정말 맛깔나게 설명을 해주셨으니 참고하시고, 여기서는 메인축과 교차축에 대한 설명만 간단하게 드리겠습니다.  

### 4. main-axis? cross-axis? justify-content? align-items?  
먼저 main-axis와 cross-axis는 어감이 주는 느낌으로 아시겠지만, main-axis는 주축, 주로 사용하는 축입니다.  
기본적으로 html은 가로로 나열하려는 성질이 있는 모양인지 display: flex를 선언하고 컨텐츠를 나열하면 가로로 다닥다닥 붙어버립니다.  
그런 의미에서 기본축인 main-axis는 가로고, cross-axis는 단어 그대로 교차축이니까 가로를 교차하는 세로가 되겠네요?  
안타깝습니다만 그렇지는 않습니다. 그러면 vertical, horizon이라고 하지 뭐하러 메인축, 교차축으로 나눠놨겠어요?  
여기서 **flex-direction** 이라는 친구가 등장합니다. 말 그대로 flex의 방향을 결정하는데, 디폴트 값이 row로 flex 컨테이너 안의 요소들을 가로로 나열하겠다고 하는 겁니다.  
여기서 flex-direction: column; 을 적용하면 메인축이 세로가 됩니다. 이래서 main은 가로, cross는 세로로 외우면 안된다는 거죠.  
간단하게 자신이 컨텐츠를 나열하고 싶은 방향을 메인축이라고 생각하시면 문제 없을것 같습니다. 그럼 이제 justify-content와 align-items에 대해 알아보죠.  

#### justify-content : 메인축 정렬
#### align-items : 교차축 정렬  

정렬하는 방법도 정말 많습니다. 디폴트 값인 flex-start랑 flex컨테이너 끝쪽으로 몰아버리는 flex-end, 가운데로 정렬하는 center, 처음과 마지막 컨텐츠를 끝에 놓고 간격을 일정하게 정렬하는 space-between, 간격을 일정하게 정렬하는 space-evenly 등등  
전부 외울 필요도 없고, 필요할때마다 flex의 정렬 효과를 찾아보는게 좋을 것 같습니다. 물론 가장 좋은 방법은 직접 써보는 거겠죠...? 위에 예시에서 한번 살펴보겠습니다.  
오른쪽 페이지의 앨범 커버와, 곡 제목, 가수 이름을 한 컨테이너에 넣었는데요, css파일을 보시면 아시겠지만 저기서 flex-direction: column, justify-content : center, align-items: center 값을 먹였습니다.  
그리고 flex-direction: column이니 각 컨텐츠가 세로로 나열되고, 메인축 가운데, 교차축 가운데로 정렬했으니 화면 가운데로 줄을 서게 됐습니다. 만약 저기서 flex-direction에 column을 주지 않았다면 가로로 다닥다닥 붙어서 와장창 났을겁니다.  


이렇게 간단하게 flex와 메인축, 교차축, 그리고 정렬을 정리해 봤습니다. 익숙해지는데 시간이 걸리고, 아직도 익숙해지려면 한참 남았지만 분명 편한 레이아웃임에는 틀림없는듯 합니다.  
위에 링크로 걸어둔 블로그는 정말 재밌게 설명을 해뒀으니 꼭 한 번 읽어보시길 추천드립니다.
