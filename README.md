# web
<pre>
HTML의 문법

1. 요소(Element)
	- HTML 요소는 시작태그와 종료태그 그리고 태그 사이의 content로 구성된다.
		<p>안녕하세요</p>
		* <p> : 시작태그
		* </p> : 종료태그
		* 안녕하세요 : 컨텐츠
	- 태그명은 소문자로 작성한다.
	- 태그에서 <p>의 "<p"는 공백없이 적는다. </p>에서 "</p"는 공백없이 적는다.
	- 요소는 중첩될 수 있다.
		* 요소는 다른 요소를 포함할 수 있다.
		* 요소가 다른 요소를 포함하면 부모-자식 관계가 성립된다.
		* 다른 요소에 포함된 요소는 가독성을 위해서 들여쓰기 한다.
			<body>
				<h1>연습</h1>
				<p>html 태그 연습입니다</p>
			</body> 
			* body는 h1과 p의 부모 요소다.
			* h1과 p는 형제 요소다.
	- 컨텐츠를 포함하지 못하는 요소가 있다.
		* meta, link, img, input, br, hr는 컨텐츠를 포함하지 못하는 요소다.
		* <meta></meta>, <input></input>와 같이 작성하지 않는다.
		* 일반적인 작성법
			* 컨텐츠없이 시작 요소만 작성해도 된다.
			<meta> 
			<input>
			* Self-Closing 요소의 형태로 작성해도 된다.
			<input />
			<br />

2. 속성(Attribute)
	- 속성의 요소(엘리먼트)의 성질, 특징을 정의하는 명세다.
		<img src="sample.png" width="100" height="60" alt="샘플 사진"/>
		* 속성은 시작 태그에 위치한다.
		* 속성은 속성명과 속성값으로 구성된다.	
			속성명	속성값
			src		sample.png
			width	100
			height	60
			alt 	샘플사진
- 모든 요소(엘리먼트)는 속성을 가질 수 있으며, 속성은 요소에 추가적인 정보를 제공한다.
		<input type="text" name="username" value="홍길동" />
		<img src="sample.png" width="100" height="60" alt="샘플 사진"/>
		<a href="home.html">홈</a>

		* 속성명과 속성명을 정의할 때는 속성명="속성값" 혹은 속성명='속성값'의 형식으로 작성할 수 있다.
		* 속성명과 속성값 사이에 공백을 추가하지 않는다.
		* 속성값은 반드시 쌍타옴표나 홑따옴표로 감싼다.
		* 속성을 작성하는 정해진 순서는 존재하지 않는다.
		* 요소에 속성을 중복해서 정의할 수 없다.
		* 어떤 속성은 속성값에 사용할 수 있는 값이 미리 정해져 있기도 하다.
			<input type="속성값" />
			* input요소의 type 속성의 속성값은 text, password, radio,... 중에서 하나다.
		* 어떤 속성은 기본값이 지정되어 있다.		
			<input type="속성값">
			* input요소의 type 속성의 기본값은 text다.
	
	- 글로벌 속성(HTML Global Attribute)
		* 글로벌 속성은 모든 HTML 요소가 공통으로 사용할 수 있는 속성이다.
		* 자주 사용되는 글로벌 속성
			속성명			설명
			--------------------------------------------------------------------------
			id				요소에 유일한 식별자를 지정한다.
			class			스타일시트에 정의된 class를 요소에 지정한다. 중복지정이 가능하다.
			style			요소에 스타일을 지정한다.
			tabindex		사용자가 키보로 페이지를 내비케이션할 때 이동 순서를 지정한다.
			title			요소에 대한 제목(풍선도움말)을 지정한다.
			---------------------------------------------------------------------------

 3. HTML Basic 태그
	<!doctype> 태그
		문서형식정의 태그다.
		출력할 웹 페이지의 형식을 웹 브라우저에게 전달한다.
		<!doctype html>
			html5 문서형식이다.
		<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
			html4 문서형식이다.
		<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
			xhtml 문서형식이다.

	<html> 태그
		모든 html 태그의 부모태그다.
		웹 페이지에 단 하나만 존재한다.
		모든 태그는 html 태그 내부에 기술한다.
		주요 속성
			<html lang="ko">
				한국어를 사용하는 경우 ko로 설정한다.

	<head> 태그
	 	메타 데이터를 요소를 포함하는 태그다.
		title, style, link, script에 대한 데이터를 포함한다.
		화면에 표시되지 않는다.

	<title> 태그
		웹브라우저의 탭에 표시될 제목을 지정한다.

	<meta> 태그
		브라우저, 검색엔진에서 참조하는 메타데이터를 정의한다.
		<meta charset="utf-8">
			브라우저가 사용하는 문자세트를 지정한다.
		<meta name="keywords" content="강의, 웹강의, 웹개발강의">
			검색엔진을 위한 키워드를 정의한다.
		<meta http-equiv="refresh" content="30">
			웹페이지를 30초마다 refresh한다
		<meta name="viewport" content="width=device-width, initial-scale=1">
			뷰포트의 너비를 장치의 너비로 지정한다.
			모든 장치에서 올바른 렌더링 및 터치 확대 조절을 보장받을 수 있다.
	
	<body>  태그
		웹브라우저에 실제로 출력되는 요소를 포함한다.

