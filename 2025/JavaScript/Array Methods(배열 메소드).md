JAVA의 array를 할 줄 안다면 JavaScript의 Array Methods는 비슷하다.

## push()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// push()
console.log(iveMembers.push('코드팩토리'))
console.log(iveMembers)
```

출력 결과

7

[ '안유진', '가을', '레이', '장원영', '리즈', '이서', '코드팩토리' ]

첫 번째 코드는 **push**를 했을 때 array의 길이를 나타내는 코드이다.

## pop()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// pop()
console.log(iveMembers.pop())
console.log(iveMembers)
```

출력 결과

코드팩토리

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**pop**은 array에 있는 값을 빼는 것이다. **push**와 다르게 parameter에 아무것도 넣지 않아도 된다. 마지막 엘리멘트를 삭제하는 데 사용

## shift()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// shift()
console.log(iveMembers.shift())
console.log(iveMembers)
```

출력 결과

안유진

[ '가을', '레이', '장원영', '리즈', '이서' ]

출력 결과를 보면 알 수 있듯이 **shift**는 **pop**과 비슷하지만 차이점은 맨 앞에 있는 값을 빼내는 것이다.

## unshift()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// unshift()
console.log(iveMembers.unshift('안유진'))
console.log(iveMembers)
```

출력 결과

6

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**unshift**도 출력 결과를 보면 알 수 있듯이 **push**와 굉장히 비슷하지만 차이점은 맨 앞에 값을 넣는다는 것이다.

## splice()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// splice()
console.log(iveMembers.splice(0, 3))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이' ]

[ '장원영', '리즈', '이서' ]

이런 식으로 **splice**는 자르는 것이라고 보면 편하다. **splice**의 매개변수에는 두 개가 들어가는데 첫 번째 매개변수에는 index, 두 번째 매개변수에는 자를 개수를 적어주면 된다.

## concat()

```javascript
iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// concat()
console.log(iveMembers.concat('코드팩토리'))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이', '장원영', '리즈', '이서', '코드팩토리' ]

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**concat**은 배열에 값을 넣는 것처럼 보여 **push**와 비슷하다고 생각할 수 있지만 **concat**은 새로운 array를 만들어서 반환을 해주는 것이다. 위 코드에서는 끝에 ‘코드팩토리’라는 글자가 붙은 array를 새로 만들어서 반환해준다.

아예 다른 메모리 공간에 저장된 값이 반환된다.

## slice()

```javascript
// slice()
console.log(iveMembers.slice(0, 3))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이' ]

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

slice는 splice의 원래 array가 변경되지 않는 버전이라 생각하면 편하다.

slice의 매개변수에는 어디부터 자를지에 대한 index와 몇 번 index까지 삭제할지를 넣어주면 된다.

## spread operator

```javascript
// spread operator
let iveMembers2 = [
    ...iveMembers,
];
console.log(iveMembers2)

let iveMembers3 = [
    iveMembers,
]
console.log(iveMembers3)

console.log('----------------')

let iveMembers4 = iveMembersaJAVA의 array를 할 줄 안다면 JavaScript의 Array Methods는 비슷하다.

## push()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// push()
console.log(iveMembers.push('코드팩토리'))
console.log(iveMembers)
```

출력 결과

7

[ '안유진', '가을', '레이', '장원영', '리즈', '이서', '코드팩토리' ]

첫 번째 코드는 **push**를 했을 때 array의 길이를 나타내는 코드이다.

## pop()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// pop()
console.log(iveMembers.pop())
console.log(iveMembers)
```

출력 결과

코드팩토리

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**pop**은 array에 있는 값을 빼는 것이다. **push**와 다르게 parameter에 아무것도 넣지 않아도 된다. 마지막 엘리멘트를 삭제하는 데 사용

## shift()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서',
];

// shift()
console.log(iveMembers.shift())
console.log(iveMembers)
```

출력 결과

안유진

[ '가을', '레이', '장원영', '리즈', '이서' ]

