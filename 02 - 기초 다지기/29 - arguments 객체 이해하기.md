# arguments 객체 이해하기

* javascript 에는 매개변수와 함께 사용되는 전달인자(arguments)라는 개념이 있습니다.

* 매개변수가 함수 선언시 작성되는 변수라면, 전달인자는 함수가 호출될 시 전달되는 값입니다.

* javascript는 매개변수와 전달인자의 갯수가 일치하지 않아도 에러를 발생시키지 않습니다.

* 이를 처리하기 위해 사용되는 객체가 arguments 입니다.

```javascript
function sum(){
  var total = 0;
  for(var i = 0; i < arguments.length; i++){
    total += arguments[i];
  }
  console.log(arguments instanceof Arrray);
  return total
}

var sumOf1to3 = sum(1,2,3);
console.log(sumOf1to3);

function testArg(){
  var newArr = Array.prototype.slice.call(arguments);
  console.log(newArr);
  console.log(newArr.indexOf('b'));
  console.log(arguments.indexOf('b'));
}

testArg{'a','b');
```

* arguments 는 배열 객체가 아닙니다.

* arguments 는 length 속성을 가지고 있습니다.

* arguments 를 배열로 사용하기 위해서는 prototpye 객체의 slice 메소드를 사용해야 합니다.

```
false
6
["a", "b"]
1
Uncaught TypeError : arguments.indexOf is not a function
```