4. HTML Text 태그
	제목 (Headings) 태그
		문서의 제목을 컨텐츠로 포함하는 태그다.
		h1 ~ h6까지의 태그가 있다.
		h1이 가장 중요한 제목을 의미하고, 나머지 태그들은 각각 부제목, 소제목.... 을 의미한다.
		제목 이외에는 사용하지 않는 것이 좋다.

	본문 내용 혹은 단락 (Paragraphs) 태그
		문서의 본문 내용을 포함하는 태그다.
		p 태그가 있다.
		뉴스의 내용, 상품의 설명, 책의 줄거리, 게시글의 내용, 답글의 내용 등을 포함할 수 있다.
		태그 안에서 입력한 줄바꿈은 화면에 표시되지 않는다.
		태그 안에서 입력한 공백은 한 칸만 표시한다.

	개행(line break) 태그
		텍스트에 줄바꿈을 적용시키는 태그다.
		br 태그가 있다.
		br은 empty 태그다.
	
	공백문자
		&nbsp; 엔티티 코드는 공백을 추가한다.

		* 엔티티 코드(Entity Code)
			- 엔티티 코드는 HTML 문서에서 특수 문자를 입력하기 위해서 사용하는 코드다.
			- 많이 사용되는 엔티티 코드
				----------------------------------------------------------------
				엔티티	문자식 표현(Entity Code)		숫자식 표현(Entity Number)
				----------------------------------------------------------------
				<		&lt;						&#60;
				>		&gt;						&#62;
				"		&quot;					&#34;
				'		&apos;					&#39;
				&		&amp;					&#38;
				공백		&nbsp;					&#160;
				-----------------------------------------------------------------

			
	pre (Preformatted) 태그
		형식화된 텍스트를 포함하는 태그다.
		pre 태그가 있다.
		pre 태그내의 컨텐츠는 작성한 그래도 브라우저에 출력된다.

	hr 태그
		수평주를 추가한다.

	q 태그
		짧은 인용문(quotation)을 포함하는 태그다.

	blockquote 태그
		긴 인용문을 포함하는 태그다.

	포맷팅 (Text formatting) 태그
		strong 태그
			중요한 텍스트를 포함하는 태그다.
		em 태그
			강조할 내용을 포함하는 태그다.
		small 태그
			small text를 포함하는 태그다.
		mark 태그
			highlighted text를 포함하는 태그다.
		del 태그
			deleted  text 를 포함하는 태그다.
		ins 태그
			inserted text를 포함하는 태그다.
		sub/sup 태그
			아랫첨자/위첨자를 포함하는 태그다.

5. 링크 태그
	지정된 경로로 이동시키는 태그다.
	a 태그가 있다.
	주요 속성
		href
			이동하고자 하는 페이지의 위치(경로)를 지정한다.
			경로를 지정하는 방법
				절대경로
					- http://로 시작하는 주소
					- "/"로 시작하는 주소
					<a href="http://www.daum.net">다음</a>
					<a href="/home">홈</a>
					
				상대경로
					- "/"로 시작하지 않는 주소
					<a href="about">도움말</a>
					<a href="../home">홈</a>

				페이지내의 요소
					- 페이지내의 특정 id를 가진 요소와 연결된 링크
					- "#아이디"의 형식이다.
					<a href="#top">맨 꼭대기로</a>
		target
			링크를 클릭했을 때 해당 페이지를 표시할 대상을 지정한다.
			target의 속성값은 "_self", "_blank"가 있다. 지정하지 않으면 "_self"가 기본값이다.

			target="_self"		- 링크를 클릭했을 때 연결된 페이지를 현재 윈도우에 표시한다.
			target="_blank"	- 링크를 클릭했을 댕 연결된 페이지를 새로운 윈도우에 표시한다.
		title
			풍선도움말을 지정한다.

