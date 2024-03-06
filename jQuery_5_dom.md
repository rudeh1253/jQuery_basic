# DOM

### Content 가져오기
```javascript
$(selector).html();

$(selector).text();
```

```text()``` 메소드는 ```innerText```처럼 element 안의 text value를 return한다.

```html()``` 메소드는 ```innerHTML```처럼 element의 tag까지 포함해서 return한다.

```javascript
<!DOCTYPE html>
<html>
    <head>
        <title>The jQuery Example</title>
        <script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
        <script>
            $(document).ready(function () {
                $("#text").click(function () {
                    alert($("p").text());
                });
                $("#html").click(function () {
                    alert($("p").html());
                });
            });
        </script>
    </head>
    <body>
        <p>The quick <b>brown fox</b> jumps over the <b>lazy dog</b></p>

        <button id="text">Get Text</button>
        <button id="html">Get HTML</button>
    </body>
</html>
```

### Form field 가져오기
```javascript
$(selector).val();
```

예시
```javascript
<!DOCTYPE html>
<html>
    <head>
        <title>The jQuery Example</title>
        <script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
        <script>
            $(document).ready(function () {
                $("#b1").click(function () {
                    alert($("#name").val());
                });
                $("#b2").click(function () {
                    alert($("#class").val());
                });
            });
        </script>
    </head>
    <body>
        <p>Name: <input type="text" id="name" value="Zara Ali" /></p>
        <p>Class: <input type="text" id="class" value="Class 12th" /></p>

        <button id="b1">Get Name</button>
        <button id="b2">Get Class</button>
    </body>
</html>
```

### Content 세팅
```html()``` 메소드와 ```text()``` 메소드는 HTML element의 content를 세팅하는 데 사용될 수 있다.
```javascript
$(selector).html(val, [function]);

$(selector).text(val, [function]);
```

val는 selector를 통해 가져온 HTML element의 content를 세팅해 준다. ```html```, ```text``` 메소드에 콜백 함수를 추가로 전달할 수 있다. 이 콜백 함수는 element의 content가 변경될 때 호출된다.

```javascript
<!DOCTYPE html>
<html>
    <head>
        <title>The jQuery Example</title>
        <script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
        <script>
            $(document).ready(function () {
                $("#text").click(function () {
                    $("p").text(
                        "The quick <b>brown fox</b> jumps over the <b>lazy dog</b>"
                    );
                });
                $("#html").click(function () {
                    $("p").html(
                        "The quick <b>brown fox</b> jumps over the <b>lazy dog</b>"
                    );
                });
            });
        </script>
    </head>
    <body>
        <p>Click on any of the two buttons to see the result</p>

        <button id="text">Set Text</button>
        <button id="html">Set HTML</button>
    </body>
</html>
```

### Form field 세팅
```val()``` 메소드는 form field의 값을 세팅할 때 사용할 수 있다.
```javascript
$(selector).val(val);
```

Example
```javascript
<!DOCTYPE html>
<html>
    <head>
        <title>The jQuery Example</title>
        <script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
        <script>
            $(document).ready(function () {
                $("#b1").click(function () {
                    $("#name").val("Zara Ali");
                });
                $("#b2").click(function () {
                    $("#class").val("Class 12th");
                });
            });
        </script>
    </head>
    <body>
        <p>Name: <input type="text" id="name" value="" /></p>
        <p>Class: <input type="text" id="class" value="" /></p>

        <button id="b1">Set Name</button>
        <button id="b2">Set Class</button>
    </body>
</html>
```

### Element 교체
```replaceWith()``` 메소드를 사용해 특정 HTML element를 다른 HTML element로 교체할 수 있다.

```javascript
<!DOCTYPE html>
<html>
    <head>
        <title>The jQuery Example</title>
        <script src="https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
        <script>
            $(document).ready(function () {
                $("#b1").click(function () {
                    $("p").replaceWith("<h1>This is new heading</h1>");
                });
                $("#b2").click(function () {
                    $("h1").replaceWith("<h2>This is another heading</h2>");
                });
            });
        </script>
    </head>
    <body>
        <p>Click below button to replace me</p>

        <button id="b1">Replace Paragraph</button>
        <button id="b2">Replace Heading</button>
    </body>
</html>
```