# 장점

- 내부 로직은 비효율적이지만 개발 속도는 빠름
- jQuery는 상당히 단순한 JavaScript programming 입니다.  또한 간결하게 코딩하고
   많은 일을 해주는 JavaScript Library 입니다.
- CSS의 selecter를 사용하고 있어서 습득하기 쉬우며,  브러우저의 다양성을 처리해
  줌으로  호환성 처리에 시간을 소비할 필요가 없습니다. 
- 복잡한 Javascript의 구현시 DOM 문법을 매우 간결하게 해주어 개발 속도를  향상
  할 수 있습니다.
- jQuery의 기능을 확장할 수 있는 plugin 구조를 지원합니다.
- Ajax를 지원해 줍니다. 
- 참고사이트 : https://api.jquery.com/

# 코드(자세한 코드는 lecture에서 확인)

### [lecture 사이트](http://lectureblue.pe.kr/index.jsp)

vs code에서 !!두개 치고 기본틀 작성

- **$( "#prev ~ div" ).css( "border", "3px groove blue" );** : "prev" 요소 다음에 오는 모든 "div" 요소를 선택

- **$( "input:not(:checked) + span" ).css( "background-color", "yellow" );** : "input"이 체크되어있지 않은 모든 요소 선택, 배경 노란색으로 변경

- **$( "td:empty" )**

   **.text( "Was empty!" )**

  **.css( "background", "rgb(255,220,200)" );** : 자식태그 혹은 text nodes 를 포함하지 않는 태그 선택후, 텍스트 채워넣고 배경색 변경

- **$( "ul li:nth-child(2)" ).append( "<span> - 2nd!</span>" );** : ui의 li태그들중 2번째 li 태그 선택 후, 문자 추가
- **$( "ul li" ).eq(2).append( "<span> - 3nd!</span>" );** :  ui의 li태그들중 2번째 li 태그 선택 후, 문자 추가
- **$( "div span:last-child" )** :  자식태그들 중에 마자막 자식태그
- **$( "div button:only-child" )** : 부모의 자식이 하나인 태그 



### Attribute 

- **$("[id]").css("color","red");** : id 속성을 가진 태그

- **$( "input[value='Hot Fuzz']" ).next().text( "Hot Fuzz" );** : input태그의 value값이 Hot Fuzz인 태그

- **$( "input[name!='newsletter']" ).next().append( "<b>; not newsletter</b>" );** : input태그의 name이 newsletter가 아닌 태그

- **$("[title^='f']").css("color","red");** : title의 이름이 f로 시작하는 태그

- **$( "input[name$='letter']" ).val( "a letter" );** : input 태그의 name이 letter로 끝나는 태그의 value 값을 a letter로 바꿈

- **$( "input[name*='man']" ).val( "has man in it!" );** :  input 태그의 name이 man을 포함하는 태그

- **$( "input[name~='man']" ).val( "mr. man is in it!" );** : 공백으로 구분된 주어진 단어를 포함하는 값으로 지정된 속성이 있는 요소를 선택

  ```
  <input name="man-news">
  <input name="milk man">
  <input name="letterman2">
  <input name="newmilk">
  ```

- **$( "a[hreflang |= 'en']" ).css( "border", "3px dotted green" );** : 값이 주어진 문자열과 같거나 해당 문자열로 시작하여 하이픈(-)이 오는 지정된 속성이
   있는 요소를 선택한다.

  ```<a href="example.html" hreflang="en">Some text</a>
  <a href="example.html" hreflang="en">Some text</a>
  <a href="example.html" hreflang="en-UK">Some other text</a>
  <a href="example.html" hreflang="english">will not be outlined</a>
  ```

  

### JQuery 필터

- **$( "ul li" ).first().addClass( "highlight" );** : 일치하는 요소 집합을 집합의 첫 번째 요소로 줄인다.
   인수가 없는 함수이다. 거기에 highlight라는 클래스 추가

