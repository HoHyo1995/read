# CSS

## 2. 속성
### 2.1 문자
#### text-align
문단을 정렬하는 속성입니다. 가운데, 왼쪽, 오른쪽 정렬이 가능합니다.
~~~css
    text-align : center; /*가운데정렬*/
    text-align : left; /*왼쪽정렬*/
    text-align : right; /*오른쪽정렬*/
    text-align : justify; /*양쪽정렬*/
~~~
#### vertical-align
inline이나 inline-block요소에만 적용되는 수직정렬 속성입니다.
~~~css
    vertical-align : baseline; /*기본 값*/
    vertical-align : super; /*윗 첨자로 표현*/
    vertical-align : sub; /*아래 첨자로 표현*/
    vertical-align : -14px; /*양수는 위로 음수는 아래로*/
    vertical-align : 20%; /*양수는 위로 음수는 아래로*/
등...
~~~
#### text-decoration
글자에 줄을 줄수 있습니다.
~~~css
    text-decoration : none; /*기본 값*/
    text-decoration : underline; /*밑줄*/
    text-decoration : overline; /*윗줄*/
    text-decoration : line-through; /*가운데줄*/
등...
~~~
#### font-size
글자의 크기를 나타냅니다. px단위를 사용하며 em, %등 사용이 가능합니다.
~~~css
    font-size : 20px;
~~~
#### font-weight
글자의 굵기를 조절하는 속성입니다.
~~~css
    font-weight : nomal; /*400은 기본굵기*/
    font-weight : lighter; /*400이하는 기본보다 얇게*/
    font-weight : bold; /*700은 굵게*/
    font-weight : bolder; /*700이상은 더 굵게*/
    font-weight : inherit; /*상위요소 상속*/
    /*숫자로도 입력이 가능합니다.*/
~~~
### 2.2 배경
#### background-attachment
배경이미지 고정에 대한 속성입니다.
~~~css
    background-attachment : scroll; /*기본 값, 고정 되어있음*/
    background-attachment : local; /*스크롤을 움직일때 이미지가 내용과 같이 움직임*/
    등...
~~~
### 2.3 display와 visibility
#### display
요소를 어떻게 보여줄지를 정합니다.
~~~css
    display : block; /* 요소를 블록 요소로*/
    display : inline; /*요소를 인라인 요소로*/
    display : inline-block; /*요소의 줄바꿈이 없지만 높이와 너비를 가짐*/
    display : none; /* 요소를 안보여줌(자신의 영역도 사라짐) */
    display : inherit; /*부모요소 상속*/
    등...
~~~
#### visibility
해당 요소가 보여질지 안보여질지를 정합니다.
~~~css
    visibility : visible; /*기본값*/
    visibility : hidden; /*요소를 안보여줌(자신의 영역은 남아있음)*/
    visibility : collapse; /*(table, tr, td, th)등의 요소에서만 사용가능하고 요소를 안보여줌*/
~~~
### 2.4 박스 안 문자
#### overflow
박스요소 안의 내용과 포함된 요소가 벗어날 때 처리 방법을 정합니다.
~~~css
    overflow : visible; /*기본 값, 박스밖으로 컨텐츠가 보임*/
    overflow : scroll; /*컨텐츠에 맞게 스크롤바가 생김*/
    overflow : hidden; /*박스밖으로 나가는 컨텐츠 모두 숨김*/
    overflow : auto; /*컨텐츠가 짧으면 없고 길면 생김*/
    overflow : inherit; /*부모의 속성 값을 물려 받음*/
~~~
### 2.5 float와 clear
#### float
이미지를 띄워서 텍스트와 함께 어떻게 배치하는지 설정하는 속성으로 최근에는 레이아웃용으로 많이 사용 됩니다.
~~~css
    float : letf; /*요소를 왼쪽으로*/
    float : right; /*요소를 오른쪽으로*/
    float : inherit; /*부모의 속성을 상속 받음*/
~~~
#### clear
float속성을 제거하기 위해 쓰입니다.
~~~css
    clear : left; /*float : letf; 해제 */
    clear : right; /*float : right; 해제 */
    clear : both; /*모두 해제*/
    clear : inherit; /*부모의 속성을 상속 받음*/
~~~
##  참고
<https://opentutorials.org/course/4>  
<http://webberstudy.com/>  
<https://aboooks.tistory.com/171>  
<https://webdir.tistory.com/348>  
<https://ofcourse.kr/css-course/clear-%EC%86%8D%EC%84%B1>