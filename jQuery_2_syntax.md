# jQuery Syntax

jQuery를 사용하면 <b>쉽게</b> HTML element를 선택하고 다룰 수 있다.
  
### Document가 준비됐을 때 코드 호출
```javascript
window.onload = function() {
    alert("Welcome");
};
```
위 코드는 브라우저가 document 로딩을 완료했을 때 호출된다. 이미지를 포함한 document의 모든 리소스가 로딩되기 전에 호출되지 않는다. document가 조작될 준비가 되자마자 함수를 호출하고 싶으면 ready 이벤트를 활용하면 된다.
```javascript
$(document).ready(fucntion() {
    alert("Welcome");
});
```

### Selector
jQuery Selector는 HTML element를 선택할 때 사용된다. HTML element를 선택하는 문법은 CSS에서 HTML element를 명시할 때 따르는 룰과 같다.
- HTML element 이름: 아무런 기호 없이 tag 이름만
```javascript
#("div")
```
- Element ID: HTML tag에 id attribute에 설정된 id로 접근
```javascript
$("#element-id")
```
- Element Class: HTML tag에 class attribute에 설정된 class 이름으로 접근
```javascript
$(".element-class")
```

### jQuery Selector Syntax
```javascript
$(document).ready(function() {
    $(selector);
});
```
jQuery selector는 $로 시작하고 () 안에 selector를 명시한다. $()는 <b>factory function</b>이라고 불린다.

1. Element selector 예시
```html
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src="https://code.jquery.com/jquery-3.7.1.js"></script>
<script>
   $(document).ready(function() {
      $("p").css("background-color", "yellow");
   });
</script>
</head>
<body>
   <h1>jQuery element Selector</h1>

   <p>This is p tag</p>
   <span>This is span tag</span>
   <div>This is div tag</div>
</body>
</html>
```
2. #id selector 예시
```javascript
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src="https://code.jquery.com/jquery/jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {
      $("#foo").css("background-color", "yellow");
   });
</script>
</head>
<body>
   <h1>jQuery #id Selector</h1>

   <p id="foo">This is foo p tag</p>
   <span id="bar">This is bar span tag</span>
   <div id="bill">This is bill div tag</div>
</body>
</html>
```
3. .class selector 예시
```javascript
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src = "https://code.jquery.com/jquery/jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {
      $(".foo").css("background-color", "yellow");
   });
</script>
</head>
<body>
   <h1>jQuery .class Selector</h1>

   <p class="foo">This is foo p tag</p>
   <p class="foo">This is one more foo p tag</p>
   <span class="bar">This is bar span tag</span>
   <div class="bill">This is bill div tag</div>
</body>
</html>
```