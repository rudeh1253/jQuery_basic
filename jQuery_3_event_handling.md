# Event Handling

### Events
| 마우스 | 키보드 | Form | Document |
|---|---|---|---|
| click | keypress | submit | load |
| dblclick | keydown | change | resize |
| hover | keyup | select | scroll |
| mousedown | | blur | unload |
| mouseup | | focusin | ready |

### ```<div>``` element에 마우스 Click 이벤트 바인딩
```javascript
$("div").click(function() {
    alert("Div has been clicked");
});
```

#### bind를 이용한 이벤트 바인딩
```javascript
$("div").bind("click", function() {
    alert("Div has been clicked");
});
```

### jQuery Event Object
이벤트가 발생할 때, <b>Event Object</b>가 모든 이벤트 handler 함수에 전달된다. Event object는 이벤트와 관련된 다양하고 유용한 정보를 포함한다.

Event Object는 불필요할 때 파라미터로 명시되지 않아도 상관없지만, Event Object를 사용해야 할 때 파라미터로 명시해야 한다.

```javascript
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {
      $("div").click(function(e){
         alert('Event type is ' + e.type);
         alert('pageX : ' + e.pageX);
         alert('pageY : ' + e.pageY);
         alert('Target : ' + e.target.innerHTML);
      });
   });
</script>
<style>
   div{ margin:10px;padding:12px; border:2px solid #666; width:60px;cursor:pointer}
</style>
</head>
<body>
   <p>Click on any of the squares to see the result:</p>

   <div>One</div>
   <div>Two</div>
   <div>Three</div>
</body>
</html>
```

#### Event Object의 properties
| Property | <div style="width: 100px">Description</div> |
|--- |--- |
| target | 이벤트가 발생한 대상 (예를 들어 특정 HTML element를 클릭했들 때 click한 element) |
| screenX | 마우스 이벤트에서 화면상의 x축 좌표 |
| screenY | 마우스 이벤트에서 화면상의 y축 좌표 |
| pageX | 마우스 이벤트에서 페이지상의 x축 좌표 |
| pageY | 마우스 이벤트에서 페이지상의 y축 좌표 |
| keyCode | 키보드를 눌렀을 때 발생하는 이벤트(keyup, keydown)에서 눌린 키보드 키의 코드값 |
| type | 발생한 이벤트의 타입 (e.g. click) |

[이외에도 더 많은 property가 담겨 있다.](https://www.tutorialspoint.com/jquery/jquery-events.htm)

### Event Handler에서 ```this``` 키워드
Event handler에서 ```this``` 키워드는 이벤트가 발생한 DOM element를 가리킨다.

Example
```javascript
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {
      $("div").click(function(){
         alert($(this).text());
      });
   });
</script>
<style>
   div{ margin:10px;padding:12px; border:2px solid #666; width:60px;cursor:pointer}
</style>
</head>
<body>
   <p>Click on any of the squares to see the result:</p>

   <div>One</div>
   <div>Two</div>
   <div>Three</div>
</body>
</html>
```

### Event handler 제거하기
jQuery에서 제공하는 ```unbind()``` 메소드를 사용함으로써 event handler를 제거할 수 있다.

```javascript
selector.unbind(eventType, handler)
```
또는
```javascript
selector.unbind(eventType)
```

### jQuery 이벤트 레퍼런스
[jQuery Events Reference](https://www.tutorialspoint.com/jquery/jquery_ref_events.htm)

이 페이지에서 jQuery에서 제공하는 모든 이벤트 메소드와 property를 참조할 수 있다.