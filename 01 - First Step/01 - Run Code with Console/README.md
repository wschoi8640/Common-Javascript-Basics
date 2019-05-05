# Code Review

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