6. 리스트 태그
	순서없는 목록(Unrodered List)
		ul태그와 li태그를 사용하면 순서없는 목록을 정의할 수 있다.
		ul태그는 순서없는 목록을 정의한다.
		ul태그는 li태그를 자식요소로 여러 개 포함할 수 있다.
		ul태그와 li태그 사이에는 어떤 태그도 위치할 수 없다.
		li태그는 컨텐츠 혹은 다른 다른 태그를 포함할 수 있다.
		내비게이션의 매뉴들, 상품 리스트, 뉴스 목록, 카테고리 리스트 순서없는 목록으로 정의되는 컨텐츠

		<ul>
			<li>커피</li>
			<li>콜라</li>
			<li>사이다</li>
			<li>주스</li> 
		</ul>

		<ul>
			<li><a href="http://www.daum.net">다음</a></li>
			<li><a href="http://google.com">구글</a></li>
			<li><a href="http://www.naver.com">네이버</a></li>
 
		</ul>

		<ul>
			<li></li>
			<p></p>		<- 유효한 HTML 문서가 아니다.
		<ul>

	순서있는 목록(Ordered List)
		ol태그와 li태그를 사용하면 순서있는 목록을 정의할 수 있다.
		베스트셀러 도서목록, 영화 예매 순위, 프로축구 팀순위 순서있는 목록으로 정의되는 컨텐츠

		

		

		<h3>영화 예매 순위</h3>

		<ol>

			<li>가디언즈 오브 갤럭시</li>

			<li>분노의 질주</la>

			<li>드림</li>

			<li>스즈메의 문단속</li>

		<ol>



	정의 목록(description List)

		dl태그, dt태그, dd태그를 사용하면 정의 목록을 정의할 수 있다.

		dl태그는 정의 목록을 정의한다.

		dl태그는 하나 이상의 dt와 dd태그를 포함한다.

		dt태그 항목명을 정의하고, dd태그의 항목의 데이터를 정의한다.

		영화정보, 도서정보, 사원정보 등을 항목과 함께 정의할 때 사용할 수 있다.		



		<dl>

			<dt>제목</dt>

			<dd>가디언즈 오브 갤럭시:Volume 3</dd>



			<dt>감독</dt>

			<dd>제임스 건</dd>



			<dt>주연</dt>

			<dd>크리스 프랫</dd>

			<dd>조 샐다나</dd>

			<dd>데이브 바티스타/dd>

			<dd>빈 디젤</dd>

			<dd>카렌 길런</dd>

			<dd>폼 크레멘티프</dd>			

		</dl>


7. 테이블 태그

	표를 작성하는 태그다.



	table 태그는 표를 정의하는 태그다.

	thead 태그는 표의 헤더부를 정의하는 태그다.

	tbody 태그는 표의 바디부를 정의하는 태그다.

	tfoot 태그는 표의 푸터부를 정의하는 태그다.

	tr 태그는 표의 행을 정의하는 태그다.

	th 태그는 제목 셀을 정의하는 태그다.

	td 태그는 데이터 셀을 정의하는 태그다.

	* table은 thead, tbody, tfoot를 포함할 수 있다.

	* table은 tr을 포함할 수 있다.

	* thead, tbody, tfoot는 tr을 포함할 수 있다.

	* tr은 th나 td를 포함할 수 있다.

	* th와 td만 컨텐츠를 포함할 수 있다.



	thead tr { ... }

	tbody tr { ... }



	<table>

		<thead>

			<tr>

				<th>제목1</th><th>제목2</th><th>제목3</th>

			</tr>

		</thead>

		<tbody>

			<tr>

				<td>컨텐츠1</td><td>컨텐츠2</td><td>컨텐츠3</td>

			</tr>

			<tr>

				<td>컨텐츠4</td><td>컨텐츠5</td><td>컨텐츠6</td>

			</tr>

			<tr>

				<td>컨텐츠7</td><td>컨텐츠8</td><td>컨텐츠9</td>

			</tr>

		</tbody>

		<tfoot>

			<tr>

				<td>컨텐츠10</td><td>컨텐츠11</td><td>컨텐츠12</td>

			</tr>

			<tr>

				<td>컨텐츠13</td><td>컨텐츠14</td><td>컨텐츠15</td>

			</tr>

		</tfoot>

	</table>



	th와 td의 주요 속성

		colspan

			해당 셀이 점유하는 열(가로방향 셀)의 수를 지정한다.

		rowspan

			해당 셀이 점유하는 행(세로방향 셀)의 수를 지정한다.
      
