# html이란

### < html, css, javascript >

구조 : `html` 웹 문서의 기본 골격이자 뼈대
표현 : `css` 각 요소들의 레이아웃과 스타일링, 배치와 ux 증대
동작 : `javascript` 동적요소, ui에 따른 행동

### < html과 css를 구분하여 사용하면 >

- 하나의 html에 두개의 css를 적용할 수도 있고
- 여러개의 html에 하나의 css를 적용할 수도 있다.(사용성 증가)
  _스타일드 컴포넌트보다 sass를 선호하는 이유가 될 수도 있겠다._

### < 웹표준과 웹접근성, 호환성 >

모든 브라우저는 각기 다른 기본값들을 갖고있다.
예를 들어 `< button >이건 버튼< /button >` 을 css 적용 없이 실행하면 브라우저마다 다르게 표현된 버튼을 확인할 수 있다. <br/>
<img src="https://nuli.navercorp.com/data/img/blog/hhj/img/compare_button.gif" width="500px"/>

만약 이 차이가 더 극명하다면?

`어쩌면 유저가 버튼이라고 인지하지 못하는 버튼이 생길 수도 있을 것이다.?!`

이를 방지하고자 문법 사전을 만들기로 함
= <strong>웹표준 HTML5버전(w3c_2014)</strong>

이후 2019 WHATWG(애플,모질라,구글,MS)가 제안한 HTML Living Stansard를 w3c가 수용하면서 공식 웹표준으로 인정.

- <b>웹접근성 (Web Accessibility)</b>
  장애여부와 관계없이 웹을 사용할 수 있게 만드는 것. 이는 일시적 장애, 상황적 제약 등을 모두 포함한다.
  <br/>
- <b>웹호환성 (Cross Browsing)</b>
  웹 브라우저 버전, 종류에 관계없이 웹사이트에 접근이 가능하게 만드는 것. 웹표준을 준수하여 브라우저의 호환성을 확보할 수 있다.

### < html 작성 >

- <b>빈요소(Empty Elements)</b>
  일반적인 html 요소는 `< 오프닝 태그 > 내용 </ 클로징 태그 >` 로 만들 수 있으나 내용없이 사용하는 태그를 `빈요소 태그` 라고 한다. 내용이 없는 빈 요소 태그는 어트리 뷰트만을 갖는다.이 경우 오프닝 태그만 작성하여도 동작하지만 명시적으로 /(슬래시)를 붙여주는 것이 좋다. 대표적인 빈 요소로는 img, br, hr, input, link, meta 등이 있다.
  `< img src="#" / >`
  `< link rel="icon" / >`
  <br/>
- <b>요소 중첩(Nesing)</b>
  요소 안에 다른 요소가 들어갈 수 있다.
  부모-자식 관계는 들여쓰기(Tab)으로 구분한다.
  <br/>
- <b>주석</b>
  html의 주석처리는 < !--내용-- > 으로 한다.
  <br/>

### < html 문서의 구조 >

<b>html</b>
페이지 전체를 감싸는 최상위 루트(root) 요소

<b>head</b>
웹 페이지의 정보. 기계(브라우저)가 식별할 수 있는 문서정보를 담는다. 단 하나의 < title > 태그를 찾는다.

- `< title ></ title >`
- `< script ></ script >`
- `< styled ></ styled >`

<b>body</b>
웹 페이지에 보이는 모든 콘텐츠를 보여준다.
특성, 속성, Attribute는 body 안에 사용되는 태그이다.

<br/>

### < body 영역 >

#### 블록(Block) 과 인라인(Inline) ⭐️⭐️⭐️⭐️⭐️

<a href="https://velog.io/@wonder1247/inline요소와-block요소에-margin-적용" alt="인라인 요소와 블록 요소의 마진 적용 링크">연관 링크 : 인라인 요소와 블록 요소의 마진 적용 <kbd>클릭</kbd> </a>

`블록(block)`
언제나 새로운 라인에서 시작하며 실제 사용하는 공간에 상관없이 부모가 허용한 최대 width를 사용한다.
`인라인(Inline)`
줄 어디에서나 시작할 수 있고, 이전 요소가 끝나는 지점부터 시작해 요소의 내용(content) 만큼 차지한다.

<br/>

<img src="https://velog.velcdn.com/images/wonder1247/post/2dc4848e-9f5a-41de-b88a-9613c5c1e389/image.png" width="500px"/>

<br/>

<hr/>

<br/>

### < html의 텍스트 요소 >