출력 결과를 보면 알 수 있듯이 **shift**는 **pop**과 비슷하지만 차이점은 맨 앞에 있는 값을 빼내는 것이다.

## unshift()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// unshift()
console.log(iveMembers.unshift('안유진'))
console.log(iveMembers)
```

출력 결과

6

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**unshift**도 출력 결과를 보면 알 수 있듯이 **push**와 굉장히 비슷하지만 차이점은 맨 앞에 값을 넣는다는 것이다.

## splice()

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// splice()
console.log(iveMembers.splice(0, 3))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이' ]

[ '장원영', '리즈', '이서' ]

이런 식으로 **splice**는 자르는 것이라고 보면 편하다. **splice**의 매개변수에는 두 개가 들어가는데 첫 번째 매개변수에는 index, 두 번째 매개변수에는 자를 개수를 적어주면 된다.

## concat()

```javascript
iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// concat()
console.log(iveMembers.concat('코드팩토리'))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이', '장원영', '리즈', '이서', '코드팩토리' ]

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

**concat**은 배열에 값을 넣는 것처럼 보여 **push**와 비슷하다고 생각할 수 있지만 **concat**은 새로운 array를 만들어서 반환을 해주는 것이다. 위 코드에서는 끝에 ‘코드팩토리’라는 글자가 붙은 array를 새로 만들어서 반환해준다.

아예 다른 메모리 공간에 저장된 값이 반환된다.

## slice()

```javascript
// slice()
console.log(iveMembers.slice(0, 3))
console.log(iveMembers)
```

출력 결과

[ '안유진', '가을', '레이' ]

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

slice는 splice의 원래 array가 변경되지 않는 버전이라 생각하면 편하다.

slice의 매개변수에는 어디부터 자를지에 대한 index와 몇 번 index까지 삭제할지를 넣어주면 된다.

## spread operator

```javascript
// spread operator
let iveMembers2 = [
    ...iveMembers,
];
console.log(iveMembers2)

let iveMembers3 = [
    iveMembers,
]
console.log(iveMembers3)

console.log('----------------')

let iveMembers4 = iveMembers

console.log(iveMembers4)
console.log(iveMembers4 === iveMembers)
```

출력 결과

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

[ [ '안유진', '가을', '레이', '장원영', '리즈', '이서' ] ]

- - - - - - - - - - - - - - - - - - - - - - - - -

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

true

위에 있는 코드 중 …이 spread operator인데 위 코드로 spread operator를 설명하자면 iveMembers의 값을 펼쳐서 iveMembers2에 넣겠다는 의미이다. spread operator를 사용하지 않은 값을 iveMembers3에 넣었는데 iveMembers3을 찍어보면 array 안에 또 array가 있는 것을 볼 수 있다.

## join()

```javascript
// join()
console.log(typeof iveMembers.join())
console.log(iveMembers.join())
console.log(iveMembers.join('/'))
console.log(iveMembers.join(', '))
```

출력 결과

string

안유진,가을,레이,장원영,리즈,이서

안유진/가을/레이/장원영/리즈/이서

안유진, 가을, 레이, 장원영, 리즈, 이서

join은 콤마를 기준으로 string으로 반환해준다.

join에도 arguement를 넣어줄 수 있는데 이 arguement에는 나눔의 기준이 되는 문자를 넣어줄 수 있다. 

## sort(), reverse()

```javascript
// sort()
iveMembers.sort()
console.log(iveMembers)

console.log(iveMembers.reverse())
```

출력 결과

[ '가을', '레이', '리즈', '안유진', '이서', '장원영' ]

[ '장원영', '이서', '안유진', '리즈', '레이', '가을' ]

sort를 실행을 하면 오름차순으로 정렬을 해준다. 또한 원래 array를 변경시키는 함수이다.

내림차순으로 정렬시키고 싶다면 reverse를 사용해주면 된다.

### sort()의 심화

