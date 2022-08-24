# 반복문 loop
반복문 loop: 동일한 작업을 여러번 반복

## for
``` js
for(let i = 0; i < 10; i++){
	// 반복할 코드
}
```

``` js
for(1번 초기값; 2번, 5번, 8번 조건;(false가 되면 멈춤); 4번, 7번 코드 실행 후 작업){
	// 3번, 6번 반복할 코드 (i=0, i가 10보다 작으므로 코드실행 i값 1증가, i =1, i가 10보다 작으므로 코드실행)}

``` js
// 1 부터 10까지 로그, 만약 로그값을 i로 설정하면 0부터 9까지 출력됨

for(let i = 0; i < 10; i++){
  console.log(i+1)
}
```

## while
```js
let i =0;
while(i<10){
	//코드
	i++
}
```
``` js
// while

let i = 0;

while(i<10){
  console.log(i);
  i++;
}
```

## do.. while
```js
let i = 0;

do{
	//코드
	i++;(1번)
} while (i < 10)(2번)
```

## break, continue
 - break : 멈추고 빠져나옴
 - continue : 멈추고 다음 반복으로 진행


``` js
// break

while(true){
  let answer = confirm('계속 할까요?');
  if(!answer){
    break;
  }
}
```

```js
// continue
// 짝수만(0,2,4,6,8)

for(let i = 0; i < 10; i++){
  if(i%2){
    continue;
  } console.log(i)
}
```

## 팁 : 횟수가 정해져있으면 for문을, 정해진 횟수가 없는 경우에는 while를 쓰는 경우가 많음, do while문은 거의 사용하지 않음.

## switch

```js
switch(평가){
	case A :
	// A일때 코드
	case B :
	// B일때 코드
	...
}
```

```js
if(평가 == A){
	// A일때 코드
} else if(평가 == B){
	// B일때 코드
}
```
위 아래 코드는 같은 코드

``` js
// 사과 : 100원
// 바나나 : 200원
// 키위 : 300원
// 멜론 : 500원
// 수박 : 500원
// 사고 싶은 과일을 물어보고 가격 알려주기

let fruit = prompt('무슨 과일을 사고 싶나요?');

switch(fruit){
  case '사과' :
    console.log('100원 입니다.');
    break;
  case '바나나' :
    console.log('200원 입니다.');
    break;
  case '키위' :
    console.log('300원 입니다.');
    break;
  case '멜론' :
  case '수박' :
    console.log('500원 입니다.');
    break;
// 같은 값을 실행할 수 있을때는 case를 연이어 작성해도 됨
  default : 
    console.log('그런 과일은 없습니다.');
// default는 if문에서 else와 같은 기능
}

// case는 해당되는 코드 이후의 코드를 모두 실행하기 때문에 break를 넣어줘야 함.
```