- #### 제목 H1~H6

H1이 제일 크고 H6이 제일 작다. H7은 존재하지 않음.
브라우저는 H1~H6을 기준으로 웹페이지를 `목록화` 하기 때문에 되도록 용도에 맞게 쓰는게 좋다.
글씨 크기를 위해 H1을 쓰지 말 것.
지금 보이는 H1이 모든 브라우저에 동일하게 표현되는 건 아니니 글씨 크기는 CSS를 통해 변경할 것. ⇨ reset.css 써서 초기화 하기
페이지단 하나의 H1만 사용하는 것이 스크린리더와 SEO에 적합하다.

- #### p (paragraph)

블록단위 요소
html은 엔터를 인식하지 않고 스페이스(사이띄기)는 1개만 인식한다.

- #### br

텍스트 요소 안에서 줄바꿈을 생성한다.(일종의 엔터)
빈요소 < br > < br/ >
문장 하나의 크기만큼 줄바꿈 된다. => 더 많은 줄바꿈을 원한다면 < br/ > 을 중첩하지 말고 css를 통해 변경하기
문단의 구분이 없다. => 접근성에 대한 고려가 필요함

- #### blockquote, q 인용요소

blockquote는 블록요소, q는 인라인 요소로 둘 다 인용하고 싶은 텍스트를 가져올 때 사용한다.
lockquote는 p 태그로 감싸면 안됨. p태그가 자동으로 닫히기 때문이다.

<img src="https://velog.velcdn.com/images/wonder1247/post/66fac6b8-12d1-44ec-857c-33765c025d4d/image.png" width="500px">

- #### pre

preformatted : 미리 서식이 준비된
< pre > 태그 안에 있는 내용은 입력값 그대로 모든 개행요소가 표현된다.
< pre > 안에는 스페이싱과 엔터가 입력값 그대로 표현된다.
고정폭 글꼴을 사용하여 모든 텍스트가 동일한 너비를 갖는다. 즉, A와 I가 동일한 글자폭을 갖는다.

<pre>
pre 태그 내에서 작성되는 글입니다.
원래 html은 스페이싱이 1개만 인식되고 엔터도 인식되지 않아 < br/ >을 사용하는데
< pre > 태그 내에 서는 
엔터는
물론이고
스    페    이    싱    도 
적    용    된    다    .
</pre>

- #### figue, figcaption
  figue 독립적인 콘텐츠를 표현할 때 사용한다.
  ⇨ < pre > 태그에 쌓인 콘텐츠, < blockquote > 의 긴 인용글

figcaption figue 태그 안에 콘텐츠의 위나 아래에 설명을 붙일 수 있다.

<img src="https://velog.velcdn.com/images/wonder1247/post/f9e8f7f9-11f6-4174-ab7a-3ca928298787/image.png" width="500px">

- #### hr
  horizon : 경계선
  문단 레벨에서의 주제 분리를 위해 사용된다.
  빈요소 < hr > < hr/ >
  ss를 통해 스타일을 바꿀 수 있다.

<br/>

### < html의 텍스트 요소 : 포매팅 formating >

포매팅 : 나열된 문단 속 문장이나 단어를 강조하는 것.

- #### b, strong 강조

  `b (bold)` 굵은 글씨 요소 : 요약의 키워드, 리뷰 속 제품명, 별로 중요하진 않지만 괜히 굵게 표시해서 있어보이고 싶은 것에 사용.

  `strong` 높은 중요도 요소 🟡 : 키워드 부터 문단까지 중요한 요소에 적용시킬 수 있다.

- #### i, em 기울기

  `i` 텍스트에서 어떤 이유로 <i>주위와 구분해야 하는 부분</i> 을 나타낸다.
  `em` 강세 요소. 요소를 중청하면 <em>강강세세</em> 요소.

- #### mark, small, sub, sup

  `mark` 현재 맥락에 관련 깊거나 중요할 때 하이라이트 표시

  - < p> 네가 < mark > 웃으면 < /mark > 나도 좋아 < /p > ( 네가 <mark> 웃으면 </mark> 나도 좋아 )

  `small` 덧붙임 글 요소

  `sub` 아래 첨자

  `sup` 위 첨자

