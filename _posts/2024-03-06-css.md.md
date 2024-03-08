# CSS에 대하여



#### 1.**selector** 알아보기

**selector란?**

-선택을 해주는 요소. 이를 통해 특정 요소들을 선택하여 스타일을 적용할 수 있게된다.

selector에도 여러가지 종류가 있는데 이 중에서도 가장 보편적인 class와 id 선택자를 알아보겠다.

```
1)class selector

클래스 선택자는 주어진 값을 class속성 값으로 가진 HTML요소를 찾아 선택한다. 이때 선택하려는 속성값 앞에 마침표를 추가해 작성한다. 클래스는 여러가지 요소를 묶어서 css를 지정할 수 있다.

2)id selector

아이디 선택자는 마침표 대신 #을 사용한다. 클래스 선택자와 매우 유사하지만 아이디 선택자는 하나의 요소만을 지정해서 css를 사용할 수 있다.


```



#### 2.**attribute** 알아보기

**attribute**란?

-HTML요소에 대한 추가적인 정보를 제공하는 속성이다. 이 속성은 HTML 태그의 시작 태그에 추가되며, 보통 속성의 값으로 특정한 동작이나 동작에 대한 정보를 전달한다.

attribute의 종류에 대해서 알아보자면

```
1)id : 요소의 고유한 식별자 정의.

2)class : 요소에 CSS 클래스 부여. 여러 개의 클래스 지정 가능.

3)style : 요소에 inline스타일 적용. CSS 속성과 값 형식으로 작성되며 해당 요소에만 적용되는 스타일 지정.

4)onclick : 클릭 이벤트를 처리하는 자바스크립트 코드 실행.

5)onload : 페이지나 요소가 완전히 로드된 후에 실행할 자바스크립트 코드를 정의. 일반적으로 페이지를 로딩하거나 요소가 표시될 때 초기화 로직을 처리하는데 사용.

6)data- : 사용자 정의 데이터 속성 정의.
```



#### 3.**조합 선택자** 알아보기

1)**그룹 선택자**:여러 선택자를 하나로 그룹 지을 때 사용 선택자와 선택자는 ,로 구분.

![image-20240303171803516](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20240303171803516.png)

2)**자식 선택자**:부모 요소의 하위에 있는 자식 요소에 스타일을 적용할때 사용.

![image-20240303171919889](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20240303171919889.png)

3**)하위 선택자**:선택자의 범위를 특정 부모 요소의 하위 요소로 한정하는 방법2개 이상의 선택자를 사용하며, 선택자와 선택자는 공백으로 구분.

4)**인접 형제 선택자**:지정된 선택자 요소 다음에 있는 형제 관계 요소를 선택자로 지정한다. 2개 이상의 선택자 사용하 선택자와 선택자는 +로 연결.

![image-20240303172354305](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20240303172354305.png)

5)**일반 형제 선택자**:이전 선택자 뒤에 오는 형제 관계 요소를 모두 선택자로 지정.

![](C:\Users\1\Pictures\대학과제\Screenshots\8.png)



#### 4.**visibility** **& display** 알아보기

1)**visibility** 속성

-visibility 속성은 요소를 보이게 할 건지 안보이게 할 건지를 지정한다.

```
visible : 박스가 보여진다.
hidden : 박스가 보이지 않지만 공간을 확보하기 때문에 여전히 레이아웃에 영향을 미친다.
collapse : 내부 테이블 객체에 적용된다. hidden과 유사하다.
inherit : 부모 요소로부터 값을 상속 받는다.
```

2)**diplay** 속성

-display는 레이아웃에서 자주 사용되는 요소이다. 기본적으로 HTML은 block 또는 inline 특성을 갖는다.

```
block : 가로영역을 모두차지하고 줄바꿈이 가능하다.
inline : 글자화영역이며 줄바꿈을 할 수 없다.
none : 해당요소를 화면에서 없애버린다.
```



#### 5.layout 배치 flex & dialog 알아보기

**1)flex란?**

-display 속성 중 하나로써 박스 레이아웃을 작성할 때 사용되는 아주 유용한 방법. 요소의 width나 height를 지정하지 않고도 유연하고 균형잡힌 배치가 가능.



**ex)**

```html
<body>
    <div id="parent">
        <div class="child">box1</div>
        <div class="child">box2</div>
    </div>
</body>
//CSS
* {
    box-sizing: border-box;
    margin : 10px;
    padding : 10px;
}

#parent {
    width : 300px;
    height : 100px;
    display: flex;
    flex-direction: row;
    border : 3px solid red;
}

.child {
    flex: 1 0 auto;
    border : 3px solid green;
}
```

![image-20240306164418830](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20240306164418830.png)



**2)dialog란?**

-dialog는 팝업 정보를 설정한다. 스크립트를 사용하지 않고 웹 페이지 위에 핍업을 쉽게 만들 수 있다. position:absolute;를 통해 위치가 설정된다.



**ex)**

```markup
<button onclick="window.dialog.show();">dialog 열기</button>

<dialog id="dialog">
    dialog를 자바스크립트와 같이 사용합니다.
    <button onclick="window.dialog.close();">닫기</button>
</dialog>
```

![](C:\Users\1\Pictures\대학과제\Screenshots\000.png)

![image-20240306170705180](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20240306170705180.png)
