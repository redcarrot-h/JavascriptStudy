# 논리 연산자
- || (OR) : 여러개 중 하나라도 true면 true 즉, 모든값이 false 일때만 false를 반환

- &&(AND) : 모든값이 true면 true 즉, 하나라도 false면 false를 반환

- ! (NOT) : true면 false false면 true

ex) 스티브 잡스는 한국인 이거나 OR, 남자이다. -true.  
스티브 잡스는 한국인 이고 AND, 남자이다. - false

## 평가
- OR는 첫번째 true를 발견하는 즉시 평가를 멈춤
- AND는 첫번째 false를 발견하는 즉시 평가를 멈춤

- 운전면허가 있고(전체 군인의 80%) 시력이 좋은(전체 군인의 60%) 여군(전체 군인의 7%)  
-> 여군인데 시력이 좋고 운전면허가 있는 사람으로 코드를 짜면 좀 더 효율적이다.

## ||(OR)
a || b // a나 b 중 true가 있으면 true

``` js
// OR
// 이름이 TOM 이거나, 성인이면 통과

const name = "Mike";
const age = 30;

if(name === 'Tom' || age > 19){
  console.log('통과');
}
```

## &&(AND)
a && b // a와 b 둘 다 true 이면 true
``` js
// AND
// 이름이 Mike이면서 성인이면 통과

const name = "TOM";
const age = 30;

if(name === 'Mike' && age > 19){
  console.log('통과');
} else {
  console.log('돌아가.')
}
// 마이크가 아니고 성인이기 때문에 돌아가로 뜸
```


## !(NOT)
!a // a가 false 이면 true

```js
// NOT
// 나이를 입력받아 성인이 아니면 돌아가라고...

const age = prompt('나이가,,?');
const isAge = age > 19;

if(!isAge){
  console.log('돌아가..')
}

console.log('----------')
```

## 우선순위
``` js
// 우선순위
// 남자이고, 이름이 Mike 이거나 성인이면 통과


const gender = 'F';
const name = 'Jame';
const isAdult = true;

//if(gender === 'M' && name === 'Mike' || isAdult){ 이구문은 아래 구문과 동일함
 //if((gender === 'M' && name === 'Mike') || isAdult){
if(gender === 'M' && (name === 'Mike'|| isAdult)){
  console.log('통과')
} else{
  console.log('돌아가.')
}
// 우선순위 && > || 
```

```js
// 우선순위
// 남자이고, 이름이 Mike 이거나 성인이면 통과


const gender = 'M';
const name = 'Jame';
const isAdult = true;

if(gender === 'M' && (name === 'Mike'|| isAdult)){
  console.log('통과')
} else{
  console.log('돌아가.')
}
// 통과로 출력 
```



