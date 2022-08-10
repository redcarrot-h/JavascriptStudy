# 자바스크립트 기초 강좌

## 1. 변수
문자열은 홑이든 겹이든 따옴표를 감싸야 함.
변수명은 예약어를 쓸 수 없음(ex)class)

### let
let은 최초로 선언할 때 기존에 선언한 값이 있으면 에러 메시지가 떠서 인지하기 쉬움, 
단 해당 변수명은 let을 생략하고 작성하면 수정이 가능함.

``` js
let grade = "F";
// ... 1000 lines

grade= "A+";
```
### const
const는 절대로 바뀌지 않는 상수, 수정 x, 대문자로 선언하는 경우가 많다.   
ex) const PI=3.14; const SPEED_LIMIT=50; const BIRTH_DAY='2020-01-01';


### 정리
자바스크립트에서 변수를 선언할때는, 변하지 않는 값은 const, 변할 수 있는 값은 let으로 선언하세요.  
tip) 모든 변수를 const로 선언 후에 변경이 필요한 것을 let으로 바꾸면 됨.

첫째, 변수는 문자와 숫자, $와 __만 사용 ex)const MY_HOME="..."; let_=1; let$=3;  
둘째, 첫글자는 숫자가 될 수 없습니다. ex) let 1stGrade = 'A+';(불가)    
셋째, 예약어는 사용할 수 없습니다. ex) let let = 99;(불가).  
넷째, 가급적 상수는 대문자로 알려주세요. ex) const MAX_SIZE = 99;   
다섯째, 변수명은 읽기 쉽고 이해할 수 있게 선언. ex) let a = 1;(불가), let userNumber = 3; (가능)



## 2. 자료형
```js
const name = "Mike"; // 문자형 String
const age = 30;

const name1 = "Mike"
const name2 = 'Mike'
const name3 = `Mike`

const message = "I'm a boy.";
const massage2 = 'I\'m a boy.';

const message3 = `My name is ${name}`; 
// 백틱이 아닌 일반 따옴표를 쓰면 변수명이 그대로 노출되기 때문에 주의필요
console.log(message3)

const message4 = `나는 ${30+1}살 입니다.`;
console.log(message4);

const name = "Mike";

const a = "나는 ";
const b = " 입니다.";

console.log(a + name + b);

const age = 30; // number
console.log(a+ age + "살" + b);
// 문자형 + 숫자형을 합치면 문자형으로 변경
```

``` js
const age = 30; // 숫자형 Number
const PI = 3.14;

console.log(1 + 2); //더하기
console.log(10 - 3); // 빼기
console.log(3 * 2); // * 곱하기
console.log(6 / 3); // / 나누기
console.log(6 % 4); // % 나머지

const x = 1/0; // ???
const y = name/2;

console.log(y)

// NaN = Not a number
```

``` js
// Boolean

const a = true; //참
const b = false; // 거짓

const name = "Mike";
const age = 30;

console.log(name == 'Mike');
console.log(age > 40)
```

``` js
// null 과 undefined 

let age;
console.log(age) // undefined

let user = null; //유저는 존재하지 않는다.

// 객체형(이후 수업)
// 심볼형(이후 수업)
```

``` js
// typeof 연산자

const name = "Mike";

console.log(typeof 3);
console.log(typeof name);
console.log(typeof true);
console.log(typeof "xxx");
console.log(typeof null);
console.log(typeof undefined);
```

### typeof
typeof null; // object 객체형    
null != 객체가 아닙니다. 