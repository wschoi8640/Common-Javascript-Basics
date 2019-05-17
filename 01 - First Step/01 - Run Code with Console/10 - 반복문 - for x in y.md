# 반복문 - for x in y

```javascript
var store = {snack: 1000, flower: 5000, beverage: 2000};

for(var item in store) {
  if(!store.hasOwnProperty(item)) continue;
  
  console.log(item + '는 가격이 ' + store[item] + '입니다.');
}
```

* for - in 반복문을 사용할 때는 hasOwnProperty를 통해 객체 안에 속성이 있는지 확인하는 것을 권장합니다.
