```jsx
SEO : Search Engine Optimization : 검색 엔진 최적화!

정보구조에 맞게 의미있는 태그를 작성해야 한다.

Div만 사용하지 않기 

*기본*  
<h1~h6></h>
<p></p>
<br></br>

<em></em>          //의미: 강조
<strong></strong>  //의미: 강조

*링크*

<a href="주소">웹URL</a>
<a href="#hello">페이지내 이동</a>                      
<a href="mailto:uiissoop@gmail.com">이메일 전송</a>  
<a href="tel:01012341234">전화걸기</a>     

*target*      
<a href="주소" target"_blank">웹URL 새탭열기</a>

*image*
<img src="#" alt="" />
alt: 대체텍스트 // 사진 경로가 사라졌을 때, 설명하는 글 & 청각장애인들을 위한 screen reader

*목록(list)*
• ol : 순서가 중요할 때 (ordered list)
• ul : 순서가 중요하지 않을 때 (unordered list)
• li : list item
⭐️ ol, ul의 자식은 li만 (웹표준)
ex)
<ul>
  <li>   // li태그만 사용 가능
   <a href="주소">웹URL</a>
  </li>
</ul>

*Description list*
// 용어를 정의 할 때 사용
// key : value로 정보를 제공할 때 
• dl(description list) : 
• dt(description term) : 
• dd(description data) : 
• dfn(definition) :
ex_good)
<dl>
 <div>           // ⭕️ div태그 사용 가능
  <dt>맥북</dt>   
  <dt>M1</dt>    // ⭕️ 연달아 두 개 사용 가능(비슷한 제목)
  <dd>맥북에 대한 설명</dd>
 </div>
</dl>

ex_bad)
01. 
<dl>
 <div>   
  <dt>맥북</dt>   
  <dd>맥북에 대한 설명</dd>
  <dt>윈도우</dt>  // ❌ dt에 대한 dd설명이 없음.
 </div>
</dl>

02.
<dl>
 <section>       // ❌ div태그, dt, dd만 사용 가능
  <dt>맥북</dt>   
  <dd>맥북에 대한 설명</dd>
 </section>
</dl>

03. 
<dt>             // ❌ dl 없이 사용 불가
  사과
</dt

*Quotations*
• blockquote  
<blockquote cite="출처">  // 출처도 적어줄 수 있다.
 명언
 <cite>출처인</cite>
</blockquote>

• q 
<p>
 <q>인용문</q> 
</p>

*division / span*
// 도저히 쓸 태그 없을 때 사용 가능

*Form*
▾ <form action=""  method=""></form>
・ action: API주소
・ method: GET/POST

▾ <input type="text" placeholdr="" maxlength="" minlength="" required  disabled value ="" />  
・ placeholder: 기본적으로 제공 되는 빈칸 안의 문구
・ maxlength: input안에 적을 수 있는 최대 문자 갯수
・ minlength: input안에 적을 수 있는 최소 문자 갯수
・ required: 무조건 입력을 해야하는 값
・ disabled: 사용할 수 없게 만듦
・ value: 기본값
・ type="email": @
・ type=""password": ***
・ type="url": url값만
・ type="number": 숫자값만 / min: 숫자의 범위 max: 숫자의 범위
・ type="file": 파일첨부 / accept=".png, .jpg"

▾ <label for="누구"> //폼 양식에 이름을 붙이는 태그  ⭐️포커싱 (사용성 개선)
・ for: <label for="인풋ID">라벨</label> / <input id="인풋ID" type="text">  ! #이용 ❌

▾ Radio & CheckBox
・ Radio         // 한 가지만 선택 / name으로 그룹핑 / value로 어느 게 서버에 제출 되는지 구분 
 <input type="radio" id="subscribed" name="subscription" value="0"/>
 <lable for="subscribed">구독중</label>
 <input type="radio" id="unsubscribed" name="subscription" value="1" />
 <label for="unsubscribed">미구독</label>
 <button type="submit">Submit</button> // form 양식에서 제출하게 되면 GET방식일 때 URL 생성

・ CheckBox      // 여러가지 선택 가능
 <input type="checkBox" /> // 다중 선택 / name으로 그룹핑 / value로 어느 게 서버에 제출 되는지 구분

▾ Select & Option
<form action="" method="GET">
  <lable for="skill">스킬</label>
  <select multiple name="Skill" id="skill">
    <option value="html">HTML</option>
    <option value="js">JS</option>
  </select>
  <button type="submit">Submit</button>
</form>

▾ Textarea
<textarea> </textarea>

▾ Button
<button type=""> </button>
type="button"
type="submit"
type="reset" 

▾ Table
<table>

 <thead>      // 헤더부분만
  <tr>
   <th>테이블 헤더</th>
   <td>테이블 데이터</td>
  </tr>
 </thead>

 <tbody>
  <tr>
  </tr>
 </tbody>

 <tfoot>
  <tr>
  </tr>
 </tfoot>

</table>

・ rowspan (세로)
・ colspan (가로)
```
