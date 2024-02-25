# CSS 기본
- Casacading style sheet의 약자로 HTML의 색. 크기, 정렬 등을 변경하여 꾸며주는 언어를 의미한다.
- CSS의 특성
- (Property)에는 색, 크기, 정렬 등이 존재한다.
## CSS 사용법
- `selector(선택자) {
	property(속성) : value(값);
    property(속성) : value(값);
    property(속성) : value(값);
    property(속성) : value(값);
 }`
 - 선택자는 class로 정의한 것이나 id로 정의한 것을 사용할 수 있다.
 - value뒤에 ";"자는 꼭 필수적으로 사용해주어야 한다!
 - css 파일 불러오기  <link rel="stylesheet" href="style sheet example.css">

 ## CSS 박스모델
 - content-box, boder-box가 있다.
 - boder-box : boder이 고정이 되고, contents의 크기가 바뀐다.(padding과 margin 조절로 인해) -> 박스가 고정
 - contents-box: contents가 고정이 되고, boder의 크기가 바뀐다. -> 박스가 커짐


## 정렬 display : flex; 속성
-/* 부모박스 */
    display: flex;

/* 행기준: row, 열기준: column */
    flex-direction: row;
    flex-direction: column;

/* flex-direction 기준 수평 방향으로 자식박스 정렬 */
    justify-content: center;

/* flex-direction 기준  수직 방향으로 자식박스 정렬 */
    align-items: center;

 ## 네비바 css꾸미기
 - 부모 -> 자식 순으로 ui 점 없애주기, li a 링크스타일 없애주기
 - /* 현재 페이지 링크 스타일 */
nav ul li **a.active** , nav ul li **a:hover** {
    font-weight: bold; /* 볼드체 적용 */
}
- /* 링크에 마우스 호버 시 스타일 */
nav ul li **a:hover** {
    color: black;
}

## 부모요소 동그라미 형태로 만든 뒤, 이미지 첨부하기
-
.부모요소 {
    width: 400px;
    height: 400px;
    flex-shrink: 0;
    border-radius: 50%; /* 원형으로 표시 */
    overflow: hidden; /* 넘치는 부분 숨김 */
    display: flex; /* 이미지를 중앙 정렬하기 위해 flex 사용 */
    justify-content: center; /* 가로 방향 중앙 정렬 */
    align-items: center; /* 세로 방향 중앙 정렬 */
}
.이미지 {
    width: 100%; /* 컨테이너 너비에 맞춤 */
    height: 100%; /* 컨테이너 높이에 맞춤 */
    object-fit: cover; /* 이미지 비율을 유지하면서 컨테이너를 가득 채움 */
    object-position: center; /* 이미지를 중앙에 위치시킴 */
}

## 