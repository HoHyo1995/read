# CSS

## 1. 선택자

### 1.1 요소 선택자
div, h1, p등의 요소명을 적어서 선택 할 수 있습니다.  
~~~css
div {
    background-color : #f7f7f7;
}
~~~  
### 1.2 ID 선택자
요소에 ID라는 속성에 값을 주어 그 값을 사용하여 선택 할 수 있습니다.  
ID값의 앞에 '#'을 붙여 사용합니다.
~~~css
#loginId {
    font-size : 10px;
}
~~~
~~~html
<p id="loginId">kiri</p>
~~~
### 1.3 Class 선택자
요소에 class라는 속성에 값을 주어 그 값을 사용하여 선택 할 수 있습니다.
ID값의 앞에 '.'을 붙여 사용합니다.
~~~css
.loginInfo {
    font-size : 10px;
}
~~~
~~~html
<p class="loginInfo">kiri</p>
~~~
### 1.4 선택자 묶어 사용하기
~~~css
div {
    background-color : #f7f7f7;
}
p {
    background-color : #f7f7f7;
}
span {
    background-color : #f7f7f7;
}
~~~  
이렇게 서로 다른 요소들에 같은 css를 적용하고 싶다면 이렇게 사용할 수 있습니다.
~~~css
div, .loginInfo, #lgoinId {
    background-color : #f7f7f7;
}
~~~
### 1.5 선택자 중첩
선택자를 중첩해서 사용하는 경우가 있습니다.(띄어쓰기를 하지 않습니다.)
ex) 제목끼리 같은 클래스값을 가졌지만 요소가 다를 경우, div요소의 title에만 css를 주고 싶은 경우
~~~html
<div class="title">제목</div>
<div class="contents">내용</div>
<span class="title">제목</span>
<span class="contents">내용</span>
~~~
~~~css
div.title{
	font-size : 10px;
}
span.contents{
    font-weight : bold;
}
~~~
### 1.6 후손 선택자
중첩 되어진 요소 중 특정한 부분에만 css를 줄 경우 사용합니다.(띄어쓰기를 해야 합니다.)  
자식 선택자만이 아닌 자식의 자식 등에도 적용이 됩니다.  
ex) 1.5와는 다르게 같은 div요소, class값 임으로 중첩을 할 수 없어 상위 요소부터 선택해서 사용합니다.
~~~html
<div>
		<div id="one">
		<div class="title">제목</div>
		<div class="contents">내용</div>
		</div>
		<div id="two">
		<div class="title">제목</div>
			<ol>
				<li><div>제목1</div></li>
				<li><div>제목2</div></li>
			</ol>
		<div class="contents">내용</div>
		</div>
	</div>
~~~
~~~css
#two div{
	font-size : 10px;
}
~~~
```후손 선택자인 경우는 제목1,제목2까지 css까지가 적용되나 자식 선택자는 적용이 되지 않습니다. ```
### 1.7 자식 선택자
중첩 되어진 요소 중 특정한 부분에만 css를 줄 경우 사용합니다.  
'>'를 사용하며 자식 선택자에게만 적용됩니다.
~~~html
<div>
		<div id="one">
		<div class="title">제목</div>
		<div class="contents">내용</div>
		</div>
		<div id="two">
		<div class="title">제목</div>
			<ol>
				<li><div>제목1</div></li>
				<li><div>제목2</div></li>
			</ol>
		<div class="contents">내용</div>
		</div>
	</div>
~~~
~~~css
#two > div{
	font-size : 10px;
}
~~~
```후손 선택자인 경우는 제목1,제목2까지 css까지가 적용되나 자식 선택자는 적용이 되지 않습니다. ```
### 1.8 가상 클래스 선택자
선택자 뒤에 ':'를 붙이면 선택한 요소들의 상태에 따라서 해당 요소를 선택되게 하는것을 말합니다.  
~~~
:link
:visited
:hover
:active
:focus
등....
~~~

~~~html
<a href="">구글</a>
~~~
~~~css
a:hover{
	color : red;
}
~~~
<hr/>

##  참고
<https://opentutorials.org/course/4>  
<http://webberstudy.com/>  
