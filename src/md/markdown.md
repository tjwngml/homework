# 마크다운 문법

1. 마크다운이란 무엇일까?

- 마크다운(Markodown)은 웹 작성자를 위한 일반 텍스트 기반의 경량 마크업 언어이다.
<!-- 마크업 언어란 : <태그> 와 같은 기호를 사용해 문서나 데이터의 구조를
 명시하는 규칙들을 정의한 컴퓨터 언어의 일종이다. -->

주요 마크업 언어들에는 HTML, XML, SGML, 그리고 이 파일에서 서술하게 될 Markdown 등이 있는데,
앞서 언급한 경량 마크업 언어(Lightweight markup language)는 간결한 문법을 가진 마크업 언어라는 의미를 가지고 있다.

따라서 마크다운을 설명하는 수식만 보아도 알 수 있듯이, 마크다운은 일반 마크업 언어에 비해
! 문법이 쉽고 간단한 것이 특징이다. !

2. 마크다운의 탄생 !

- 마크다운은 존 그루버(John Gruber)가 에런 스워츠(Aaron Swartz)와 협력하여 2004년에 만들어졌다.
  존 그루버는 자신의 마크다운에 대한 소개 및 설치 방법 그리고 마크다운의 정의 및 목표, 개발 과정 및 감사 등이 담겨있는 마크다운 공식 사이트를 만들었다.
  마크다운 공식 사이트의 URL은 다음과 같다.

https://daringfireball.net/projects/markdown/

존 그루버의 마크다운 웹 사이트에서 ' 마크다운 서식 구문의 가장 중요한 설계 목표는 가능한 한 읽기 쉽게 만드는 것,
태그나 서식 지침으로 마크업된 것처럼 보이지 않으면서도, 일반 텍스트로 그대로 게시될 수 있어야.
여러 기존 텍스트-HTML 필터의 영향을 받았지만, 가장 큰 영감의 원천은 일반 텍스트 이메일 형식.'
이라는 내용을 보면 마크다운의 창시자인 존그루버가 왜 이 언어를 만들었는지, 그리고 마크업 언어에 대해 어떤 철학을 가지고 있는지를 확인할 수 있다.

3. 마크다운의 작동 원리 ?

- 우리가 마크다운으로 글을 작성할때, 텍스트는 지금 내가 글을 쓰고 있는 'markdown.md' 파일 처럼 .md 또는 .markdown 확장자를 가진
  일반 텍스트 파일에 저장된다. 그런데, 그 후에 마크다운 서식 파일은 어떻게 HTML이나 인쇄가 가능한 문서로 변환이 될 수 있을까?

간단히 말하자면 마크다운 파일을 처리할 수 있는 ' 마크다운 애플리케이션' 이 필요하다.
사용자가 왼쪽 창에 마크다운 문법으로 글을 쓰면, 오른쪽 창에 실시간으로 HTML로 변환된 결과물을 보여주는 'Dillinger'라는 이름의 애플리케이션 처럼,
마크다운 서식이 지정된 텍스트를 HTML로 변환하여 웹 브라우저에 표시될 수 있도록 하는 마크다운 애플리케이션을 필요로 한다.

마크다운 애플리케이션은 '마크다운 프로세서' 라는 것을 사용하여 마크다운으로 서식이 지정된 텍스트를 가져와 HTML 형식으로 출력한다.
이 시점에서 문서는 웹 브라우저에서 보거나 스타일 시트와 결합하여 인쇄할 수도 있다.

<!-- !주의! 마크다운 애플리케이션과 프로세서는 두개의 별개 구성 요소다 ! -->

이 과정을 4단계로 요약하자면 :

- 텍스트 편집기나 전용 마크다운 애플리케이션을 사용해 마크다운 파일을 만든다. 파일은 .md 또는 .markdown 확장자를 가져야 한다.
- 마크다운 애플리케이션에서 마크다운 파일을 연다.
- 마크다운 애플리케이션을 사용해 마크다운 파일을 HTML 문서로 변환한다.
- 웹 브라우저에서 HTML 파일을 보거나, 마크다운 애플리케이션을 사용하여 PDF와 같은 다른 파일 형식으로 변환한다

