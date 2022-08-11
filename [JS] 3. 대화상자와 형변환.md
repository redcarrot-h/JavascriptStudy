# 3. 대화상자

alert 알려줌.  
prompt 입력 받음.  
confirm 확인 받음   

## alert() 
알람창 띄우는 함수, 메시지를 보여줌, 확인버튼을 누르면 없어짐

## prompt()
입력창 띄우는 함수, 입력값을 입력받을 수 있는 필드를 제공함. 두번째 인수를 넣어주면 디폴트 값을 넣어줄 수 있음

``` js
// const name = prompt("이름을 입력하세요.");
// alert("환영합니다, "+ name + "님");

// const name = prompt("이름을 입력하세요.");
// alert(`안녕하세요, ${name}님. 환영합니다.`);

// const name = prompt("이름을 입력하세요.");
// console.log(name)
// 안내창에서 취소를 누르면 null이 뜸

const name = prompt("예약일을 입력해주세요", "2020-10-");
// prompt는 2개의 인수를 가질 수 있음 첫번째 인수는 메시지이고, 두번째 인수는 입력받을 디폴트 값입니다.
```

## confirm()
확인 받는 함수, 확인 버튼은 true 반환, 취소는 false를 반환함.

``` js
const isAdult = confirm("당신은 성인 입니까?");

console.log(isAdult)
// 확인 클릭하면 Console에 true, 취소 클릭하면 Console에 false로 뜸

// 결제 하시겠습니까?
// 정말 삭제 하시겠습니까?

```

## 단점
1. 스크립트 일시 정지
2. 스타일링 X(위치, 모양 변경 안됨)


# 4. 형변환(Type Conversion)

## 형변환 
String() -> 문자형으로 변환  
Number() -> 숫자형으로 변환  
Boolean() -> 불린형으로 변환

## 형변환이 필요한 이유 
prompt 입력하면 문자형으로 입력됨.  
숫자형이 아니더라도 나누기 같은 표현식은 자동으로 변환되어 계산을 함   
ex) "90" + "80" = "9080" /2 = 4540  
"6" / "2" = 3 (자동 형변환)  
자동 형변환이 되면 알 수 없는 에러가 발생할 수 있기 때문에 명시적 형변환을 하는 것이 좋다.

## String()

``` js
console.log(
String(3),
String(true),
String(false),
String(null),
String(undefined)
)
//"3" "true" "false" "null" "undefined"
```

## Number()
``` js
console.log(
 Number(true),
  Number(false)
)
// 숫자형 + 문자형이 되면 NaN으로 반환, true는 1로 변환, false는 0으로 변환됨
```

## Boolean()
false가 되는 케이스
- 숫자0
- 빈 문자열 "
- null
- undefined
- NaN

``` js
console.log(
Boolean(1),
  Boolean(123),
  Boolean("javascript")
)
// true로 반환하는 케이스

console.log(
Boolean(0),
  Boolean(""),
  Boolean(null),
  Boolean(undefined),
  Boolean(NaN)
)
// false로 반환하는 케이스
```

## 정리
String() -> 문자형으로 변환  
Number() -> 숫자형으로 변환, Number("문자") // NaN으로 반환된다는 것을 염두해야 함.  
Boolean() -> 불린형으로 변환, 0, ", null, undefined, NaN -> false가 됨

## 주의사항
그냥 외우기.  
Number(null) // 0  
Number(undefined) // NaN     
Boolean(0) // false.  
Boolean('0') // true.  
Boolean('') //false.  
Boolean(' ') //true, 공백이 있는 것
