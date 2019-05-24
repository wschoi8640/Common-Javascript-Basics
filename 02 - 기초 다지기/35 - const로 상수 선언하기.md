# const로 상수 선언하기

* ES6에서 추가된 const 키워드는 let 키워드와 마찬가지로 블록 단위로 스코프를 정의할 수 있습니다.

* 하지만 let과의 차이점은 선언 시 값을 할당해야 하고 이후에 재할당을 할 수 없습니다.

```javascript
const URL = 'http://js.com';
URL = 'https://js.com';

if (true) {
    const URL2 = 'http://js2.com'
}
console.log(URL2);
```

* const로 정의한 상수에 새로운 값을 할당하면 에러가 발생합니다.

* 그리고 const는 관례적으로 대문자로 변수명을 작성합니다.

* const로 작성한 변수는 블록 밖에서 접근할 수 없습니다.

```
Uncaught TypeError: Assignment to constant variable.
```

---

* const로 정의된 CONST_USER는 불변 객체가 아니라서 name 속성에 다른 값을 할당할 수 있습니다.

* const로 배열을 선언하여도 새로운 요소를 추가하거나 변경할 수 있습니다.

```javascript
const USER = {name: 'choi', age: 30};
console.log(USER.name, USER.age);
USER.name = 'kim';
USER.age = '29';
console.log(USER.name, USER.age);
USER = {name: 'park'};
```

```
choi 30
kim 29
Uncaught TypeError : Assignment to constant Variable.
```