- #### del, ins, code, kbd

  `del` 텍스트 취소선, 삭제

  `ins` 추가된 텍스트 표시

  - 토끼 나비 당근 < del >딸기</ del > < ins >젤리</ ins > 말랑
  - 토끼 나비 당근 <del>딸기</del> <ins>젤리</ins> 말랑
  - cite : 이슈 추적 내용 추가 가능 (삭제이유, 추가이유)
  - datatime : 변경 발생 일자

  `code` 인라인 요소, 문장 중간에 짧막하게 코드 요소를 넣고 싶을 때 사용. 고정폭 글씨체.
  여러 줄을 표시하고 싶으면 겉에 < pre > 로 감싸고 < code >를 적으면 된다.
  <br/>
  `kbd` 키보드 표현 요소 .

  - <kbd>cmd</kbd> + <kbd>s</kbd> 는 저장 단축키 이다.
  - < kbd > cmd < /kbd > + < kbd > s < /kbd >

<br/>

### < html의 텍스트 요소 : a태그와 하이퍼링크 >

- #### a태그
  Anchor 앵커
  어트리뷰트 href를 통해 특정 주소로 이동하는 하이퍼링크를 만든다.

`절대경로` : 현재 위치와 관계없이 정해진 위치로 이동할 수 있다.

```
<a href="https://www.mozilla.com">
```

`상대경로` : 브라우저나 로컬상태와 같이 다른환경에서 변화하는 이동경로.(로컬 환경에서 폴더위치 등)

<img src="https://velog.velcdn.com/images/wonder1247/post/f082cde2-5d92-40f1-bb90-a08d2977b6ea/image.png" width="200px" >

<br/>

href 로 메일이나 연락처를 연결할 수 있다.

```javascript
<a href="mailto:glow2myself@gmail.com"> 이메일 연결 </a>
<a href="tel:010-000-0000"> 연락처 연결 </a>
```

href 로 지정한 링크를 어디에 띄울 것인지 정할 수 있다.
`_self` : 기본값. 현재 브라우저, 현재 탭에 열기
`_blank` : 현재 브라우저, 새로운 탭에서 열기

```javascript
<h3> 속성2 = terget </h3>
<a href="https://www.mozilla.com" target="_blank">Mozilla</a>
```

- #### 엔티티(Entity)
  html에서의 엔티티는 < 나 > 또는 " & 같은 태그 예약어를 그대로 사용하고 싶을 때 쓰는 방법을 말한다.

< p > 해당 태그를 html파일에 그대로 적으면 태그로 인식되어 페이지에 보이지 않지만
&lt;p&gt;`&lt;p&gt;` 이런식으로 엔티티를 사용해 태그 그대로를 표현할 수 있다.
"힣" `&qout;힣&qout;`
(여백) `&nbsp;&nbsp;&nbsp;`

<img src="https://velog.velcdn.com/images/wonder1247/post/c0cc2b71-141b-4cfe-b985-4158da18d617/image.png" width="500px">

<br/>

### < html의 구조 요소 : container 요소 >

- #### div

  division
  특정 구획이나 구역을 나누는 태그.
  블록 라인 요소이다.
  flow contents를 위한 통용 컨테이너
  블록 요소이고 순수 컨테이너로 내용이 없으면 css를 주지 않을 때는 보이지 않는다. \*순수컨테이너 \_ div 자체는 의미없는 태그이다.
  <b>무분별한 div 남용보다는 기획의도에 맞는 `시멘틱 태그`(head, nav, article...)을 사용하는 것이 웹표준과 사용성에 맞다.</b>

- #### span
  div와 사용은 동일, 순수 컨테이너
  다만, 인라인 요소로 구문 컴텐츠를 담는다 (text)

<img src="https://velog.velcdn.com/images/wonder1247/post/42b2be84-4913-4383-a202-67d35f029c79/image.png" width="500px">

<img src="https://velog.velcdn.com/images/wonder1247/post/cb230ca7-ada9-4c7f-a713-da483caeaa27/image.png" width="500px">

<br/>

### < html의 구조 요소 : 시멘틱웹 Semantic Web >

Semantic : 의미, 의미론적인
요소의 의미를 고려하여 구조를 설계하고 코드를 작성한다.

✅ 의미론적인 마크업을 사용하면 생기는 장점

- SEO에 용의
- 스크린 리더 사용 시 정확한 전달이 가능하여 접근성을 높일 수 있음.
- 의미있는 코드블록을 사용했을 때 개발자간의 소통이 원활해지고 코드 찾기도 쉬움.
- 의미있는 이름짓기는 사용자 정의 요소/ 구성 요소의 이름짓기를 반영.

