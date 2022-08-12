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
	i++;
} while (i < 10)
```