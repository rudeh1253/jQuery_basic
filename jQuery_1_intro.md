# jQuery
JavaScript를 더욱 쉽고 멋지게 사용하게 해 주는 JavaScript 라이브러리

### jQuery의 장점
- Vanila JavaScript의 코드를 현격하게 줄여준다.
  
### jQuery로 할 수 있는 것
- HTML/DOM manipulation
- CSS manipulation
- HTML event methods
- Effects and animations
- AJAX
- Utilities

### jQuery를 사용하는 기업
- Google
- Microsoft
- IBM
- Netflix

## jQuery 도입하는 법
### 다운로드 받기
jQuery에는 Production 버전과 Development 버전이 있다. Production 버전은 경량 버전으로 AS-IS 시스템에 적용시키기 용이한 버전이다.
Development 버전은 콘텐츠가 모두 담긴 완전한 jQuery 라이브러리로 테스팅, 개발에 사용된다.

jQuery는 하나의 JavaScript 파일이다. HTML의 ```<script>``` 태그로 포함시켜주면 된다.
```html
<head>
    <script src="jquery-3.7.1.min.js"></script>
</head>
```

### jQuery CDN Link
jQuery를 다운로드받지 않더라도 CDN (Content Delivery Network) Link를 포함시킴으로써 jQuery를 사용할 수 있다.
```html
<script src="https://code.jquery.com/jquery-3.7.1.js"     
        integrity="sha256-eKhayi8LEQwp4NKxN+CfCh+3qOVUtJn3QNZ0TciWLP4="
        crossorigin="anonymous"></script>
```

#### ※ CDN (Content Delivery Network)
CDN은 지리적으로 여러 군데에 퍼진 서버 그룹으로, CDN을 이루는 각 서버는 JavaScript, HTML, CSS, 이미지 등의 리소스를 캐싱(cache)한다. 클라이언트(user)에서 서버 호스트에 리소스를 요청(request)하면 해당 클라이언트에서 가장 가까운 CDN 서버에 저장(캐싱)된 리소스를 클라이언트에게 제공한다. 클라이언트의 요청은 원 서버(origin server)에까지 도달할 필요가 없으므로 응답시간이 단축된다. CDN을 이루는 각 서버는 proxy server의 한 종류이다.