<img src="https://velog.velcdn.com/images/wonder1247/post/d6445a8c-78b4-4e7c-99c1-855a64011653/image.png" width="300px">
<img src="https://velog.velcdn.com/images/wonder1247/post/808b5c58-f403-4f96-bb0c-a7736e286516/image.png" width="300px">

- #### header, footer
  `Semantic Tag`, `Block Container`
  웹페이지의 header는 하나만 사용 가능하다.
  header 안에 다른 header 나 footer는 올 수 없다.
  페이지제목 < h1 >, 글제목 < h2 >
  소개, 탐색에 도을을 주는 콘텐츠

footer는 웹페이지 정보, 연관사이트연결, 홈페이지 단체, 연락망 등의 정보를 포함한다.
footer안에 다른 footer나 header는 올 수 없다.

- #### nav

  navigation
  `탐색, 구획 요소`
  웹 전체 nav 또는 페이지 내 목차형 nav (ex 나무위키)로 사용 가능

- #### aside

  sidebar
  본문과 직접적인 관련은 없지만 옆에 적고싶은 내용
  웹페이지 광고를 띄울 때 사용하는 편.

- #### main

  `< body >태그 하위의 자식 태그로 오직 1개만 사용할 수 있다.`
  body의 핵심주제나 핵심 기능이 직접적인 연관있는 것을 담는다.
  문서에 2개 이상의 main이 존재할 경우, 하나 이외의 main은 `hidden` 속성값으로 숨겨야 한다.

- #### article
  문서, 페이지 또는 사이트 내에서 독립적으로 구분되어 배포, 재사용 가능한 구획

하나의 문서 안에 여러개의 aritcle이 존재할 수 있다.
article 내에 구분되는 `h2` 제목이 사용되면 좋다.

- #### session

  article로 <strong>사용할 수 없는 독립 객체</strong>

<br/>

### < html의 목록 >

- #### List 요소

  - ul ( unordered list )
    비정렬 목록, 순서없는 목록
    목록 내 중첩이 가능하고, 불렛 포인트의 차이로 구분된다.

  - ol ( orderd list )
    순위가 있거나 단계적으로 수행해야 하는 레시피 같은 것.
    기본적으로 숫자로 정렬 (type="1")

    - type 속성
      < ol type="1" > 1.2.3....
      < ol type="i" > i. ii. iii....
      < ol type="a" > a.b.c....
      < ol type="A" > A.B.C....

    - start 속성
      항목을 셀 때 시작하는 수를 설정할 수 있다.
      type이 'a','A'이거나 'i','I' 인 경우,
      'd'나 'iv' 부터 세고 싶다면 start="4" 라고 적으면 된다.
    - reversed
      목록의 순번이 역전된다.
      1.2.3. -> 3.2.1

  - li ( list item )
    ul과 ol 안에 속하는 단일 아이템

- #### 용어 정리
  - dl ( defination list ), dt dd
    `dt`로 표기한 용어와 `dd`로 표기한 목록을 감싸서 dl을 생성한다.
    <img src="https://velog.velcdn.com/images/wonder1247/post/009c402a-6bd8-431c-9bd2-85172256f004/image.png" width="500px">

### < html의 표 >

- #### table, caption
<img src="https://velog.velcdn.com/images/wonder1247/post/3ac661ea-0a11-4f91-a932-632618b630d2/image.png" width="500px">

<img src="https://velog.velcdn.com/images/wonder1247/post/bc1fb5c6-3e27-47f8-bc9b-7abf13412065/image.png" width="500px">

### < html의 img >

- #### img 태그

  내부 내용을 작성하는 코드가 아닌 빈요소로 내용을 적어도 보이지 않는다.
  필수 어트리뷰트 Atrribute 속성으로 `src` 를 포함하여 이미지 경로를 지정한다. `alt` 속성은 이미지의 설명을 적는 텍스트 이고, 필수는 아니지만 스크린리더 사용자에게 이미지를 읽어주기 때문에 접근성에 용이하다.

- #### img의 경로

  절대경로와 상대경로

  - 절대경로
    어떤 위치에서 불러도 동일한 장소로 도달하는 경로
    예\_이미지의 웹주소
  - 상대경로
    현재 위치에서 찾는 경로
    예\_A위치에서 C파일로 가는 123, B위치에서 C파일로 가는 023

- #### img의 alternative text

  스크린리더 사용에 도움을 주거나 이미지가 어떠한 이유로 불러오기 어려울 경우, 대체 텍스트를 이용하여 이미지가 어떤 이미지인지 설명을 대체할 수 있다.
  간혹, alt 를 마우스 오버 시 툴팁으로 보여지는 경우가 있는데 그건 브라우저 설정에 따른 것이므로 마우스 오버 툴팁을 지정하고 싶으면 title 속성으로 주면 된다.

