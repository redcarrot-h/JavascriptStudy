## 함수표현식, 화살표 함수

### 함수 선언문 vs 함수 표현식

```js
sayHello();
function sayHello(){
	console.log('Hello');
}

// 이를 함수 선언문이라고 함, 어디서든 호출 가능
// 예를 들어 sayHello(); 호출을 선언 상단에 위치해도 동작을 함, 왜냐하면 눈으로 봤을때는 저 모습이지만 자바스크립트 내부 알고리즘으로 인해 초기화 단계에서 코드에 선언된 모든 함수 모임을 먼저 찾아서 생성 해놓는다. 이에 함수에 대한 사용가능 범위가 늘어나서 가능함. 이를 호이스팅(hoisting)이라고 한다. 코드위치가 실제로 올라간다는 뜻은 아님!
```

* 인터프리터 언어(Interpreted language) : 순차적으로 실행하고 즉시 결과를 반환하는 프로그래밍 언어를 인터프리터 언어라고 함 Ex)js

```js
let sayHello = function(){ 생성 
	console.log('Hello'); 사용가능
}
sayHello();
// 이를 함수 표현식이라고 함, 코드에 도달하면 생성
```
- 그래서 뭘 쓰는 것이 좋은가? 
함수선언문이 좀 더 자유롭게 코딩할 수 있어서 더 많이 쓰임.

### 화살표 함수(arrow function)
```js
let add = function(num1, num2){
	return num1 + num2;
}
이를 화살표 함수로 바꾸면
let add =(num1, num2) => {
	return num1 + num2;
}

코드본문이 한줄이고 return문이 있으면 아래와 같이 일반괄호로 변경 가능
let add = (num1, num2) => (num1 + num2;)

return문이 한줄이라면 아래와 같이 생략 가능
let add = (num1, num2) => num1 + num2;

인수가 딱 하나라면 () 괄호를 아래와 같이 쓸 수 있음
let sayHelllo = name => `Hello, ${name}`;

만약 인수가 없는 함수라면 이때는 괄호를 생략할 수 없음
let showError = () => {
	alert('error!');
}

또한 return문이 있다고 하더라도 return 전에 여러개의 코드가 있을 경우 일반 괄호()를 사용할 수 없음
let add = function(num1, num2){
	const result = num1 + num2;
	return result;
}
```

```js
// 함수 선언문

showError();

function showError(){
  console.log('error');
}

// 화살표 함수로 변경하면?!

let showError = () => {
  console.log('error');
}

showError();
```

``` js
// 화살표 함수(다른 예시)

const sayHello = (name) => {
  const msg = `Hello, ${name}`;
  console.log(msg);
}

sayHello('Mike');
```
```js
// 화살표 함수(인수2개, return문이 있음)

const add = function(num1, num2){
  const result = num1 + num2;
  return result;
};

console.log(add(1,2));

//이를 화살표 함수로 변경하면?
const add = (num1, num2) => (num1 + num2);

console.log(add(1,2));
```
