### 공통점

클라이언트가 요청하면 콘텐츠를 반환해준다.

---

# WebServer

클라이언트가 요청한 정적 콘텐츠를 제공하는 서버이다. (단순 HTML, CSS, JS, 이미지, 파일 등 즉시 응답 가능한 컨텐츠)

# WAS

DB조회나 다양한 로직 처리가 필요한 동적 콘텐츠를 제공하는 서버이다.

ex) 로그인, 조회 등 API요청은 대부분 해당

![Untitled](https://github.com/user-attachments/assets/e5b98852-6e92-4746-8d3d-c0b580a998d2)

**‼ [ 클라이언트(사용자)  →  Web Server  →  WAS  →  DB ] 구조의 동작 과정 ‼**

```
1. Web Server는 웹 브라우저 클라이언트(사용자)로부터 HTTP 요청을 받는다.

2. Web Server는 클라이언트의 요청(Request)을 WAS에 보낸다.

3. WAS는 관련된 Servlet을 메모리에 올린다.

4. WAS는 [web.xml을](https://codechasseur.tistory.com/web.xml%EC%9D%84) 참조하여 해당 Servlet에 대한 Thread를 생성한다. (Thread Pool 이용)

5. HttpServletRequest와 HttpServletResponse 객체를 생성하여 Servlet에 전달한다.

5-1. Thread는 Servlet의 service() 메서드를 호출한다.

5-2. service() 메서드는 요청에 맞게 doGet() 또는 doPost() 메서드를 호출한다.

6. protected doGet(HttpServletRequest request, HttpServletResponse response)

7. doGet() 또는 doPost() 메서드는 인자에 맞게 생성된 적절한 동적 페이지를 Response 객체에 담아 WAS에 전달한다.

8. WAS는 Response 객체를 HttpResponse 형태로 바꾸어 Web Server에 전달한다.

9. 생성된 Thread를 종료하고, HttpServletRequest와 HttpServletResponse 객체를 제거한다.
```

---

## WebServer를 사용하는 이유

WAS가 WebServer의 역할도 할 수 있다. 그럼에도 WebServer를 사용하는 이유는 무엇인가?

WebServer는 단순한 정적 콘텐츠만 제공한다. 그렇기 때문에 WAS보다 빠르고 서버에 부하가 덜 가해진다. 따라서 서버의 부하를 줄이기 위해 WebServer가 필요하다.