- #### img 의 width, height

  width, height 모두 이미지의 픽셀 기준 고유 너비.
  단위 없는 정수.
  width="100" (단위 없는 정수)
  width 또는 height 중 하나만 지정하여도 원본 이미지에 비례하여 자동으로 변화된다.
  width와 height의 값을 각각 지정했다면 지정값으로 변화한다.

- #### 웹에서 사용하는 이미지 유형

  html은 지원하는 이미지를 명시하지 않지만 브라우저(사용자 에이전트)별로 지원형식이 다르니 확장자를 보기 전에 브라우저들에서 사용 가능한 확장자가 무엇인지를 확인하는 것이 중요하다.
  <br/>
  캔아이유즈
  https://www.caniuse.com
  <br/>
  <img src="https://velog.velcdn.com/images/wonder1247/post/e055353d-35a3-43c6-b651-992b6bece723/image.png" width="700px">

- #### img : 반응형 적용 - srcset
  브라우저별로 적용시킬 수 있는 이미지 세트를 만드는 것.
  쉽표로 구분하는 한개 이상의 이미지 목록을 말한다.
  - 여러 개의 이미지 경로 지정 가능.
  - 사용자의 뷰포트에 따른 반응형에 적용할 수 있다.
  - 너비서술자, 밀도서술자 사용
  - srcset = "소스주소 너비w 픽셀밀도x, ..."

```html
<img src="../img/large.png" /* 대표 src는 반드시 넣어줘야 함 */ srcset=
"../img/small.png 300w, /* url, 너비서술자 */ ../img/medium.png 450w,
../img/large.png 600w" alt="image set" />
```

- #### img : 반응형 적용 - sizes

  src set는 뷰포트에 따라서 다른 이미지를 주지만
  sizes는 조건에 따라서 다른 파일을 주거나, 파일의 width값을 지정해서 보여줄 수 있다.

  min-width : 지정값보다 큰 화면일 경우,
  max-width : 지정값보다 작은 화면일 경우

```html
<img
  src="../img/large.png"
  sizes="(min-width: 600px) 600px, /* 600px보다 큰 화면은 600px 로 고정된 이미지를 보여줘 -> 화면이 600~450px 사이에서 600px 사이즈로 고정되어 보여진다. */
                 (min-width: 460px) 450px, 
                 300px"
  alt="image set"
/>
/*600px 보다 큰 화면이면 600px로, 460px 보다 큰 화면이면 450px로, 그것도 아니면
300px로 보여줘*/
```

### < html의 video >

- #### < video > < /video >

  - src : 경로. video 태그의 src는 선택사항이다. 이유는 video 태그 내부에 < sourse src="./video/location.mp4" >로 여러개의 소스를 적용 가능하기 떄문이다.
  - 빈 요소가 아니므로 내용 = alternative 속성처럼 브라우저가 미지원 시 대신 적용된다.
  - controls : boolean 속성. 입력하면 컨트롤 패널이 보인다.
  - autoplay : 자동재생. 페이지를 새로고침하면 멈추게 된다.(사운드가 있을 경우)
  - mute : 영상의 음성을 막는다. 영상이 음소거 된 경우는 autoplay는 자동으로 실행된다.
  - poster : 지정하지 않을 경우 영상의 첫 프레임이 썸네일이 된다.

- #### audio

  - src : video와 같이 선택사항으로 태그 내부에 < source src="" >로 여러개의 소스를 적용 가능하다.
  - controls : boolean 속성. 입력하면 컨트롤 패널이 보인다.
  - autoplay : 자동재생. 사용자 경험을 이유로 audio 속성은 자동재싱이 적용되지 않을 수 있다.

- #### canvas, iframe
  - canvas는 자바스크립트를 사용해야 함.
  - 인라인 프레임 안에 다른 html 페이지를 삽입할 수 있다.(보통 지도, youtube)

### < html의 ⭐︎ form 폼 (사실 form보다는 input)>

사용자가 작성하는 정보를 받을 수 있다. 단독 사용은 안되고 내부에 input 같은 요소를 넣어주어야 한다.