8. 폼과 폼 요소
	폼 태그
		사용자가 입력한 데이터를 수집하고, 서버 전송하기 위해서 사용되는 태그다.
		form 태그가 있다.
		form 태그는 다양한 입력 양식 태그를 포함할 수 있다.
			* 입력양식 태그 : input, textarea, select, checkbox, radio, button
		주요 속성
			method
				사용자가 입력한 데이터를 서버로 전송하는 방식을 지정한다.
				지정하지 않으면 method="GET"이 기본값이다.
				<form method="GET"> 
					폼이 수집한 입력데이터가 요청 메세지의 헤더부의 요청 URL 뒤에 포함되어 서버로 전송된다.
				<form method="POST">
					폼이 수집한 입력데이터가 요청 메세지의 바디부에 포함되어 서버로 전송된다.
			action
				폼이 수집한 입력값이 전송될 서버의 URL을 지정한다.
				필수 속성값이다.
				<form method="GET" action="login.jsp">
			enctype
				폼이 수집한 입력값의 인코딩방식을 지정한다.
				지정하지 않으면 enctype="application/x-www-form-urlencoded"이 기본값이다.
				<form enctype="application/x-www-form-urlencoded">
					폼이 수집한 값이 name=value&name=value&name=value의 형식으로 변환되어 서버로 전송된다.
					첨부파일을 전송할 수 없다.
				<form method="POST" enctype="multipart/form-data">
					폼이 수집한 입력값과 첨부파일을 서버로 전송할 때 사용하는 인코딩 방식이다.
					첨부파일 업로드가 없는 경우에는 지정하지 않는다.
	input 태그
		사용자로부터 데이터를 입력받기 위해서 사용된다.
		input 태그가 있다.
		input 태그의 type 속성값에 따라서 다양한 종류의 입력필드를 정의할 수 있다.
		주요 속성
			type
				입력필드의 타입의 지정한다.
				type속성을 지정하지 않으면 기본값은 type="text"다.
				<input type="text" />
					텍스트 입력필드
				<input type="password" />
					비밀번호 입력필드
				<input type="checkbox" />
					복수개 체크가 가능한 체그박스
				<input type="radio" />
					하나만 선택가능한 라디오버튼	
				<input type="date" />
					날짜 입력필드
				<input type="datetime" />
					날짜와 시간 입력필드
				<input type="file" />
					첨부파일 등록 필드
				<input type="number" />
					숫자 입력 필드
				<input type="reset" />
					폼 입력값을 초기화하는 버튼
				<input type="submit" />
					폼 입력값을 서버로 전송시키는 버튼
				<input type="hidden" />
					숨김필드
				<input type="email" />
					이메일 입력필드
				<input type="url" /> 
					url 입력필드
			value
				입력필드의 값을 지정한다.
				체크박스, 라디오버튼은 value 속성으로 값을 미리 지정해야 한다.
				첨부파일 필드는 value 속성으로 값을 지정할 수 없다.
				<input type="text" name="username" value="홍길동" />

				<input type="radio" name="gender" value="male" /> 남자
				<input type="radio" name="gender" value="female" /> 여자
			name
				입력필드의 값이 서버로 전송될 때 값의 이름을 지정한다.
				입력필드에서 name 속성은 꼭 설정해야되는 속성값이다.
				입력필드에 name 속성이 없으면 해당 입력필드의 값이 서버로 전달되지 않는다.
				<input type="text" name="userId" />
					위의 입력필드에 값을 입력하면, "userId=값"의 형태로 서버로 전달된다.
			checked
				체크박스와 라디오버튼에서 사용가능한 속성이다.
				체크박스와 라디오버튼의 체크여부를 지정한다.
				<input type="checkbox" name="skill" value="java" checked="checked"/> 자바
				<input type="checkbox" name="skill" value="python" /> 파이썬

				<input type="radio" name="gender" value="male" /> 남자
				<input type="radio" name="gender" value="female" checked="checked"/> 여자
			placeholder
				입력값에 대한 힌트를 지정한다.
			minlength, maxlength
				입력필드에 입력가능한 최소 문자길이, 최대 문자길이를 지정한다.
			min, max, step
				입력필드가 type="number"인 경우, 최소값, 최대값, 한번에 증가감소되는 값을 각각 지정한다.
				<input type="number" name="amount" min="0" max="1000" step="10" />
	select 태그
		콤보박스 생성하는 태그다.
		복수개의 아이템 중에서 하나 혹은 여러개를 선택할 수 있다.
		select 태그는 여러 개의 옵션 태그를 포함한다.
		option 태그는 콤보박스의 아이템을 정의한다.
		optgroup 태그는 옵션들을 그굽화 한다.

		<select name="city">
			<option value=""> -- 선택하세요 --</option>
			<option value="seoul">서울</>
			<option value="pusan">부산</>
			<option value="daegu">대구</>
			<option value="incheon">인천</>
			<option value="tadjeon">대전</>
			<option value="Gwangju">광주</>
			<option value="ulsan">울산</>
			<option value="sejong">세종특별시</>
		</select>

		select의 속성
			name
				서버로 전송된 값의 이름을 지정한다.
			size
				한번에 표시되는 옵션의 갯수를 지정한다.
				기본값은 1이다.
			multiple
				옵션을 복수개 선택가능하게 한다.
		option의 속성
			value
				옵션의 값을 지정한다.
			selected
				해당 옵션이 기본으로 선택된다.
			disabled
				해당 옵션은 선택할 수 없다.
	textare 태그
		여러 줄 입력 가능한 입력필드를 정의한다.
		여는 태그와 닫는 태그를 반드시 기술해야 한다.
		입력필드의 값은 여는 태그와 닫는 태그 사이에 적는다.
			<input type="text" value="입력값" />
			<textarea>입력값</textarea>
		주요속성
			rows
				라인의 갯수를 지정한다.
			cols
				표시되는 너비를 지정한다
			
	
	폼 입력양식의 속성