- **$( "ul li" ).even().addClass( "highlight2" );** : 일치하는 요소 집합을 0부터 번호가 지정된 집합의 짝수로 줄인다.

- **$( "ul li" ).odd().addClass( "highlight" );** : 일치하는 요소 집합을 0부터 번호가 지정된 집합의 홀수로 줄인다.

- **$( "body" ).find( "div" ).eq(2 ).addClass("blue");** : 3번 태그 선택

- **$( "body" ).find( "div" ).slice( 0, 2 ).css("background" ,"yellow" );** : 0~1번 태그 선택

- **$( "body" ).find( "div" ).slice( 3 ).css("background" ,"orange" );** : 3번태그부터 끝까지 선택

- **$( ":header" ).css({ background: "#ccc", color: "blue" });** : h1 ~ h6까지의 heading태그

- **$( "div:contains('John')" ).css( "text-decoration", "underline" );**  : 특정 text를 포함하고 있는 태그

- **$( "div:has(p)" ).addClass( "test" );** : 특정 태그를 포함하고 있는 태그 

- **$( "td:parent" ).fadeTo( 1500, 0.3 );** : 하나 이상의 자식 노드(요소 또는 텍스트)가 있는 모든 요소를 선택한다.(fadeTo는 흐려지는 효과)

   

### JQuery 명령어

**(1) 텍스트 변경과 가져오기**  

 \- text(...) / text() / text(function)

**(2) HTML 변경과 취득**

 \- html(...) / html() / html(funtion) 

**(3) HTML 삽입**

\- prepend(...)/append(...)  : 태그 안의 맨앞/맨뒤에 HTML을 삽입함

\- before(...)/after(...)   : 태그 밖의 앞/뒤에 HTML을 삽입함
\- p 태그는 앞뒤로 한줄의 공간을 가진다.

**(4) HTML 이동**

 \- prependTo()/appendTo(...) 
 \- $( "span" ).prependTo( "#foo" );
  : 'span' 를 #foo요소 안의 앞으로 이동
 \- $( "span" ).appendTo( "#foo2" );
  : 'span' 를 #foo2요소 안의 뒤로 이동

**(5) 다른 태그로 묶음**

 \- .wrap('<div></div>') ; 각 요소를 <div></div> 태그로 각각 감싼다.
 \- .wrapAl('<div></div>')   ; 요소 전체를 <div></div> 태그로 한번에 감싼다.

 \- .wrapInner(.'<b></b>')  ; 자식 요소 각각을 <b></b> 태그로 각각 감싼다.

**(6) 태그변경/제거**

\- $( this ).replaceWith( "<div>" + $( this ).text() + "</div>" );
  this 요소를 "<div>" + $( this ).text() + "</div>" 로 바꾼다.

\- .remove() : 태그를 제거

**(7) 속성값 변경과 취득**

 \- attr(...,...)  : 지정한 속성값 변경

 \- attr(...)    : 지정한 속성값 가져옴

 \- removeAttr(...) : 지정한 속성값 제거

**(8) class속성 추가/제거**

 \- addClass(...)   : class 속성 추가

 \- removeClass(...) : class 속성 제거

**(9) css 제어**

 \- css(...,...)   : 지정한 CSS 속성값 설정

 \- css(..)    : 지정한 CSS 속성값 가져옴



### JQuery 이벤트

**1.이벤트가 발생한 태그 얻기**

   - $(function(){........})  : 아래 명령어의 생략형

   - $(document).ready(function()(......)  : 웹 페이지를 모두 읽어드리고, 준비가 되었다는 뜻



**2. toggle()**

  \- 일치하는 요소를 표시하거나 숨긴다.

 

**3. unbind()**
\- 요소에서 이전에 연결된 이벤트 핸들러 제거



**4. on**
 \- 하나 이상의 이벤트에 대한 이벤트 핸들러 함수를 선택한 요소에 연결한다..