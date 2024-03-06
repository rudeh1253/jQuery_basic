# Manipulate Elements

### ```append()``` 메소드
```append()``` 메소드를 사용해서 element 뒤에 새로운 content를 덧붙일 수 있다.
```javascript
$(selector).append(content, [content]);
```
<b>content</b> 파라미터로 HTML string, HTML element(DOM element), text node, element 배열, jQuery object가 올 수 있다.

다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="container">
    <h2>jQuery append() Method</h2>
    <div class="inner">Hello</div>
    <div class="inner">Goodbye</div>
</div>
```
다음 jQuery 코드를 호출하면:
```javascript
$(".inner").append("<p>Zara</p>");
```
다음과 같은 결과를 만들 수 있다.
```html
<div class="container">
    <h2>jQuery append() Method</h2>
    <div class="inner">Hello
    <p>Zara</p>
    </div>
    <div class="inner">Goodbye
    <p>Zara</p>
    </div>
</div>
```

### ```after()``` 메소드
```after()``` 메소드를 사용해서 특정 element 다음에 content를 삽입할 수 있다.
```
$(selector).after(content, [content]);
```

다음과 같은 HTML 코드가 있다.
```html
<div class="container">
    <h2>jQuery after() Method</h2>
    <div class="inner">Hello</div>
    <div class="inner">Goodbye</div>
</div>
```

다음 jQuery 코드를 호출하면
```javascript
$( ".inner" ).after( "<p>Zara</p>" );
```
HTML이 다음과 같이 변경된다.
```html
<div class="container">
    <h2>jQuery after() Method</h2>
    <div class="inner">Hello</div>
    <p>Zara</p>
    <div class="inner">Goodbye</div>
    <p>Zara</p>
</div>
```

append, after와 대응하는 메소드로 prepend, before 메소드가 있다.

### Element 제거
```remove()``` 메소드로 Element를 제거해 줄 수 있다.
```javascript
$(selector).remove();
```

### Filtering하면서 Element 제거
```javascript
$("div").remove(".hello");
```
이렇게 하면 div 태그 내부에 class가 hello인 element만 제거해 준다.