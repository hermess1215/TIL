## Object란

```javascript
// key : value pair
let yuJin = {
    name: '안유진',
    group: '아이브',
    dance: function() {
        return '안유진이 춤을 춥니다.'
    }
}
console.log(yuJin)
console.log(yuJin.name)
console.log(yuJin['name'])

const key = 'name'
console.log(yuJin[key])
```

출력 결과

{ name: '안유진', group: '아이브', dance: [Function: dance] }

안유진

안유진

안유진

Object는 기본적으로 key, value 한 쌍으로 만든다.

추가적으로 함수를 추가해서 사용할 수 있는데 이것을 메소드라고 부른다.

### this 키워드

```javascript
let yuJin = {
    name: '안유진',
    group: '아이브',
    dance: function() {
        return `${this.name}이 춤을 춥니다.`
    }
}
console.log(yuJin.dance())
```

출력 결과

안유진이 춤을 춥니다.

**this** 키워드는 해당 함수가 정의되어있는 객체, 즉 Object를 가리킨다.

### 객체 선언 시 변수 사용 방법

```javascript
const nameKey = 'name'
const nameValue = '안유진'

const groupKey = 'group'
const groupValue = '아이브'

const yuJin2 = {
    [nameKey] : nameValue,
    [groupKey] : groupValue,
    dance : function() {
        return `${this.name}이 춤을 춥니다.`
    }
}
console.log(yuJin2)
console.log(yuJin2.dance())

yuJin2['group'] = '코드팩토리'
console.log(yuJin2)

yuJin2['englishName'] = 'An Yu Jin'
console.log(yuJin2)
```

출력 결과

{ name: '안유진', group: '아이브' }

안유진이 춤을 춥니다.

{ name: '안유진', group: '코드팩토리', dance: [Function: dance] }

{

  name: '안유진',

  group: '코드팩토리',

  dance: [Function: dance],

  englishName: 'An Yu Jin’

}

Object의 키에다가 변수를 집어넣을 때는 대괄호를 이용해주면 된다. 또한 존재하지 않았던 키를 넣으면 새로 생성이 된다.

```javascript
delete yuJin2['englishName']
console.log(yuJin2)
```

출력 결과

{ name: '안유진', group: '코드팩토리', dance: [Function: dance] }

키를 삭제하고 싶다면 위처럼 delete를 사용하면 된다.

### 모든 키 값 및 밸류 값 가져오기

```javascript
// 모든 키 값 가져오기
console.log(Object.keys(wonYoung))

// 모든 밸류 값 가져오기
console.log(Object.values(wonYoung))
```

## const로 선언한 Object의 특징

1. const로 선언할 경우 객체 자체를 변경할 수는 없다.
2. 객체 안에 property나 method는 변경할 수 있다.

```javascript
const wonYoung = {
    name : '장원영',
    group : '아이브',
}
console.log(wonYoung)

// wonYoung = {} <- 에러

wonYoung['group'] = '코드팩토리'
console.log(wonYoung)
```

```javascript
const name = '안유진'

const yuJin3 = {
    name,
}
console.log(yuJin3)
```

출력 결과

{ name: '안유진' }

위 코드처럼 key 이름도 name이고, 밸류 값에 들어갈 것도 name 변수이면 하나만 써도 된다.

전체 코드

```javascript
// key : value pair
let yuJin = {
    name: '안유진',
    group: '아이브',
    dance: function() {
        return `${this.name}이 춤을 춥니다.`
    }
}
console.log(yuJin)
console.log(yuJin.name)
console.log(yuJin['name'])

const key = 'name'
console.log(yuJin[key])

console.log(yuJin.dance())

console.log('----------------')

const nameKey = 'name'
const nameValue = '안유진'

const groupKey = 'group'
const groupValue = '아이브'

const yuJin2 = {
    [nameKey] : nameValue,
    [groupKey] : groupValue,
    dance : function() {
        return `${this.name}이 춤을 춥니다.`
    }
}
console.log(yuJin2)
console.log(yuJin2.dance())

yuJin2['group'] = '코드팩토리'
console.log(yuJin2)

yuJin2['englishName'] = 'An Yu Jin'
console.log(yuJin2)

delete yuJin2['englishName']
console.log(yuJin2)

console.log('----------------')

const wonYoung = {
    name : '장원영',
    group : '아이브',
}
console.log(wonYoung)

// wonYoung = {} // 에러

wonYoung['group'] = '코드팩토리'
console.log(wonYoung)

console.log('----------------')

// 모든 키 값 가져오기
console.log(Object.keys(wonYoung))

// 모든 밸류 값 가져오기
console.log(Object.values(wonYoung))

console.log('----------------')

const name = '안유진'

const yuJin3 = {
    name,
}
console.log(yuJin3)
```