```javascript
let numbers = [
    1,
    9,
    7,
    5,
    3,
];
console.log(numbers)

// a, b를 비교했을 때
// 1) a를 b보다 나중에 정렬하려면 (뒤에 두려면) 0보다 큰 숫자를 반환
// 2) a를 b보다 먼저 정렬하려면 (앞에 두려면) 0보다 작은 숫자를 반환
// 3) 원래 순서를 그대로 두려면 0을 반환
numbers.sort((a, b) => {
    return a > b ? 1 : -1
})
console.log(numbers)

numbers.sort((a, b) => a > b ? -1 : 1)
console.log(numbers)
```

출력 결과

[ 1, 9, 7, 5, 3 ]

[ 1, 3, 5, 7, 9 ]

[ 9, 7, 5, 3, 1 ]

출력 결과를 이해하려면 위 코드의 주석을 보면 된다.

## map()

```javascript
// map()
console.log(iveMembers.map((x) => x))
console.log(iveMembers.map((x) => `아이브: ${x}`))

console.log(iveMembers.map((x) => {
    if(x === '안유진') {
        return `아이브: ${x}`
    }
    else
        return x
}))
```

출력 결과

[ '장원영', '이서', '안유진', '리즈', '레이', '가을' ]

[ '아이브: 장원영', '아이브: 이서', '아이브: 안유진', '아이브: 리즈', '아이브: 레이', '아이브: 가을' ]

[ '장원영', '이서', '아이브: 안유진', '리즈', '레이', '가을' ]

array에 있는 모든 값들을 순회하면서 그 각각의 값들을 변형시키는 역할을 한다. 또한 **map**도 원래의 array를 변형시키는 것이 아닌 새로운 array를 반환을 해준다.

## filter()

```javascript
// filter()
numbers = [1, 8, 7, 6, 3]

console.log(numbers.filter((x) => true))
console.log(numbers.filter((x) => false))
console.log(numbers.filter((x) => x % 2 === 0))
```

출력 결과

[ 1, 8, 7, 6, 3 ]

[]

[ 8, 6 ]

**filter**는 원하는 값을 찾을 수 있는 함수라 생각하면 된다.

## find()

```javascript
// find()
console.log(numbers.find((x) => x % 2 === 0))
```

출력 결과

8

**find**도 **filter**와 같이 원하는 값을 찾을 수 있는 함수이지만 **filter**와의 차이는 **filter**는 true에 해당하는 값을 모두 찾지만 **find**같은 경우에는 순서대로 본 후 해당하는 첫 번째 값만 가져온다.

## findIndex()

```javascript
// find()
console.log(numbers.find((x) => x % 2 === 0))
```

출력 결과

1

**findIndex**는 find와 같지만 index를 반환한다.

## reduce()

```javascript
// reduce()
console.log(numbers.reduce((p, n) => p + n, 0))
```

![image.png](attachment:6a08e6ec-10e4-4a64-8d66-6227f223d0e8:image.png)

### reduce()함수가 작동하는 순서

![image.png](attachment:fd8d2b88-c437-456b-8000-82b02d8dd2d6:image.png)

1. 초기값인 0이 p에 입력된다.
2. numbers array에 첫 번째 값인 1이 n에 입력된다.
3. p + n 즉, 0 + 1의 결과값인 1이 반환된다.
4. 3에서 반환한 값(1)이 p에 입력된다.
5. array의 두 번째 값인 8이 n에 입력된다.
6. p + n 즉, 1 + 8의 결과값인 9가 반환된다.
7. 6에서 반환한 값(9)가 p에 입력된다.
8. numbers list의 모든 값들을 다 순회할 때까지 반복

결국 모든 값들을 다 더한 25가 반환된다.

전체 코드

