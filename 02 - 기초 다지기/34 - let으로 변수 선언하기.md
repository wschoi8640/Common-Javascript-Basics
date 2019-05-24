# let으로 변수 선언하기

* ES6 이전에는 var 키워드로만 변수를 정의할 수 있었습니다.

* ES6에서는 let 키워드가 나오면서 변수 선언시 유효범위를 블록 범위로 지정할 수 있게 되었습니다.

```javascript
if (true) {
    var functionScopeValue = 'global';
    let blockScopeValue = 'local';
}
console.log(functionScopeValue);
console.log(blockScopeValue);
```

```
global
Uncaught ReferenceError : blockScopeValue is not defined
```

---

* let은 var과는 달리 호이스팅으로 undefined 값이 할당되기 보다는 블록 시작부터 선언이 이루어진 라인까지 접근을 막습니다.

* 해당 영역에서 변수에 접근을 하게 되면 에러가 발생합니다.

```javascript
let value = "바깥값";
if (true) {
    console.log(value);
    let value = "안쪽값";
}
```

```
Uncaught ReferenceError : value is not defined
```
