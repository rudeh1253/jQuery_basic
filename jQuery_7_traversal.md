# Traversal

HTML은 hierarchy 구조로 구조화됐기 때문에 child element의 child element의 child element의... 와 같은 방식으로 element를 순회할 수 있다.

### Travering ancestor: ```parent()```
```parent()``` 메소드는 바로 상위의 element를 리턴한다.

다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ```parent()``` 메소드를 다음과 같이 사용할 수 있다.
 ```
 $(".child-two").parent().css("border", "2px solid red");
 ```
 이 코드를 실행시키면 HTML 코드가 다음과 같이 변경된다.
 ```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent" style="border:2px solid red">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ### Travering ancestor: ```parents()```
 ```parent()``` 메소드와 달리 해당 element의 모든 상위 element를 리턴한다.

 다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ```parents()``` 메소드를 다음과 같이 사용할 수 있다.
 ```
 $(".child-two").parents().css("border", "2px solid red");
 ```
 이 코드를 실행시키면 HTML 코드가 다음과 같이 변경된다.
 ```html
<div class="great-grand-parent" style="border:2px solid red">
    <div class="grand-parent" style="border:2px solid red">
        <ul class="parent" style="border:2px solid red">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ### Travering ancestor: ```parentsUntil()```

```
$(selector1).parentsUntil([selector2]);
```
selector1과 selector2 사이의 element를 반환한다.

 다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ```parentsUntil()``` 메소드를 다음과 같이 사용할 수 있다.
 ```
 $(".child-two").parentsUntil(".great-grand-parent").css("border", "2px solid red");
 ```
 이 코드를 실행시키면 HTML 코드가 다음과 같이 변경된다.
 ```html
<div class="great-grand-parent">
    <div class="grand-parent" style="border:2px solid red">
        <ul class="parent" style="border:2px solid red">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
 </div>
 ```

 ### Traversing descendants: ```children()```

 ```children()``` 메소드는 바로 하위의 element를 반환한다.

다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-three">Child Three</li>
            <li class="child-four">Child Four</li>
        </ul>
    </div>
 </div>
 ```

 ```children()``` 메소드를 다음과 같이 사용할 수 있다.
 ```
 $(".great-grand-parent").children().css("border", "2px solid red");
 ```
 이 코드를 실행시키면 HTML 코드가 다음과 같이 변경된다.
 ```html
<div class="great-grand-parent">
    <div class="grand-parent" style="border:2px solid red">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
    <div class="grand-parent" style="border:2px solid red">
        <ul class="parent">
            <li class="child-three">Child Three</li>
            <li class="child-four">Child Four</li>
        </ul>
    </div>
 </div>
 ```

### Traversing descendants: ```find()```

```
$(selector).find(filter);
```
filter에 맞는 하위의 element들을 반환한다.

다음과 같은 HTML 코드가 있다고 하자.
```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one">Child One</li>
            <li class="child-two">Child Two</li>
        </ul>
    </div>
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-three">Child Three</li>
            <li class="child-four">Child Four</li>
        </ul>
    </div>
 </div>
 ```

 ```find()``` 메소드를 다음과 같이 사용할 수 있다.
 ```
 $(".great-grand-parent").find("li").css("border", "2px solid red");
 ```
 이 코드를 실행시키면 HTML 코드가 다음과 같이 변경된다.
 ```html
<div class="great-grand-parent">
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-one" style="border:2px solid red">Child One</li>
            <li class="child-two" style="border:2px solid red">Child Two</li>
        </ul>
    </div>
    <div class="grand-parent">
        <ul class="parent">
            <li class="child-three" style="border:2px solid red">Child Three</li>
            <li class="child-four" style="border:2px solid red">Child Four</li>
        </ul>
    </div>
 </div>
 ```

## parent, parents, parentsUntil, children, find 메소드에 filter를 argument로 추가 전달함으로써 반환될 element를 filtering할 수 있다.

```javascript
$(selector1).parents(selector2)
```