-----------------------------------------------------------------------------------------------------------------------------
태그명 	구분		속성명		속성값							설명
-----------------------------------------------------------------------------------------------------------------------------
form				method		get, post							요청방식을 지정한다.
				action		텍스트							폼 입력값을 전달받아서 처리하는 웹 애플리케이션의 경로
				enctype		application/x-www-form-urlencoded		폼 입력값의 인코딩 방식을 지정한다.
								multipart/form-data
-----------------------------------------------------------------------------------------------------------------------------
input	type=checkbox
				checked		checked							체크박스의 체크여부를 지정한다.
		type=radio	
				checked		checked							라디오버튼의 체크여부를 지정한다.
-----------------------------------------------------------------------------------------------------------------------------
option			selected		selected							옵션의 선택여부를 지정한다.
				disabled		disabled							해당 옵션을 비활성화한다.
-----------------------------------------------------------------------------------------------------------------------------
input	type=text
		type=password
				minlength		숫자								최소문자열길이를 지정한다.
				maxlength		숫자								최대문자열길이를 지정한다.
-----------------------------------------------------------------------------------------------------------------------------
input	type=number
				min			숫자								최소값
				max			숫자								최대값
				step			숫자								증감치
-----------------------------------------------------------------------------------------------------------------------------
input	type=file
				accept		audio/*							첨부가능한 파일의 종류를 지정한다.
							video/*
							image/*
							.jpg
							.png
							.xls	
															<input type="file" accept="image/*,video/*" />						
-----------------------------------------------------------------------------------------------------------------------------
select			size			숫자								한번에 표시되는 옵션의 갯수를 지정한다.
				multiple		multiple							옵션의 복수개 선택가능여부를 지정한다.
----------------------------------------------------------------------------------------------------------------------------
textarea			rows			숫자								최대 라인 수를 지정한다.
				cols			숫자								최대 너부를 지정한다.
----------------------------------------------------------------------------------------------------------------------------
input			
select
textarea			
				name			텍스트							입력양식에 이름을 지정한다.						
				disabled		disabled							입력양식을 비활성화한다.
				readonly		readonly							입력양식의 값을 읽기전용으로 설정한다. 값변경 불가능
															(chekbox와 radio 버튼은 제외)
----------------------------------------------------------------------------------------------------------------------------

* 모든 폼입력양식(input, select, textarea)에 name 속성을 지정하자.
* 체크박스, 라디오버튼에는 value 속성을 지정하자.
* 첨부파일 업로드가 있는 form에는 enctype="multipart/form-data" 속성을 지정하자.
* 첨부파일 필드는 value 속성으로 값을 설정할 수 없다.
* 모든 폼입력양식은 disabled="disabled" 속성이 적용되면 해당 폼입력값은 수정할 수 없고, 서버로 전달되지 않는다.
* 버튼에 disabled="disabled"를 지정하면 해당 버튼이 비활성화된다.
* checkbox, raio를 제외한 모든 폼입력양식은 readonly 속성을 지정해서 읽기 전용 필드로 지정할 수 있다.
* 모든 폼입력양식은 form 태그 내부에 존재할 때만 서버로 전송할 있다.
* 폼 입력값을 서버로 전송시키는 (<button type="submit">전송</button, <input type="submit" value="전송" />,<button>전송</button)버튼은 form 태그 내부에 존재해야 한다.
* 폼내부에 위치하고 있는 입력필드(checkbox, radio, textarea, select는 제외)에서 Enter를 입력하면 그 입력필드가 위치하고 있는 폼의
모든 입력값이 서버로 전송된다. 
* 폼태그 내부에 폼태그를 포함할 수 없다.

9. 블록요소와 인라인요소
	블록요소
		<태그명 style="display: block;">		
		특징
			* 항상 새로운 라인에서 시작한다.
			* 화면 크기 전체의 가로폭을 차지한다.(width:100%)
			* width, height, margin, padding 프로퍼티 지정이 가능하다.
			* block 레벨 요소는 inline 레벨 요소를 자식 요소로 포함할 수 있다.
		블록요소들
			* div, h1 ~ h6, p, ol, ul, li, dl, dt, dd, hr, table, form 등

	인라인요소		
		<태그명 style="display: inline;">	 
		특징
			* 새로운 라인에서 시작하지 않으며, 문장의 중간에 들어갈 수 있다. 다른 요소와 함께 한 행에 위치한다.
			* content의 너비만큼 가로폭을 차지한다.
			* width, height, margin-top, margin-bottom 프로퍼티를 지정할 수 없다.
			* inline 레벨 요소는 block 레벨 요소를 자식 요소로 포함할 수 없다.
			* 일반적으로  inline 레벨요소는 block 레벨 요소에 포함되어 사용된다.
		인라인요소들
			* span, a, strong, em, del, mark, small, img, input, select, textarea, button

	컨테이너 요소(컨테이너 엘리먼트)
		블록레벨 컨테이너 요소
			div
				* 다른 블록레벨 요소 혹은 다른 인라인레벨 요소를 담는 태그다.
				* 사용예
					<div>
						블록레벨 요소 혹은 인라인레벨 요소
					</div>
		인라인레벨 컨테이너 요소
			span
				* 텍스트의 일부분을 담는 태그다.
				* 사용예
					<p>인라인레벨 요소는 <span>width, height, margin-top, margin-bottom</span> 프로퍼티를 지정할 수 없다</p>
					<p>할인가격 : <strong>15,000</strong> 원</p>

10. id 속성과 class 속성
	id 속성
		* 특정 엘리먼트(태그)를 식별하기 위한 용도로 사용된다.
		* 웹문서 전체에서 똑같은 id 속성값을 가진 태그는 없어야 한다.
		* id의 속성의 값은 고유해야 한다.
		* 사용 목적
			* 특정 아이디값을 가진 태그(엘리먼트)에만 스타일을 지정할 때
			* 특정 아이디값을 가진 태그를 선택해서 javascript로 조작해야 할 때
		
	class 속성
		* 같은 클래스값을 가진 태그는 같은 스타일이 적용되게 하기위한 용도로 사용된다.
		* html 파일내에 같은 클래스값을 가진 태그들이 여러 개 있을 수 있다.			
		* class속성은 여러 개의 속성값을 가지는 것이 가능하다.	
		* class속성에서 사용되는 속성값은 CSS파일 혹은 <style>태그 안에 선택자와 스타일이 미리 정의되어 있어야 한다.

		* 사용 목적
			* 같은 클래스 속성값을 가진 태그에는 같은 스타일을 지정할 때

</pre>
