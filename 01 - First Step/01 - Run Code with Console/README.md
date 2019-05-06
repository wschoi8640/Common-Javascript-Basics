# 콘솔로 코드 실행하기

```javascript
document.createElement('div');
var element_div = document.createElement('div');
element_div.id = 'div_name';
```

1. document.createElement('div') 를 입력하면, 'div'로 지정된 태그 이름으로 엘리멘트를 생성합니다.

2. var 키워드로 변수 element_div에 document.createElement('div')를 대입하여 입력하면, 변수의 값이 출력
되지 않고 undefined가 보입니다. 이는 브라우저 내부메모리에 변수 div를 저장했기 때문입니다.

3. element_div.id에 'div_name'을 입력하면 'div_name'이 출력됩니다. 이는 div 태그에 id를 추가한 것과 동일
합니다.

```javascript
1+12
x = 5
var foo = 'hello'
console.log(foo);
```

1. 1+12 에 대한 결과값 13이 출력됩니다.

2. 임의의 변수 x에 5를 대입하면 변수의 값이 출력됩니다.

3-4. 변수 foo에 'hello'문자열을 대입한후 log로 foo를 출력하면 입력된 값이 출력됩니다.

* index.html
```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8">
    <title>Daily Javascript</title>
  </head>
  <body>
    <script type="text/javascript" src="./003.js></script>
  </body>
</html>
```

* 003.js
```javascript
console.log('html로 코드 실행해보기');
var a = 5;
var b = 2;
console.log(a + b);
```

* html 이 실행되면 script에서 불러온 js파일이 실행됩니다.

# 값과 변수 이해하기

```javascript
var name = 'Peter';
var number = 200;
var isTrue = true;
var nothing = null;
var empty = undefined;
var list = [ ];
var ref = { };
var func = function(){}
```

* 선언 키워드 - 자바스크립트는 다른 언어와는 달리 변수 타입을 지정해주지 않아도 됩니다. 런타임시 변수의 값에 의해 타입이 동적으로
결정됩니다. 이를 동적 바인딩(Dynamic Binding)이라고 합니다.

* 변수명 - 변수를 선언할 시 var 다음에 변수명을 작성합니다. 변수명은 자유이지만 키워드(문법 용어)를 변수명으로 지정하면 에러가 발생합니다.

* 값 - 자바스크립트는 다양한 값을 변수에 대입할 수 있습니다. 단일 자료형부터 표현식, 함수까지 대입할 수 있습니다.

# 표현식과 명령문

## Expression(표현식)

```javascript
(3 + 12) / 5
declaredVariable
greeting('hello')
```

* 표현식은 값을 생성합니다. 연산자를 통해 값을 생성하거나, 변수 또는 함수 인자로 값을 넣을때 표현식을 사용합니다.

## Statement(명령문)

```javascript
if(true){
// do something
}
```

* 명령문은 행동을 수행하게 하는 코드입니다. 명령문에는 if, for, switch 등이 있습니다.

## Expression Statement(표현식 명령문)

```javascript
function greeting(){
  "hello"
  "Chloe" + 3
  greeting()
}
```

* 명령문은 때로는 표현식으로 대체 될 수 있습니다. 

# 주석 처리하기

```javascript
// x 변수에 'a' 값을 할당하여 선언합니다.
var x = 'a';
console.log(x);

/*
x = 'b';
console.log(b);
*/
```

* javascript는 한줄 주석과 블록 주석을 지원합니다.

# 자료형 이해하기

```javascript
var x = 5; // 숫자형
var y = 'five'; // 문자형
var isTrue = true; // Boolean
var empty = null; // null
var nothing // undefined
var sym = Symbol('me'); // Symbol

var item = {
  price : 5000,
  count : 10
}; // 객체
var fruits = ['apple', 'orange', 'kiwi']; // 배열
var addFruit = function(fruit) {
  fruits.push(fruit);
} // 함수
addFruit('watermelon');
console.log(fruits);
```

* 원시 데이터 : 숫자형, 문자형, Boolean, Symbol, null, undefined (null은 빈 값, undefined는 값이 없음)

* 참조 데이터 : 값을 저장하지 않고 메모리 주소를 참조. 객체는 참조 데이터

* 객체 : {}안에 키 : 값 형태로 이루어진 속성들의 모음. 키는 반드시 문자형이어야 하고 키를 통해 값에 접근할 수 있음

* Global Object 객체 : 모든 객체의 부모가 되는 객체 

* 표준 내장 객체 : 함수, 배열, Math, JSON, RegEx... Global Object의 자식 객체

# 콘솔로 자료형 출력하기

```javascript
var str = 'javascript';
var num = 200;
var arr = [1, 2, 3, 4, 5];
var obj = {a: 1, b: 2, c: 3};

console.log(str);
console.log(num);
console.log(arr);
console.log(obj);
```
1. str을 출력하면 'javascript' 문자열이 출력됩니다.

2. num을 출력하면 200이 출력됩니다.

3. arr을 출력하면 배열형값 [1, 2, 3, 4, 5]가 출력됩니다.

4. obj을 출력하면 객체값 {a: 1, b: 2, c: 3}가 출력됩니다.

# 조건문 - if

```javascript
var result = true;
if(result) console.log('result가 참 입니다.');
if(!result) console.log('실행되지 않습니다.');
if(result) {
  console.log('result의 결과');
  console.log('>> 참 입니다.');
}
```
