## chapter3_함수

함수의 구성 요소

keyword (함수에 정의할 이름)
name (사용 목적에 맞는 이름)    
parameter (사용자가 입력 한 값(변수))
body (사용자가 입력(호출)을 하였을때 작동하는 부분)

 

 

함수의 의미

코드의 묶음 (즐겨찾기 버튼)
기능의(function) 단위
입력과 출력간의 매핑(mapping)
호출 후에는 반드시 돌아온다 (return)

 

함수의 사용법

1. 버튼제작
선언 (declaration)
```js 
function cal(param1, param2) {

console.log(param1 + param2);

return param1 * 10;
}
```
 

2. 버튼 사용
호출 (call, invocation)
cal(10, 20);

 

함수가 어떻게 평가 되는지 확인.

```js
let result = cal(10, 20);

function cal(param1, param2) {

console.log(param1 + param2);

return param1 * 10;
}
```
 

위 예제를 토대로 parameter에 적용된 값

```js
let result = cal(10, 20);

function cal(10, 20) {

console.log(10+20);

return 10 * 10;

}
```
 

함수는 return 값을 반환하게 되어 있어서
100이라는 값을 출력하고 종료하게 된다.



함수의 기초

함수란? 
어떤 목적을 가진 작업들을 수행하는 코드들이 모인 블록
함수는 항상 출력값을 반환하고 return 값을 입력 하지 않으면
undefined라는 값이 출력 된다.

또는 지시사항의 묶음이라고 할 수도 있다.

함수 선언 방법

함수 선언식

```js
function getTriangleArea(base, height) {
let triangleArea = (base * height) / 2;
return triangleArea
}
```

특징
1. 함수 선언 방식은 함수 리터럴 형식과 같다.
*함수 리터럴 이란 함수를 선언함과 동시에 값 또는 
코드를 지정해 주는 것을 말함.
2. 함수 선언문은 반드시 함수 이름이 명시되어 있어야 한다.
3. 함수 이름으로 함수를 호출한다.

```js
   ex) getTriangleArea();
   ```

함수 표현식

```js
const getTriangleArea = function (base, height) {
//변수 getTriangeArea에 함수 할당
let triangleArea = (base * height) / 2;
return triangleArea
}
```

특징
1. 함수 리터럴로 생성한 함수를 변수에 할당하는 방법을 함수 표현식이라고 한다.
함수의 참조값이 getTriangleArea라는 변수로 저장된다.

2. 위 예에서 getTriangleArea는 함수의 이름이 아니다. funtion은 익명함수이고 함수가
할당된 변수인 getTriangleArea를 통해 호출할 수 있다. ex) getTriangleArea(); 

3. 함수 표현식에서 const getTriangleArea = function getTriangle() {......}과 같이 
함수에 이름이 지정되었다고 하더라도 변수 이름을 사용하여 함수를 호출해야한다.
단, 함수에 이름을 정하면 코드를 디버깅 할 때 도움이 된다.

4. 함수 표현식에서 함수 이름을 지정하였다고 하여도, 호출 방식에는 영향을 미치지 않는다.

화살표 함수

```js
const getTriangleArea = (base, height) => {
let triangleArea = base * height / 2;
return triangleArea;
};
```

특징
1. 함수 표현식보다 단순하고 간결한 문법으로 함수를 만들 수 있는 방법.
2. 함수 내부의 코드가 한줄일 경우에는 retrun과 중괄호를 생략 할 수 있다.

```js
ex) 
const getTriangleArea = (base, height) => base * height / 2;
```

함수란?

1급객체 - 함수의 특징 특등시민

함수를 인자로 받을 수 있음
함수의 형태로 매개변수로 호출 할 수도 있음 
함수를 변수에 담을 수도 있음