함수에서 입력받는 값에 대한 정의를 Parameter라고 한다.

실제 입력하는 값은 arguement라고 한다.

```javascript
function calculate(number) {
    console.log((number * 10 / 2 % 3).toString())
}

calculate(4)
```

위 코드에서 number가 parameter, 4가 arguement이다.

## return 키워드

함수에서 arguement값들의 연산을 반환받고 싶을 때 return을 사용한다.

```javascript
// 반환받기
// return 받기
function multiply(x, y) {
    return x * y
}

const result1 = multiply(2, 4)
console.log(result1)

const result2 = multiply(4, 5)
console.log(result2)
```

출력 결과

8

20

## 화살표(Arrow)함수

```javascript
// Arrow함수(화살표 함수)
const multiply2 = (x, y) => {
    return x * y
}
console.log(multiply2(3, 4))

const multiply3 = (x, y) => x*y
console.log(multiply3(4, 5))
```

당장은 일반적인 함수와 큰 차이 없음

multiply2와 multiply3은 똑같은 함수임

괄호 안 파라미터가 1개면 괄호는 생략해도 됨

```javascript
const multiply4 = x => x*2
console.log(multiply4(2))
```

```javascript
const multiply5 = x => y => z => `x: ${x} y: ${y} z: ${z}`
console.log(multiply5(2)(5)(7))

function multiply6(x) {
    return function(y){
        return function(z){
            return `x: ${x} y: ${y} x: ${z}`
        }
    }
}
console.log(multiply6(3, 4, 5))
```

multiply5의 구조를 보여준 것이 multiply6

일반함수도 arrow함수처럼 변수선언 하듯이 함수선언이 가능하다.

```javascript
const multiplyTwo = function(x, y) {
    return x * y
}
console.log(multiplyTwo(4, 5))
```

이런 식으로 사용하면 된다.

## arguements 키워드

```javascript
const multiplyThree = function(x, y, z) {
    console.log(arguments)
    return x * y * z
}
console.log(multiplyThree(4, 5, 6))
```

출력 결과

[Arguments] { ‘0’ :  4, ‘1’ :  5, ‘2’ :  6 }

120

### arguements 사용하기

```javascript
const multiplyAll = function(...arguments) {
    return Object.values(arguments).reduce((a, b) => a * b, 1)
}
console.log(multiplyAll(3, 4, 5, 6, 7, 8, 9, 10))
```

출력 결과

18814400

정의와 동시에 실행시키고 싶다면

```javascript
// Immediatly Invoked function Expression
(function(x, y) {
    console.log(x * y)
})()
```

이런 식으로 사용하면 된다.

## 함수의 타입

```javascript
console.log(typeof multiply)
console.log(multiply instanceof Object)
```

출력 결과

function

true

함수는 object이기 때문에 출력 결과가 저렇다.

※지금 당장은 instanceof가 좌측에 있는 게 우측과 같은 타입인지 질문하는 키워드라 생각

전체 코드

```javascript
// function -> 함수

// 만약 2라는 숫자에 * 10 / 2 % 3 스트링으로 변환해서
// 반환받고 싶다면 어떻게 해야할까?
console.log((2 * 10 / 2 % 3).toString())
console.log((3 * 10 / 2 % 3).toString())

function calculate() {
    console.log((2 * 10 / 2 % 3).toString())
}

calculate()

function calculate(number) {
    console.log((number * 10 / 2 % 3).toString())
}

calculate(4)
calculate(5)

function multiply(x, y) {
    console.log(x * y)
}

multiply(2, 4)

function multiply(x, y = 10) {
    console.log(x * y)
}

multiply(2, 4)
multiply(2)

// 반환받기
// return 받기

console.log('----------------')

function multiply(x, y) {
    return x * y
}

const result1 = multiply(2, 4)
console.log(result1)

const result2 = multiply(4, 5)
console.log(result2)

// Arrow함수(화살표 함수)
const multiply2 = (x, y) => {
    return x * y
}
console.log(multiply2(3, 4))

const multiply3 = (x, y) => x*y
console.log(multiply3(4, 5))

const multiply4 = x => x*2
console.log(multiply4(2))

const multiply5 = x => y => z => `x: ${x} y: ${y} z: ${z}`
console.log(multiply5(2)(5)(7))

function multiply6(x) {
    return function(y){
        return function(z){
            return `x: ${x} y: ${y} x: ${z}`
        }
    }
}
console.log(multiply6(3, 4, 5))

const multiplyTwo = function(x, y) {
    return x * y
}
console.log(multiplyTwo(4, 5))

console.log('----------------')

const multiplyThree = function(x, y, z) {
    console.log(arguments)
    return x * y * z
}
console.log(multiplyThree(4, 5, 6))

const multiplyAll = function(...arguments) {
    return Object.values(arguments).reduce((a, b) => a * b, 1)
}
console.log(multiplyAll(3, 4, 5, 6, 7, 8, 9, 10))

// Immediatly Invoked function Expression
// (function(x, y) {
//     console.log(x * y);
// })(4, 5)

console.log(typeof multiply)
console.log(multiply instanceof Object)
```