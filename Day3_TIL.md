# 📘 Day 3 Today I Learned - 문법학습 시작!


###  기본 데이터 타입의 이해

- **변수(Variable)** : `var` 키워드를 사용하며 값을 변경할 수 있습니다.  
- **상수(Constant)** : `let` 키워드를 사용하여 선언하며, 한번 값이 설정되면 변경할 수 없습니다.

### 주요 데이터 타입
- `Int` : 정수형 숫자  
- `Double` : 소수점을 포함한 숫자  
- `Float` : 소수점을 포함한 숫자(더 적은 정밀도)  
- `String` : 텍스트 데이터를 저장하는 타입  
- `Bool` : 참(`true`) 또는 거짓(`false`) 값을 저장


### 데이터 타입 변환하기 (Type Casting)

- 정수를 실수로 변환 : `Double(정수)`  
- 실수를 정수로 변환 : `Int(실수)`  
- 숫자를 문자열로 변환 : `String(숫자)`

---

### 연산자의 이해

### 산술 연산자
```swift
+  // 덧셈        let sum = 10 + 5  
-  // 뺄셈        let diff = 10 - 5  
*  // 곱셈        let product = 10 * 5  
/  // 나눗셈      let quotient = 10 / 5  
%  // 나머지 연산  let remainder = 10 % 3
```

### 비교 연산자
```swift
==  // 값이 같은지 비교 a == b  
!=  // 값이 다른지 비교 a != b  
>   // 왼쪽 값이 더 큰지 비교 a > b  
<   // 오른쪽 값이 더 큰지 비교 a < b  
>=  // 왼쪽 값이 크거나 같은지 비교 a >= b  
<=  // 오른쪽 값이 크거나 같은지 비교 a <= b
```

### 논리 연산자
```swift
&&  // AND: 둘 다 참이어야 참          true && false -> false  
||  //OR (둘 중 하나가 참이어야 참)      true || false -> true
!   // NOT: 참을 거짓으로, 거짓을 참으로  !true -> false
```

### 할당 연산자
```swift
=   // 값 할당       var x = 10  
+=  // 더한 후 할당   x += 5   // x = x + 5  
-=  // 뺀 후 할당     x -= 5   // x = x - 5  
*=  // 곱한 후 할당   x *= 5   // x = x * 5  
/=  // 나눈 후 할당   x /= 5   // x = x / 5
```

---

### 조건문 이해하기

### if - else 문

특정 조건이 `true`면 실행되고, `false`이면 다른 코드가 실행됩니다.

```swift
let temperature = 30

if temperature > 25 {
    print("더운 날씨입니다.")
} else {
    print("시원한 날씨입니다.")
}
```

- `if - else` 문은 조건이 하나이고 그 조건이 참인지 거짓인지에 따라 두 가지 경우로 나뉘는 상황에 적합합니다.
- 예: 사용자가 로그인 상태인지에 따라 메시지를 출력할 때


### else if 문

여러 개의 조건을 순차적으로 검사할 때 사용됩니다.

```swift
let score = 85

if score >= 90 {
    print("A 등급입니다!")
} else if score >= 80 {
    print("B 등급입니다!")
} else {
    print("더 노력하세요!")
}
```

- `else if` 문은 조건이 여러 개인 경우 우선순위에 따라 차례로 검사하는 상황에 적합합니다.
- 예: 시험 점수에 따라 등급을 나누는 경우


### switch 문

- 여러 경우의 고정된 값을 비교할 때 사용합니다.
- `if - else if`보다 코드가 깔끔하고 가독성이 높습니다.
- Swift의 `switch` 문은 범위값도 지원합니다.

```swift
switch day {
case "월요일":
    print("한 주의 시작입니다!")
case "금요일":
    print("주말이 다가오고 있어요!")
case "토요일", "일요일":
    print("주말입니다! 푹 쉬세요!")
default:
    print("일상적인 하루입니다.")
}
```

- `switch` 문은 `day`의 값에 따라 적절한 메시지를 출력합니다.
- `default`는 모든 경우에 해당하지 않을 때 실행됩니다.
- 예: 특정 요일에 따라 다른 동작을 수행하는 상황에서 유용합니다.

---

### 과제

## Swift Playgrounds로 실습 완료하기

```swift
var myName = "이태윤"
print("안녕하세요, \(myName)님! Swift Playground에 오신 것을 환영합니다!")
```

## 변수와 상수 선언하기

```swift
var name = "Tae Yun"
var age = 26
let birthYear = 2000

print("이름 : \(name) \n 나이 : \(age) \n 출생연도 : \(birthYear)")
```

## 데이터 타입 

```swift
var height: Double = 185.1
var isStuent: Bool = true
var hobby: String = "운동"

print("키 : \(height) \n 학생인가요? : \(isStuent) \n 취미 : \(hobby)")
```

## 데이터 타입 변환하기 (Type Casting)

```swift
let score: Double = 95.7
let intScore = Int(score)
let age1 = 25
let ageMessage: String = "나는 \(String(age1)) 살 입니다."

print("정수형 점수 : \(intScore)")
print(ageMessage)
```

## 간단한 대화형 프로그램 만들기

```swift
var userName: String = "이태윤"
var userAge: Int = 26

print("안녕하세요, \(userName)님!")
print("당신의 나이는 \(String(userAge))살입니다.")
```

## 산술 연산자

```swift
let num3 = 20
let num4 = 5

let sum1 = num3 + num4
let difference = num3 - num4
let product = num3 * num4
let quotient = num3 / num4
let remainder = num3 % num4

print("덧셈: \(sum1), 뺄셈: \(difference)")
print("곱셈: \(product), 나눗셈: \(quotient), 나머지: \(remainder)")
```

## 비교 연산자

```swift
let height1 = 170
let height2 = 170

print("키 비교: \(height1 > height2)")
print("같은 키인가요? \(height1 == height2)")
```

## 논리 연산자

```swift
let isSunny = false
let isWeekend = true

let goOutside = isSunny && isWeekend
let stayHome = !isSunny

print("외출할까요? \(goOutside)")
print("집에 있을까요? \(stayHome)")
```
## 할당 연산자


```swift
var points = 60

points += 10
print("현재 점수: \(points)")

points *= 2
print("현재 점수: \(points)")
```

## 간단한 성적 평가 프로그램 만들기

```swift
let score1 = 85
let result: String
if score1 >= 90 {
    result = ("A 등급입니다!")
} else if score1 >= 80 {
    result = ("B 등급입니다!")
} else if score1 >= 70 {
    result = ("C 등급입니다!")
} else {
    result = ("더 노력하세요!")
}
print(result)
```

## 나이에 따른 영화 관람 가능여부

```swift
var age5: Int = 20

if age5 >= 19 {
    print("청소년 관람 불가 영화를 볼 수 있습니다.")
}
else if age5 >= 13 {
    print("일반 영화는 볼 수 있지만 청소년 관람 불가 영화는 볼 수 없습니다. ")
}
else {
    print("보호자 동반이 필요합니다.")
}
```

## 시험 점수에 따른 학점 부여

```swift
var grade: Int = 85
var reslut: String

if grade >= 90 {
    reslut = "A 학점"
}
else if grade >= 80 {
    reslut = "B 학점"
}
else if grade >= 70 {
    reslut = "C 학점"
}
else if grade >= 60 {
    reslut = "D 학점"
}
else {
    reslut = "F 학점"
}

print("점수 : \(grade) \n\(reslut)")
```