```javascript
let iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

console.log(iveMembers)

// push()
console.log(iveMembers.push('코드팩토리'))
console.log(iveMembers)

console.log('----------------')

// pop()
console.log(iveMembers.pop())
console.log(iveMembers)

console.log('----------------')

// shift()
console.log(iveMembers.shift())
console.log(iveMembers)

console.log('----------------')

// unshift()
console.log(iveMembers.unshift('안유진'))
console.log(iveMembers)

console.log('----------------')

// splice()
console.log(iveMembers.splice(0, 3))
console.log(iveMembers)

console.log('----------------')

iveMembers = [
    '안유진',
    '가을',
    '레이',
    '장원영',
    '리즈',
    '이서', 
];

// concat()
console.log(iveMembers.concat('코드팩토리'))
console.log(iveMembers)

console.log('----------------')

// slice()
console.log(iveMembers.slice(0, 3))
console.log(iveMembers)

console.log('----------------')

// spread operator
let iveMembers2 = [
    ...iveMembers,
];
console.log(iveMembers2)

let iveMembers3 = [
    iveMembers,
]
console.log(iveMembers3)

console.log('----------------')

let iveMembers4 = iveMembers

console.log(iveMembers4)
console.log(iveMembers4 === iveMembers)

console.log('----------------')

// join()
console.log(typeof iveMembers.join())
console.log(iveMembers.join())
console.log(iveMembers.join('/'))
console.log(iveMembers.join(', '))

console.log('----------------')

// sort()
iveMembers.sort()
console.log(iveMembers)

console.log(iveMembers.reverse())

let numbers = [
    1,
    9,
    7,
    5,
    3,
];
console.log(numbers)

// a, b를 비교했을 때
// 1) a를 b보다 나중에 정렬하려면 (뒤에 두려면) 0보다 큰 숫자를 반환
// 2) a를 b보다 먼저 정렬하려면 (앞에 두려면) 0보다 작은 숫자를 반환
// 3) 원래 순서를 그대로 두려면 0을 반환
numbers.sort((a, b) => {
    return a > b ? 1 : -1
})
console.log(numbers)

numbers.sort((a, b) => a > b ? -1 : 1)
console.log(numbers)

console.log('----------------')

// map()
console.log(iveMembers.map((x) => x))
console.log(iveMembers.map((x) => `아이브: ${x}`))

console.log(iveMembers.map((x) => {
    if(x === '안유진') {
        return `아이브: ${x}`
    }
    else
        return x
}))

console.log('----------------')

// filter()
numbers = [1, 8, 7, 6, 3]

console.log(numbers.filter((x) => true))
console.log(numbers.filter((x) => false))
console.log(numbers.filter((x) => x % 2 === 0))

console.log('----------------')

// find()
console.log(numbers.find((x) => x % 2 === 0))

console.log('----------------')

// findIndex()
console.log(numbers.findIndex((x) => x % 2 === 0))

console.log('----------------')

// reduce()
console.log(numbers.reduce((p, n) => p + n, 0))
```

console.log(iveMembers4)
console.log(iveMembers4 === iveMembers)
```

출력 결과

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

[ [ '안유진', '가을', '레이', '장원영', '리즈', '이서' ] ]

- - - - - - - - - - - - - - - - - - - - - - - - -

[ '안유진', '가을', '레이', '장원영', '리즈', '이서' ]

true

위에 있는 코드 중 …이 spread operator인데 위 코드로 spread operator를 설명하자면 iveMembers의 값을 펼쳐서 iveMembers2에 넣겠다는 의미이다. spread operator를 사용하지 않은 값을 iveMembers3에 넣었는데 iveMembers3을 찍어보면 array 안에 또 array가 있는 것을 볼 수 있다.

## join()

```javascript
// join()
console.log(typeof iveMembers.join())
console.log(iveMembers.join())
console.log(iveMembers.join('/'))
console.log(iveMembers.join(', '))
```

출력 결과

string

안유진,가을,레이,장원영,리즈,이서

안유진/가을/레이/장원영/리즈/이서

안유진, 가을, 레이, 장원영, 리즈, 이서

join은 콤마를 기준으로 string으로 반환해준다.

join에도 arguement를 넣어줄 수 있는데 이 arguement에는 나눔의 기준이 되는 문자를 넣어줄 수 있다. 

## sort(), reverse()

```javascript
// sort()
iveMembers.sort()
console.log(iveMembers)

