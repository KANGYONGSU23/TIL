# break/continue와 레이블

여러 개의 중첩 반복문을 한 번에 빠져나와야 하는 경우가 종종 생기곤 합니다. 이럴 때 레이블을 사용할 수 있습니다.

```jsx
labelName: for (...) {
  ...
}
```

반복문 안에서 break <labelName>문을 사용하면 레이블에 해당하는 반복문을 빠져나올 수 있습니다.

```jsx
outer: for (let i = 0; i < 3; i++) {

  for (let j = 0; j < 3; j++) {

    let input = prompt(`(${i},${j})의 값`, '');

    // 사용자가 아무것도 입력하지 않거나 Cancel 버튼을 누르면 두 반복문 모두를 빠져나옵니다.
    if (!input) break outer; // (*)

    // 입력받은 값을 가지고 무언가를 함
  }
}
alert('완료!');
```