- #### action, method

  - action : 양식데이터를 처리할 프로그램의 url (절대, 상대경로)
  - method : GET, POST 등 메소드를 지정할 수 있다.
    특히 GET 메소드는 제출 시 주소창에 입력내용이 드러나므로 비번 같은 민감정보는 해당 방식으로 보내면 안된다.
    주로 키워드, 검색창 등에 사용한다.

- #### label 과 input
  - input 영역을 설명해주는 label을 붙여주면 사용자의 편의성이 좋아지고 접근성도 좋아진다.
  - input MDN [링크 바로가기](https://developer.mozilla.org/ko/docs/Web/HTML/Element/Input)
  - input은 다양한 type을 갖는다.
  - ⭐︎ label의 `for`과 input의 `id`를 동일한 이름을 사용해 연결할 수 있다.
  - label은 이미지 등이 올 수 없다. >css / bg-img로 넣어보니까 label에 적용은 되는데 텍스트가 옆으로 옮겨지지 않음. 상위 div에 적용하고 label에 마진으로 넓히는 건 가능.

```html
<div>
  <label for="color">
    좋아하는 색 ::
    <input type="text" id="color" />
  </label>
</div>
```

<img src="https://velog.velcdn.com/images/wonder1247/post/2f1c59ad-d5f8-4d8b-ba1d-3b9ddfb21a14/image.png" width="300px">

- #### feildset, legend
  여러 input을 역할 별로 구분할 수 있게 만든다.
  legend는 fildset의 자식으로 올 수 있다.
  feildset의 첫번째 자식이 legend가 와야 한다.

```html
<form>
  <fieldset>
    <legend>제일 좋아하는 것</legend>

    <input type="radio" id="쿠키" name="좋아" value="K" />
    <label for="쿠키">마카다미아 쿠키</label><br />

    <input type="radio" id="음료" name="좋아" value="S" />
    <label for="음료">딸기우유</label><br />

    <input type="radio" id="한식" name="좋아" value="M" />
    <label for="한식">된장찌개</label>
  </fieldset>
</form>
```

<img src="https://velog.velcdn.com/images/wonder1247/post/1589a8ff-75da-4692-a452-5fdb548e4cb8/image.png" width="300px">

- #### input type(1) :: text입력

  - input type="text"
    한 줄만 입력 가능. 개행을 위해 Enter 입력 시 제출.
    min-length 와 max-length 로 글자수 제한 가능.
    min-length 미만 입력 후 제출 시 브라우저 제공 툴팁이 확인 가능

  <img src="https://velog.velcdn.com/images/wonder1247/post/afafb059-14f7-4a24-be5c-1bc0d80e1cee/image.png" width="600px">

  - input type="password"
    type="text"와 동일하나 마스킹 처리되어 보인다.

  <img src="https://velog.velcdn.com/images/wonder1247/post/ee41b95d-9c68-4f9e-b179-216faaa9247c/image.png" width="600px">

  - input type="email"
    브라우저가 자동으로 이메일 형식인지를 파악하여 형식에 맞지 않으면 경고 툴팁을 보여준다.

  <img src="https://velog.velcdn.com/images/wonder1247/post/70752240-e206-4651-a041-d99dc64c822b/image.png" width="600px">

  - input type="tel"
    형식은 판단하지 않으나 모바일의 경우 자동으로 숫자판을 띄워주기도 한다고 함.

  <img src="https://velog.velcdn.com/images/wonder1247/post/0a4c0b38-5582-4d1e-b418-861e86faa8fa/image.png" width="600px">

- #### input type(2) :: 날짜/숫자 입력

  - input type="number"

  <img src="https://velog.velcdn.com/images/wonder1247/post/829e38d2-5c89-4c54-b66d-1e8ba5600f07/image.png" width="600px">

  - input type="range"

  <img src="https://velog.velcdn.com/images/wonder1247/post/8e831661-232b-4d8e-ab7d-896a3907e75c/image.png" width="600px">

  - input type="date"

  <img src="https://velog.velcdn.com/images/wonder1247/post/a0480d9d-7f0d-401a-9bdf-2d8d70c397f0/image.png" width="600px">

  - input type="month / week"

  <img src="https://velog.velcdn.com/images/wonder1247/post/f8459601-16bc-45bd-92da-a51a2f12bbb6/image.png" width="600px">

  - input type="time"

  <img src="https://velog.velcdn.com/images/wonder1247/post/c64347f5-3482-4397-90f2-f58e4ca04e74/image.png" width="600px">

- ####

- ####

- ####

- ####

- ####

- ####

- ####

- ####

- ####

- ####

- ####

  <b></b>
  <br/>
