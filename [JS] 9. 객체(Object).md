# 객체(Object)

객체는 중괄호로 구성하고 키(key)와 값(value)로 구성된 프로퍼티(property 정보)가 들어갑니다.   
각 프로퍼티는 쉼표로 구분합니다. 마지막 쉼표는 없어도 되지만 수정 삭제 시 용이하기 때문에 있는 것이 나음 

``` js
const superman = {
	name : 'clark',
	age : 33,
}
```

## Object - 접근, 추가, 삭제

1. 객체에 접근을 할때는 점 또는 대괄호를 사용할 수 있다.  
```js
superman.name //'clark'
superman['age'] //33
```

2. 객체에 추가를 할때도 점 또는 대괄호를 사용할 수 있다.
``` js
superman.gender = 'male';
superman['hairColor'] = 'black';
```

3. 객체를 삭제할때는 삭제하고픈 프로퍼티 앞에 delete 키워드를 사용하면 됨
``` js
delete superman.hairColor;
```

## Object - 단축 프로퍼티
``` js
// 예시 값
const name = 'clark';
const age = 33;

// 예시 객체
const superman = {
	name : name,
	age : age,
	gender : 'male',
}

// 예시 객체는 아래와 같이 쓸 수 있음
const superman = {
	name, // name : name
	age, // age : age
	gender : 'male',
}

```

## Object - 프로퍼티 존재 여부 확인
``` js
const superman = {
	name : 'clark',
	age: 33,
}

superman.birthDay; // 존재하지 않은 프로퍼티에 접근하면 undefined

//in 연산자를 사용하면 프로퍼티에 있는지 확인이 가능함
'birthDay' in superman;
//false

'age' in superman;
//true
```

## for ... in 반복문

``` js
for(let key in superman){
	console.log(key)
	console.log(superman[key])
}
```

``` js
// 객체

const superman = {
  name : 'clark',
  age : 30,
}

console.log(superman.name)
console.log(superman['age'])
console.log(superman)
/* Object {
	age: 30,
	name: "clark"
}
이렇게 출력 됨 */
```

``` js
// 객체 추가

const superman = {
  name : 'clark',
  age : 30,
}
superman.hairColor = 'black';
superman['hobby'] = 'football';
console.log(superman)
/* Object {
	age: 30,
	hairColor: "black",
	hobby: "football",
	name: "clark"
}
이렇게 출력 됨 */
```
``` js
// 객체 삭제

const superman = {
  name : 'clark',
  age : 30,
}
delete superman.age;
console.log(superman)
```

```js
// 객체를 반환하는 함수 예시

function makeObject(name, age){
  return {
    name : name,
    age: age,
    hobby: 'football'
  }
}

const Mike = makeObject('Mike', 30);
console.log(Mike)

// 객체를 반환하는 함수 -> 단축형

function makeObject(name, age){
  return {
    name,
    age,
    hobby: 'football'
  }
}

const Mike = makeObject('Mike', 30);
console.log(Mike)
```

```js
// in 이용 예시

function makeObject(name, age){
  return {
    name,
    age,
    hobby: 'football'
  }
}

const Mike = makeObject('Mike', 30);
console.log(Mike);

console.log("age" in Mike); //true
console.log("birthday" in Mike); //false
// 이런 경우는 점이나 대괄호를 이용하여 확인 가능하므로 실용적인 예제라고 할 수 없음

```

```js
// 객체 in

function isAdult(user){
  if(!('age' in user) || // user에 age가 없거나
     user.age < 20){ // 20살 미만이거나
    return false;
  } 
    return true;
}

const Mike = {
  name : 'Mike',
  age : 30
};

const Jane = {
  name : "Jane"
};

console.log(isAdult(Jane)) //false
```

```js
// 객체 for ... in

const Mike = {
  name : "Mike",
  age: 30
};

for(x in Mike){
  console.log(Mike[x]) // Mike['age']
}
// "Mike", 30값이 출력됨
```
