## chapter4_조건문

조건문 기초

Boolean 타입에 대한 이해가 필요함.

let isAdult = true; // 또는 fales
let isStudent = fales; // 또는 true

*조건문은 어떠한 조건을 판별하는 기준을 만드는 것
*조건문에는 반드시 비교연산자(comparison operator)가
필요함.

비교연산자

```js
3 > 5; // false
9 < 10 // true
'hello' === 'world'; // false
```

비교의 결과는 늘 Boolean, 즉 true 혹은 false 이다.

비교연산자

```
> 초과
< 미만
>= 이상
<= 이하
=== 같다
!== 다르다.
```

권장하지 않는 연산자

이유
1.왼쪽과 오른쪽의 타입을 엄격하게 비교하지 않음
2. 원치 않는 예외 케이스가 많음

```
== 같다.
!= 다르다.
```

조건문

```js
if (조건1) {
// 조건1이 통과할 경우
} else if (조건 2) {
// 조건1이 통과하지 않고
// 조건2가 통과할 경우
} else {
// 모든 조건이 통과하지 않는 경우
}

* 조건에는 Boolean 으로 결과가 나오는 비교문이 들어간다.
```

유용한 예

두가지 조건이 한번에 적용되는 경우는 
논리 연산자(Logical Operator)를 사용

```js
학생이면서, 여성일 때 통과
AND 연삱자
isStudent && isFemale;

학생이거나, 여성일 때 통과
OR 연산자
isStudent || isFemale;

학생이 아니면서, 여성일 때 통과
NOT 연산자 (!는 true, false 여부를 반전시킴)
!isStudent && isFemale;
```
논리 연산자 NOT

```js
!false // true
!(3>2) // false
!undefined // true
!'hello' // false
```
논리 연산자 OR
둘중 하나만 true 이면 true

```js
true || true // true
true || false // true
false || false // false
```

논리 연산자 AND
둘다 true 일 때만 true

```js
true && true // true
true && false // false
false && true // false
```
 

*기억해야 할 6가지 falsy 값

   다음은 if 문에서 false로 변환되므로, if 구문이 실행되지 않음.

   if (false)          // false

   if (null)           // null은 값이 없다

   if (undefined)   // 정의되지 않음

   if (0)              // 0은 on/off 기능에서 off를 의미

   if (NaN)          // NaN 은 Not a Number를 의미하는 키워드

   if ('')               // 비어있는 문자열