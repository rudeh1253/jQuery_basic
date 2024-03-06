# Attributes 조작

jQuery에서 ```attr()``` 메소드로 HTML element의 attribute를 가져와서 조작할 수 있다.

```javascript
<!doctype html>
<html>
<head>
<title>The jQuery Example</title>
<script src="https://code.jquery.com/jquery/jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {
      $("button").click(function(){
         alert( "Href = " + $("#home").attr("href"));
         alert( "Title = " + $("#home").attr("title"));
      });
   });
</script>
</head>
<body>
   <p>Click the below button to see the result:</p>
   
   <p><a id="home" href="index.htm" title="Tutorials Point">Home</a></p>
   <button>Get Attribute</button>
</body>
</html>
```

### Attribute 조작하기
```html
<body>
    <p>
        <a id="home" href="index.html" title="Tutorials Point">
            Home
        </a>
    </p>

    <script type="text/javascript">
        $("#home").attr("href", "https://www.google.com/");
    </script>
</body>
```

### 표준 attributes
HTML에서 제공하는 기본적인 attribute이다.
- class
- id
- href
- title
- rel
- src
- style
```html
<img id="id" src="image.gif" alt="Image" class="class" title="This is an image"/>
```

### 커스텀 데이터 attributes
HTML element에 커스텀 attribute를 부여할 수 있다. 이와 같은 attirbute 이름들은 "<b>data-</b>"로 시작한다.
```html
<img data-copyright="Tutorials Point" id="imageid" src="image.gif" alt="Image"/>
```

커스텀 attribute는 standard attribute와는 달리 element에 특정한 기능을 부여하지 않지만, element에 커스텀 데이터를 세팅해 줄 수 있다. 세팅된 데이터를 서버에 전송하는 등 데이터를 가지고 추가적인 로직을 수행할 수 있다.

### 커스텀 데이터 attribute 세팅
jQuery의 ```data(name, value)``` 메소드는 커스텀 attribute에 값을 세팅하는 데 사용된다.
```html
<div id="home" data-author-name="Richard Bellman" data-year="2022">
    Just an Example Content
</div>

<script type="text/javascript">
    $("#home").data("author-name", "Edger Dijkstra");
</script>
```