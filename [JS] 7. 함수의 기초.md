# 함수(function)

## 함수(function)의 기초

### 함수의 기본 구조

``` js
함수의 기본 구조
function(함수) sayHello(함수명)(name)(매개변수){
	console.log(`Hello, ${name}`);
}
함수의 호출
sayHello('Mike');
```

```js
// 함수 작성

function showError(){
  alert('에러가 발생했습니다. 다시 시도해주세요.');
}

showError();
```

### 지역변수

```js
// 함수 작성
// 매개변수가 있는 함수

function sayHello(name){
  const msg = `Hello, ${name}`;
  console.log(msg);
}

sayHello('Mike');
sayHello('Tom');
sayHello('Jane');
```

```js
// 함수 작성
// 매개변수가 있는 함수

function sayHello(name){
  let msg = `Hello`;
  if(name){
    msg += `, ${name}`;
  }
  console.log(msg);
}

sayHello();
sayHello('Mike');
console.log(msg)

// 지역변수 msg를 함수 밖에서 호출하면 에러가 뜸
```

### 전역변수
``` js
// 함수 작성
// 매개변수가 있는 함수

let msg = `Hello`; // 전역 변수(global varable)

console.log('함수 호출 전')
console.log(msg)

function sayHello(name){
  if(name){
    msg += `, ${name}`;
  }
  console.log('함수 내부')
  // 지역 변수(local varable)
  console.log(msg);
}

sayHello('Mike');
console.log('함수 호출 후')
console.log(msg)
```

```js
// 전역 변수와 지역 변수

let msg = "welcome";
console.log(msg)

function sayHello(name){
  let msg = "Hello"
  console.log(msg + ' ' + name);
}

sayHello('Mike');
console.log(msg)

//출력 :  "welcome" "Hello Mike" "welcome"
//전역변수 let과 지역변수 let은 서로 간섭을 받지 않음
```

```js
// 전역 변수와 지역 변수

let name = "Mike";

function sayHello(name){
  console.log(name)
}

sayHello();
sayHello('Jane');

// 전역변수로 선언한 매개변수가 지역변수로 넣어서 undefined와 Jane으로 출력이 됨, 
//전역변수가 많아지면 혼선이 생길 수 있으니 함수 내에 지역변수를 쓰는 습관을 들이는 것이 좋다.
```

### 함수의 응용(OR)

``` js
// OR

function sayHello(name){
  let newName = name || 'friend';
  let msg = `Hello, ${newName}`
  console.log(msg)
  }

sayHello();
sayHello('Jane');

// 매개 변수가 없으면 undefined 대신에 friend가 들어감
```
### 함수의 응용(default value 설정)
``` js
// default value

function sayHello(name = 'friend'){
  let msg = `Hello, ${name}`
  console.log(msg)
  }

sayHello();
sayHello('Jane');
// 디폴트값을 friend로 설정하면 코드가 깔끔해짐
```

### return으로 반환

```js
// return 으로 값 반환

function add(num1, num2){
  return num1 + num2;
}

const result = add(2,3);
console.log(result)
```

```js
// return 으로 값 반환

function showError(){
  alert('에러가 발생했습니다.');
 return;
  alert('이 코드는 절대 실행되지 않습니다.');
}
const result = showError();
console.log(result);

// return문이 없거나 return만 있으면 undefined를 반환한다. return만 쓰는 경우 종료 목적으로 쓰기도 함. 그래서 return뒤에 있는 코드는 실행이 안됨
```

### 함수(function) 관련 팀
 - 한번에 한 작업에 집중하는 것이 좋다. 
 - 읽기 쉽고 어떤 동장인지 알 수 있게 네이밍.  
	showError // 에러를 보여줌.  
 	getName // 이름을 얻어옴.  
	createUserData // 유저데이터 생성.  
	checkLogin // 로그인 여부 체크