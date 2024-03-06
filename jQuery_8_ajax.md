# AJAX

AJAX는 Ayschronous JavaScript and XML의 약자로, 화면을 <b>새로고침하지 않고</b> 서버에 요청을 보내고 응답을 받는 행위를 할 수 있다. 화면을 렌더링하는 동작과 별개로 이루어지므로 서버에 요청을 전송하고 응답을 받는 동안 화면 렌더링을 방해하지 않을 수 있다.

### AJAX 요청 보내기
```load()``` 메소드를 활용해 보낼 수 있다.

#### Syntax
```[selector.]load(URL[, data[, callback]])```

- URL

요청을 보낼 URL
- data

요청 바디에 담을 데이터
- callback

서버로부터 응답이 왔을 때 호출될 callback 메소드

예시
```html
<script type="text/javascript">
    $(document).ready(function() {
        $("#driver").click(function(event)) {
            $("#stage").load("/jqeury/result.html");
        };
    });
</script>
<div id = "stage" style = "background-color:cc0;">
    STAGE
</div>

<input type = "button" id = "driver" value = "Load Data" />
```
```load()``` 메소드가 AJAX 요청을 /jquery/result.html로 보내고, 그 응답 결과를 "stage"라는 id를 가진 ```<div>``` element에 담는다.