console.log(iveMembers.reverse())
```

출력 결과

[ '가을', '레이', '리즈', '안유진', '이서', '장원영' ]

[ '장원영', '이서', '안유진', '리즈', '레이', '가을' ]

sort를 실행을 하면 오름차순으로 정렬을 해준다. 또한 원래 array를 변경시키는 함수이다.

내림차순으로 정렬시키고 싶다면 reverse를 사용해주면 된다.

### sort()의 심화

```javascript
let numbers = [
    1,
    9,
    7,
    5,
    3,
];
console.log(numbers)

// a, b를 비교했을 때
// 1) a를 b보다 나중에 정렬하려면 (뒤에 두려면) 0보다 큰 숫자를 반환
// 2) a를 b보다 먼저 정렬하려면 (앞에 두려면) 0보다 작은 숫자를 반환
// 3) 원래 순서를 그대로 두려면 0을 반환
numbers.sort((a, b) => {
    return a > b ? 1 : -1
})
console.log(numbers)

numbers.sort((a, b) => a > b ? -1 : 1)
console.log(numbers)
```

출력 결과

[ 1, 9, 7, 5, 3 ]

[ 1, 3, 5, 7, 9 ]

[ 9, 7, 5, 3, 1 ]

출력 결과를 이해하려면 위 코드의 주석을 보면 된다.

## map()

```javascript
// map()
console.log(iveMembers.map((x) => x))
console.log(iveMembers.map((x) => `아이브: ${x}`))

console.log(iveMembers.map((x) => {
    if(x === '안유진') {
        return `아이브: ${x}`
    }
    else
        return x
}))
```

출력 결과

[ '장원영', '이서', '안유진', '리즈', '레이', '가을' ]

[ '아이브: 장원영', '아이브: 이서', '아이브: 안유진', '아이브: 리즈', '아이브: 레이', '아이브: 가을' ]

[ '장원영', '이서', '아이브: 안유진', '리즈', '레이', '가을' ]

array에 있는 모든 값들을 순회하면서 그 각각의 값들을 변형시키는 역할을 한다. 또한 **map**도 원래의 array를 변형시키는 것이 아닌 새로운 array를 반환을 해준다.

## filter()

```javascript
// filter()
numbers = [1, 8, 7, 6, 3]

console.log(numbers.filter((x) => true))
console.log(numbers.filter((x) => false))
console.log(numbers.filter((x) => x % 2 === 0))
```

출력 결과

[ 1, 8, 7, 6, 3 ]

[]

[ 8, 6 ]

**filter**는 원하는 값을 찾을 수 있는 함수라 생각하면 된다.

## find()

```javascript
// find()
console.log(numbers.find((x) => x % 2 === 0))
```

출력 결과

8

**find**도 **filter**와 같이 원하는 값을 찾을 수 있는 함수이지만 **filter**와의 차이는 **filter**는 true에 해당하는 값을 모두 찾지만 **find**같은 경우에는 순서대로 본 후 해당하는 첫 번째 값만 가져온다.

## findIndex()

```javascript
// find()
console.log(numbers.find((x) => x % 2 === 0))
```

출력 결과

1

**findIndex**는 find와 같지만 index를 반환한다.

## reduce()

```javascript
// reduce()
console.log(numbers.reduce((p, n) => p + n, 0))
```

![image.png](attachment:6a08e6ec-10e4-4a64-8d66-6227f223d0e8:image.png)

### reduce()함수가 작동하는 순서

![image.png](attachment:fd8d2b88-c437-456b-8000-82b02d8dd2d6:image.png)

1. 초기값인 0이 p에 입력된다.
2. numbers array에 첫 번째 값인 1이 n에 입력된다.
3. p + n 즉, 0 + 1의 결과값인 1이 반환된다.
4. 3에서 반환한 값(1)이 p에 입력된다.
5. array의 두 번째 값인 8이 n에 입력된다.
6. p + n 즉, 1 + 8의 결과값인 9가 반환된다.
7. 6에서 반환한 값(9)가 p에 입력된다.
8. numbers list의 모든 값들을 다 순회할 때까지 반복

결국 모든 값들을 다 더한 25가 반환된다.