# 기본 연산자(Operators)
 '+ 더하기.   
 '- 빼기.   
 '* 곱하기    
/ 나누기  
% 나머지

## 나머지(%)를 어디에 쓸까?   
홀수 : X % 2 = 1  
짝수 : Y % 2 = 0

어떤 값이 들어와도 5를 넘기면 안돼    
X % 5 = 0 ~ 4 사이의 값만 반환

## 거듭제곱
``` js
const num = 2 ** 3;    
console.log(num); // 8
```

## 우선순위 
*(곱하기) /(나누기) > +(더하기) -(빼기) 

## 연산자 줄여서 쓰기
``` js
// 연산자 줄여서 쓰기

let num = 10;
// num = num + 5; *와 -, %도 가능
num += 5;

console.log(num);
```

## 증가 연산자, 감소 연산자
``` js
// 증가 연산자, 감소 연산자

let num = 10;
let result = ++num;
// ++ 로 적거나 --로 적으면 됨, 뒤에 연산자를 넣으면 증가시키기 전의 값을 결과로 넣음. 앞에 연산자를 쓰면 증가시킨 값을 결과로 넣음

console.log(result);
```

# 비교 연산자, 조건문

## 비교 연산자
< > <= >= == !=

a = 3 // 할당을 의미함
a != 3 // true or false

``` js
console.log(10>5); //true
console.log(10 == 5); //false, 동등연산자
console.log(10 != 5); // true
```

### 동등연산자
``` js
// 동등 연산자

const a = 1;
const b = "1";

console.log(a == b); // true로 출력, 하지만 ===(일치 연산자)은 타입까지 비교함
```

## 조건문

### if문

``` js
if(age > 19){
	console.log('환영합니다.');
}

if(age <= 19){
	console.log('안녕히가세요.');
}
// {}는 생략가능하지만 가독성을 위해 항상 써주는 것이 좋음, if 뒤에 괄호()안에 값은 항상 불린형이어야 한다.

```

``` js
// if, else, else if
// 추가 요구사항 : 
// 19살이면 수능 잘치세요 라는 문구를 보여주세요
// age === 19

const age = 19;

if(age > 19) {
  console.log('환영합니다.');
} else if(age === 19) {
  console.log('수능 잘치세요.');
} else { console.log('안녕히 가세요.');
}

console.log('-------------------')
```
