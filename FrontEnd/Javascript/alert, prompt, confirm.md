# alert

사용자가 '확인(OK)'버튼을 누를 때까지 메시지를 보여주는 작은 모달창이 계속 떠있게 됩니다.

```javascript
alert("Hello world!");
```

<img width="50%" src="https://developer.mozilla.org/en-US/docs/Web/API/Window/alert/alerthelloworld.png">

&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;

# confirm

`confirm` 함수는 `매개변수(메시지)`와 확인 및 취소 버튼이 있는 모달 창을 보여줍니다.  
사용자가 확인 버튼을 누르면 **`true`**, 그 외의 경우는 **`false`** 를 반환합니다.

```javascript
confirm("게시글을 삭제하시겠습니까?");
```

<img width="50%" src="https://images.velog.io/images/hyejin4169/post/3c72303b-382d-406b-9d57-2fd7dcb920e6/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-02-17%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2012.13.31.png">

&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;

# prompt

함수가 실행되면 `텍스트 메시지`와 `입력 필드`,&nbsp; `확인` 및 `취소` 버튼이 있는 모달 창을 띄워줍니다.  
함수의 첫 번째 인자에는 사용자에게 보여줄 `문자열`이 입력되고, 두 번째 인자에는 텍스트필드의 `초깃값`이 입력됩니다.
&nbsp;  
`prompt`함수는 사용자가 입력필드에 기재한 **`문자열을 반환`** 합니다. 입력을 취소한 경우는 **`null이 반환`** 됩니다.

```javascript
prompt("title", ["default"]);
```

<img width="50%" src="data:image/png;base64,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">
