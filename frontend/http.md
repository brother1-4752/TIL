# 3강 HTTP

- HTTP란? 우리가 서버와 소통하는 방법이야.
- HTTP Request는 웹사이트에 접속하고 서버에 정보를 보내는 방법이다.
- Get, HTTP 메서드는 브라우저가 자동으로 해당 라우터에서 화면을 얻어내려고 하는 것이야.

```html
1. application을 만들고
2. application을 설정하고
3. application listen하고 외부로 개방할거야.
```

- app.get(’경로’, 콜백함수)
    
    ```html
    콜백함수는 route handle하는 함수이다. 이것에는 인자가 2개가 꽁짜다.
    바로 req object와 res object이다.
    이 두 인자는 express로부터 받은 것이다.
    ```
    

<aside>
💡 즉, home(’/’)으로 get request가 오면, express는 handleHome에다가 req, res object를 넣어준다. 이것이 express가 무대 뒤에서 하는 일이야.

</aside>

- Middle ware = middle software이다. 무엇에 중간에 있나? 바로 req와 res 사이에 있다. 브라우저가 request한 다음에, 내가 응답을 하기 전 middleware가 있다. 인자는 하나 더 받는다. next.
- 미들웨어 morgan은 status, url, http method, 페이지를 렌더링하는데 걸리는 시간을 로그해준다.
