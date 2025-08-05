## 타입 변환의 종류

- 명시적
- 암묵적

## 명시적 타입 변환

```javascript
let age = 32

// 명시적
let stringAge = age.toString()
console.log(typeof (stringAge), stringAge)
```

출력 결과

string, 32

위 코드는 number타입인 age를 string타입으로 변환한 것

명시적으로 어떤 타입을 string타입으로 바꿀 때 toString()을 사용한다.

```javascript
// 숫자 타입으로 변환
console.log(typeof parseInt('0'), parseInt('0'))
console.log(typeof parseFloat('0.99'), parseFloat('0.99'))
console.log(typeof + '1', + '1')
```

출력 결과

number, 0

number, 0.99

number, 1

명시적으로 어떤 타입을 number타입으로 바꿀 때 parseInt, parseFloat을 사용한다.

```javascript
// Boolean타입으로 변환
console.log(!!'abcdefghijklmnop')
console.log(!!'')

console.log(!!0)
console.log(!!'0')
console.log(!!'false')
console.log(!!false)
console.log(!!undefined)
console.log(!!null)

console.log(!!{})
console.log(!![])
```

출력 결과

true

false

false

true

true

false

false

true

true

**string값 안에 값이 들어있으면 boolean기준으로 봤을 때 true**다. 또한 **objec**t와 **list**는 언제나 **true를 반홚한다.**

**아무 글자도 없는 string, string에 값이 없거나 0이거나 undefined 혹은 null인 경우, 0인 경우 무조건 false를 반환한다.**

명시적으로 어떤 타입을 boolean타입으로 바꿀 때 !를 사용하는데 **! 한번 사용은 반대를 의미하고 !!는 원래 것의 boolean타입을 의미한다**. boolean타입으로의 변화가 제일 중요하다.

## 암묵적 타입 변환

```javascript
// 암묵적
let age = 32

let test = age + ''
console.log(typeof test, test)
```

출력 결과

string, 32

숫자에 글자를 더하면 string타입이 된다.

또 다른 예시

```javascript
console.log('98' + 2)
console.log('98' * 2)
console.log('98' - 2)
```

출력 결과

982

196

96

첫 번째 경우는 숫자 2가 string타입으로 변환되면서 98 뒤에 2가 붙게 된다.

하지만 두 번째 경우에는 string에는 곱셈이라는 개념이 없어서 string타입인 98이 number타입으로 변환되면서 98 * 2인 196이 나온다.

세 번째 경우는 두 번째 경우와 같다.

암묵적 변환은 잘 사용하지 않는 것이 좋다.

 

전체 코드

```javascript
let age = 32

// 명시적
let stringAge = age.toString()
console.log(typeof (stringAge), stringAge)

let test = age + ''
console.log(typeof test, test)

console.log('98' + 2)
console.log('98' * 2)
console.log('98' - 2)

console.log('----------------')

// 명시적 변환 몇가지 더 배우기
console.log(typeof (99).toString(), (99).toString())
console.log(typeof (true).toString(), (true).toString())
console.log(typeof (Infinity).toString(), (Infinity).toString())

// 숫자 타입으로 변환
console.log(typeof parseInt('0'), parseInt('0'))
console.log(typeof parseFloat('0.99'), parseFloat('0.99'))
console.log(typeof + '1', + '1')

console.log('----------------')

// Boolean타입으로 변환
console.log(!!'abcdefghijklmnop')
console.log(!!'')

console.log(!!0)
console.log(!!'0')
console.log(!!'false')
console.log(!!false)
console.log(!!undefined)
console.log(!!null)

console.log(!!{})
console.log(!![])
```