4. 마크다운의 문법

- 이제 마크다운의 개념에 대한 전반적인 감을 잡았으니, 마크다운의 문법에 대해 정리를 해 볼 차례이다.

지금까지는 마크다운으로 글을 작성하지 않았지만, 마크다운의 문법을 정리하기 위해 ctrl + shift + p 를 사용해 vscode 명령 팔레트에서 >Markdown Open Preview 창을 열어 왼쪽에는 markdown.md 파일을, 오른쪽 창에는 preview 창을 열고 실시간으로 마크다운이 어떻게 적용되는 지 확인할 것이다.

(1) 제목 (Headings)

- 제목을 만들기 위해서는 샵(#)을 제목으로 만들고 싶은 단어나 문장 앞에 붙이면 된다. 붙이게 되는 샵의 개수가 heading의 level을 결정한다.

예시:

# Heading level 1

## Heading level 2

### Heading level 3

#### Heading level 4

##### Heading level 5

###### Heading level 6

<!-- # Heading level 1 = <h1> Heading level 1 </h1> in HTML -->
<!-- ## Heading level 2 = <h2> Heading level 2 </h2> in HTML -->
<!-- ### Heading level 3 = <h3> Heading level 3 </h3> in HTML -->
<!-- #### Heading level 4 = <h4> Heading level 4 </h4> in HTML -->
<!-- ##### Heading level 5 = <h5> Heading level 5 </h5> in HTML -->
<!-- ###### Heading level 6 = <h6> Heading level 6 </h6> in HTML -->

number sign이 2개일때 까지는 밑 줄이 형성 됨을 확인할 수 있다.

- Alternate Syntax

Heading level 1 의 경우 샵(#)을 사용하지 않고
Heading 으로 만들고 싶은 단어나 문장 아래에 '=' 기호를 원하는 만큼 반복해서 추가하면, 해당 텍스트는 h1 태그가 적용된 1단계 제목이 된다.

Heading level 2 의 경우 level 1 과 방법은 동일하나, '=' 기호 대신 '-'
기호를 원하는 만큼 반복해서 추가하면 해당 텍스트는 h2 태그가 적용된
2단계 제목이 된다.

- 제목을 작성 할 때 유의사항

! 샵(#)과 제목 텍스트 사이에 공백을 두어야 한다. !

다양한 마크다운 애플리케이션에서 호환성 문제를 피하기 위해서는 샵 기호와 제목 텍스트 사이에 항상 공백을 넣는 것이 좋다.

! 제목 앞 뒤에 빈줄을 넣어라 !

제목 위 아래에는 빈 줄을 추가하는 것이 좋다.

(2) 문단 (Paragraphs)

- 하나 이상의 텍스트 줄을 빈 줄로 구분하면 새로운 문단이 생성된다.

예시:

첫 번째 문장입니다.

두 번째 문장입니다.

<!-- <p>첫 번째 문장입니다.</p> <p>두 번째 문장입니다.</p> in HTML -->

- 문단을 작성할 때 유의사항

목록에 속하지 않는 한, 문단을 공백이나 택으로 들여쓰기 하지 말 것.

모든 줄을 왼쪽으로 정렬해야 예상치 못한 서식 오류를 방지 할 수 있다.

(3) 줄 바꿈 (Line Breakes)

- 줄 끝에 두 개 이상의 공백을 추가한 다음 엔터키를 누르면 줄 바꿈이
  생성된다. 이렇게 하면 br 태그가 만들어져 한줄 아래로 내려간다.

예시:

이것은 첫 번째 줄입니다.  
이것은 두 번째 줄입니다.

- 줄 바꿈 작성시 유의 사항

줄 끝에 두 개 이상의 공백을 사용하는 방법은 대부분의 마크다운 애플리케이션에서 작동하지만, 편집기에서 공백이 잘 보이지 않아 br-HTML 태그를 사용하는 것이 더 명확하고 호환성이 좋다.

(4) 강조 (Emphasis)

- 강조는 텍스트를 굵게 또는 기울여서 표현하는 것이다.

(4-1) 굵게 (Bold)

- 단어나 문장 앞뒤에 별표 두 개 (\*\*) 또는 밑줄 두 개(\_\_)를 사용한다.

예시 : **bold text** 또는 **bold text**

(4-2) 기울임 (Italic)

- 단어나 구문 앞 뒤에 별표 한 개(\*) 또는 밑줄 한 개 (\_)를 사용한다.

예시 : _Italic_ 또는 _Italic_

- 유의 사항 : 단어 중간을 기울여 쓸 때는 **별표(\*)**를 사용하는 것이 더 높은 호환성을 보장한다.

(4-3) 굵게와 기울임 동시 사용

- 단어나 구문 앞뒤에 별표 세 개(\*\*\*) 또는 밑줄 세 개(\_\_\_)를 추가한다.

예시 : **_really important_** **_really important_**

(5) 인용문 (Blockquotes)

- 문단 앞에 > 기호를 추가한다

예시 :

> Dorothy followed her through many of the beautiful rooms in her castle.

- 인용문 작성 시 유의 사항

인용문 위 아래에 빈 줄을 추가해야 한다. 빈 줄이 없으면 제대로 표시되지 않을 수 있다.

(6) 목록 (List)

(6-1) 정렬된 목록 (Ordered Lists)

- 항목 앞에 **숫자.**를 붙여서 만든다. 이때, 숫자는 반드시 순서대로일 필요는 없으나 1로 시작하는 것이 좋다. 마크다운 프로세서가 자동으로 올바른 순서로 번호를 매겨주기 때문이다.

예시 :

1. First item
2. Second item
3. Third item
4. Fourth item

<!-- <ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ol> in HTML  -->

1. First item
1. Second item
1. Third item
1. Fourth item

<!-- <ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ol> in HTML  -->

1. First item
2. Second item
3. Third item
4. Fourth item

<!-- <ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ol> in HTML  -->

1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item

<!--<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item
    <ol>
      <li>Indented item</li>
      <li>Indented item</li>
    </ol>
  </li>
  <li>Fourth item</li>
</ol> in HTML  -->

- 들여쓰기를 위해 네 개의 공백이나 하나의 택을 사용한다.

(6-2) 비정렬된 목록(Unordered Lists)

- 항목 앞에 대시 -, 별표 \*, 또는 더하기 기호 +를 붙인다.

- 들여쓰기를 위해 네 개의 공백이나 하나의 탭을 사용한다.

- 만일 비정렬 목록 항목이 숫자와 마침표로 시작해야 할 경우, 마침표 앞에
  백슬래시 \를 넣어 이스케이프 처리해야 한다.

예시 :

- First item
- Second item
- Third item
- Fourth item

<!-- <ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ul> in HTML -->

- First item
- Second item
- Third item
- Fourth item

<!--<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ul> in HTML  -->

- First item
- Second item
- Third item
- Fourth item

<!--<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ul> in HTML  -->

- First item
- Second item
- Third item
  - Indented item
  - Indented item
- Fourth item

<!--<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item
    <ul>
      <li>Indented item</li>
      <li>Indented item</li>
    </ul>
  </li>
  <li>Fourth item</li>
</ul> in HTML  -->

(7) 목록에 다른 요소 추가하기

- 목록의 연속성을 유지하면서 다른 요소를 추가하려면, 해당 요소(예: 문단, 인용문 등)를 네 개의 공백 또는 하나의 탭으로 들여쓰기해야 한다.

(7-1) 문단 추가

- 두 번째 목록 항목 아래에 빈 줄을 두고 네 개의 공백으로 들여쓰기한 다음 문단을 작성한다.

예시 :

- This is the first list item.
- Here's the second list item.

  I need to add another paragraph below the second list item.

- And here's the third list item.

(7-2) 인용문 추가

- 네 개의 공백으로 들여쓰기하여 인용문을 추가한다.

예시 :

- This is the first list item.
- Here's the second list item.

  > A blockquote would look great below the second list item.

- And here's the third list item.

(7-3) 코드 블록 추가

- 일반적인 코드 블록은 네 개의 공백 또는 한 개의 탭으로 들여쓰기하지만 목록 안에 코드를 넣을 때는 여덟 개의 공백 또는 두 개의 탭으로 들여쓰기해야 한다.

예시 :

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
    The rendered output looks like this:

Open the file.
Find the following code block on line 21:

 <html>
   <head>
     <title>Test</title>
   </head>
Update the title to match the name of your website.

(7-4) 목록 추가

- 정렬된 목록 안에 비정렬된 목록을 넣거나, 비정렬된 목록 안에 정렬된 목록을 넣을 수 있다.

- 이때도 중첩된 목록은 들여쓰기(4칸 공백 또는 1 탭)를 해야 한다.

예시 :

1. First item
2. Second item
3. Third item
   - Indented item
   - Indented item
4. Fourth item

(8) 코드 (Code)

- 단어나 문장을 코드로 표시하려면, 백틱(`)으로 감싸면 된다.

예시 : At the command prompt, type `nano`.

<!-- At the command prompt, type <code>nano</code>. in HTML -->

(9) 백틱 이스케이프

- 코드로 표시하려는 단어나 문장에 하나 이상의 백틱이 포함된 경우, 이 단어 또는 문장을 이중 백틱(``)으로 감싸서 이스케이프 처리할 수 있다.

예시 : ``Use `code` in your Markdown file.``

<!-- <code>Use `code` in your Markdown file.</code> in HTML -->

(10) 코드 블록 (Code Block)

- 코드 블록을 만드려면, 블록의 모든 줄을 최소 네 개의 공백 또는 하나의 탭으로 들여쓰기 하면 된다.

참고 ! 줄을 들여쓰기 하지 않고 코드 블록을 만드려면, 펜스 코드 블록(fenced code blocks)을 사용하면 된다.!

(11) 가로선 (Horizontal Rules)

- 가로선을 만들려면, 한 줄에 세 개 이상의 별표(\*\*\*), 대시(---), 또는 밑줄(\_\_\_)만 사용하면 된다.

예시 :

---

---

---

가로선 사용 시 유의 사항 : 호환성을 위해, 가로선 앞 뒤에 빈 줄을 넣어라.
빈 줄이 없으면, 이는 제목으로 처리될 수 있다.

예시 :

- 올바른 예 :

Try to put a blank line before...

---

...and after a horizontal rule.

- 잘못된 예:

## Without blank lines, this would be a heading.

Don't do this!

(12) 링크 (Links)

- 링크를 만들려면, 링크 텍스트를 대괄호([])로 감싸고, 그 뒤에 바로 URL을 괄호(())로 감싸서 붙이면 된다.

예시 :

y favorite search engine is [Duck Duck Go](https://duckduckgo.com).

(13) 제목 추가하기

- 선택적으로 링크에 제목을 추가할 수 있다.
  사용자가 링크에 마우스를 올렸을 때, 툴팁으로 나타나게 되는데, 제목을 추가하려면 URL 뒤에 따옴표로 감싸서 넣으면 된다.

예시 :

[구글](https://www.google.com '구글 홈페이지로 이동합니다')

- URL이나 이메일 주소를 빠르게 링크로 바꾸려면 , 꺾쇠괄호(<>)로 감싼다.

- 링크를 강조하려면, 대괄호와 괄호 앞뒤에 별표를 추가하면 된다. 링크를 코드로 표시하려면, 대괄호 안에 백틱을 추가한다.

(14) 링크 포맷팅 (Formatting Links)

- 대괄호 [] 안에 링크 텍스트를 넣고, 바로 뒤에 소괄호 () 안에 URL을 넣는다.

1. 강조된 링크: 링크를 강조하고 싶을 때 대괄호와 소괄호 양쪽에 별표(\*)를 추가하여 기울임꼴이나 굵은 글씨로 만들 수 있다.

예시:

*[Markdown Guide](https://www.markdownguide.org)*는 Markdown Guide처럼 보인다.

2. 코드 링크: 링크 텍스트를 코드로 표시하고 싶을 때, 대괄호 안에 백틱(`)으로 감싸면 된다.

예시:

[`code`](#code)는 code처럼 보인다.

(15) 참조 스타일 링크 (Reference-style Links)

(15-1) 링크 텍스트 부분

- 본문에서 실제로 보일 텍스트를 나타낸다.

- 두 쌍의 대괄호로 구성된다.

- 첫 번째 대괄호 [] 안에는 링크 텍스트를 넣는다.

- 두 번째 대괄호 [] 안에는 다른 곳에 저장해둔 참조 레이블(label)을 넣는다. 이 레이블은 대소문자를 구분하지 않으며 숫자, 글자, 공백, 구두점 등을 포함할 수 있다.

- 두 대괄호 사이에 공백을 넣어도 되고 생략해도 된다.

예시:

[hobbit-hole][1] 또는 [hobbit-hole] [1]

(15-2) 참조 정의 부분

- 링크의 실제 URL과 제목을 정의하는 부분이다.

- 형식: [레이블]: URL "선택적 제목"

- 레이블: 대괄호 [] 안에 레이블을 넣고 바로 뒤에 콜론(:)과 하나 이상의 공백을 쓴다.

- URL: 링크 주소를 입력하며 꺾쇠괄호(< >)로 감싸도 된다.

- 제목(선택 사항): 마우스를 올렸을 때 나타나는 툴팁(tooltip)으로 이중 따옴표, 작은따옴표, 또는 괄호 안에 넣을 수 있다.

- 이 정의 부분은 문서의 아무 곳에나 배치할 수 있다. 보통은 해당 링크가 있는 문단 바로 아래에 두거나, 문서 맨 끝에 모아둔다.

예시 :

[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'

(16) 이스케이프할 수 있는 문자들 (Characters You Can Escape)

- 마크다운에서 특별한 의미를 가지는 문자들을 일반 텍스트로 사용하고 싶을 때 해당 문자 앞에 백슬래시()를 붙여서 그 특별한 기능을 무효화시킬 수 있다.

- 이스케이프(escape)할 수 있는 문자들: 백슬래시(\), 백틱(`), 별표(\*), 밑줄(\_), 중괄호({ }), 대괄호([ ]), 꺾쇠괄호(< >), 괄호(( )), 샵 기호(#), 더하기 기호(+), 빼기 기호(-), 마침표(.), 느낌표(!), 수직선(|)

5. 마크다운 실습

- 이렇게 마크다운 문법을 살펴보았으니, 조지 오웰의 소설《1984》의 일부를 발췌하여 마크다운 실습에 인용하고자 한다.

<br>

<!-- 저작자 : 조지 오웰(George Orwell)
             작품 명: 《1984》
             출판연도 : 1949년

  조지 오웰은 1950년 사망하였다. 대부분의 국가에서 저작권은 저작자 사후 70년간 보호되므로,《1984》는 2021년 1월 1일 이후부터 공공 영역 (Public Domain)에 속하게 되었다. 따라서 저작권 보호 기간이 만료되어 자유로이 이용할 수 있다.

   -->

---

# 1984 - 조지 오웰 (George Orwell)

_윈스턴_ 은 텔레스크린에 등을 돌렸다. 그게 더 안전하긴 했지만, 그는 등을 보이면 들통날 수 있다는 걸 잘 알고 있었다. 1킬로미터 떨어진 곳에 그의 사무실인 진실부가 지저분한 풍경 위로 거대하고 하얗게 우뚝 솟아 있었다. 그는 왠지 모르게 **_혐오감_**을 느꼈다. 이곳은 오세아니아에서 세 번째로 인구가 많은 **_'에어스트립 원'_** 의 중심지, 런던이었다.

그는 런던이 원래부터 이런 모습이었는지 떠올리려 애썼다. 썩어가는 19세기 집들이 항상 있었던 걸까? 옆면은 나무로 덧대어져 있고, 창문은 판지로, 지붕은 골함석으로, 정원 벽은 사방으로 축 늘어져 있었다. 폭탄에 무너진 곳에서 석고 가루가 공중에 흩날리고 버드나무가 잔해 더미 위로 흩날리는 모습도. 폭탄이 넓은 지역을 휩쓸고 지나간 자리에 닭장 같은 초라한 목조 가옥들이 솟아오른 곳은? 하지만 소용없었다. **그는 기억할 수 없었다.** 어린 시절의 기억이라곤 배경 없이, 대부분 알아볼 수 없는 밝은 조명의 풍경화뿐이었다.

**진실부(Ministry of Truth)**— _신어(Newspeak)_ 로는 미니트루라고 불렸다. _[신어는 오세아니아의 공식 언어였다. 그 구조와 어원에 대한 설명은 부록을 참조하라.]_ —는 눈에 보이는 다른 어떤 것과도 놀라울 정도로 달랐다. 반짝이는 하얀 콘크리트로 이루어진 거대한 피라미드형 구조물이 층층이 300미터 상공으로 솟아 있었다. 윈스턴이 서 있는 곳에서는 하얀 표면에 우아한 글씨로 적힌 당의 세 가지 슬로건을 겨우 읽을 수 있었다.

> 전쟁은 평화이고
> 자유는 노예이고
> 무지는 힘이다

---

진실부는 지상 3천 개의 방과 그에 상응하는 지하 분지로 구성되어 있다고 전해졌다. 런던 곳곳에는 비슷한 외관과 크기를 가진 건물이 세 채 더 있었다. 그 건물들은 주변 건축물을 완전히 압도해서 '빅토리 맨션' 옥상에서 네 채를 동시에 볼 수 있었다. 이 건물들은 정부 기관 전체를 담당하는 네 개의 부처를 맡고 있었다. 진실부는 뉴스, 오락, 교육, 미술을 담당했다. 평화부는 전쟁을 담당했다. 사랑부는 법과 질서를 유지했다. 그리고 풍요부는 경제를 담당했다. 이 건물들의 이름은 신어로 각각 **미니트루(Minitrue)** , **미니팍스(Minypax)**, **미니러브(Miniluv)**, **미니플렌티(Miniplenty)** 였다.

**사랑부는 정말 무서웠다.** 창문이 하나도 없었지. 윈스턴은 사랑부 안에 들어가 본 적도, 500미터 안에 들어가 본 적도 없었다. 공무상 방문이 아니면 들어갈 수 없는 곳이었고, 그것도 철조망과 철문, 그리고 숨겨진 기관총 소굴로 이루어진 미로를 뚫고 들어가야만 가능했다. 심지어 외곽 경계로 이어지는 길에도 검은 제복을 입고 관절 곤봉으로 무장한 고릴라 얼굴 경비병들이 순찰하고 있었다.

---

### 중략 ...

*윈스턴*은 자신이 펼친 네 장의 종이 조각을 살펴보았다. 각 종이 조각에는 한두 줄 정도의 메시지가 담겨 있었는데, 약어로 되어 있었다. 사실 신어는 아니지만 대부분 신어 단어로 이루어져 있었는데, 이는 내각에서 내부 목적으로 사용하는 것이었다. 내용은 다음과 같았다.

      - 17.3.84 bb 연설이 잘못 보고된 아프리카 정정

      - 19.12.83 예측 3년 4분기 83 오타 확인 현재 문제

      - 14.2.84번 미니플렌티 잘못된 인용 초콜릿 수정

      - 3.12.83 빅브라더의 일일 지시 보고서, 이중으로 좋지 않음, 비인간화된 사람들을 참조하여, 완전히 재작성하여 서류 제출 전에 상급자에게 제출할 것.

*윈스턴*은 **희미한 만족감**을 느끼며 네 번째 메시지를 옆으로 치웠다. 복잡하고 책임감 있는 일이라 마지막에 처리하는 게 나았다. 나머지 세 가지는 일상적인 일이었지만, 두 번째는 아마 숫자 목록을 훑어보는 지루한 일이었을 것이다.

---

원문 링크 : _[1984- 조지오웰, 구텐베르크 도서관](https://gutenberg.net.au/ebooks01/0100021h.html '1984 원문 보기')_
