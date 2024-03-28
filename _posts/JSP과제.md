```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>투두리스트 만들기</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous">

<script type="text/javascript">
	function addItem() {
		let todo = document.getElementById("item");
		let list = document.getElementById("todolist");
		let listitem = document.createElement("li");
		listitem.className
		= "d-flex list-group-item list-group-item-action list-group-item-warning";
		let xbtn = document.createElement("button");
		xbtn.className = "btn-close ms-auto";
		
		xbtn.onclick = function(e) {
			let pnode = e.target.parentNode;
			list.removeChild(pnode);
		}
		listitem.innerText = todo.value;
		listitem.appendChild(xbtn);
		list.appendChild(listitem);
		
		todo.value = "";
		todo.focus();
	}
</script>

</head>
<body>
	<div class = "container bg-warning shadow mx-auto mt-5 p-5 w-75"> 
		<h2>My ToDo App</h2>                                            
		<hr>                                                                
		<div class = "input-group">
			<input id = "item" class = "form-control" type = "text" placeholder="할일을 입력하세요">
			<button type = "button" class = "btn btn-primary" onclick = "addItem()">할일 추가
			</button>
		</div>
		<hr>
		<ul id = "todolist" class = "list-group"></ul>
	</div>
</body>
</html>
```

```html
<div class = "container bg-warning shadow mx-auto mt-5 p-5 w-75">
//container: 화면 전체를 차지하지 않는 고정크기 컨테이너로 크기 변동에 반응해서 변한다.
//bg-warning: 기본 노란색 컬러로 배경을 지정한다.
```

```html
function addItem() {
		let todo = document.getElementById("item");
		let list = document.getElementById("todolist");
		let listitem = document.createElement("li");
}
//입력값을 읽어와 todo변수에 저장하고 <ul>요소를 참조하여 list 변수에 저장한 다음 새로운 <li>요소를 생성하여 listitem변수에 저장하는 코드이다
```

```html
let xbtn = document.createElement("button");
		xbtn.className = "btn-close ms-auto";
listitem.appendChild(xbtn);
//<li>요소에 들어갈 닫기 버튼을 생성하고 버튼에 부투스트랩 클래스를 적용한 다음 <li>에 버튼을 추가하는 코드이다.
```

```html
xbtn.onclick = function(e) {
			let pnode = e.target.parentNode;
			list.removeChild(pnode);
		}
//close버튼에 이벤트를 처리하는 함수이다. 이벤트가 발생한 <li>요소를 구하여 <ul>요소에서 제거하는 코드이다.
```
