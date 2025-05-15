# 📘 Day 4 Today I Learned - 문법 학습 시작!


## 📌 반복문 이해하기

### 🔁 `for-in` 문
- 정해진 횟수만큼 반복할 때 사용
- 배열(`Array`) 또는 범위(`Range`)의 요소를 순회 합니다.
- 단 반복 횟수가 미리 정해져 있어야 합니다.
- 범위를 사용하여 특정 범위의 숫자를 반복할 수 있습니다.

```swift
for i in 1...5 {
    print("반복 \(i)회")
}
```

```swift
let names = ["Alice", "Bob", "Charlie"]
for name in names {
    print("이름: \(name)")
}
```

---

### 🔄 `while` 문
- 반복 횟수가 정해져 있지 않고, **조건이 참(`ture`)인 동안 반복**
- **조건을 먼저 검사**하고, 거짓(`false`)이면 실행 안 함

```swift
var number = 1

while number <= 10 {
    print("현재 숫자: \\(number)")
    number += 1
}
```

```swift
var input = -1

while input != 0 {
    print("숫자를 입력하세요 (0을 입력하면 종료): ")
    if let userInput = readLine(), let num = Int(userInput) {
        input = num
    }
}
print("프로그램 종료")
```

---

### 🔁 `repeat-while` 문
- **최소 한 번은 무조건 실행**
- 실행 후 조건을 검사

```swift
var count = 0

repeat {
    print("반드시 한 번 실행됩니다! (현재 count: \\(count))")
    count += 1
} while count < 3
```

```swift
var password = ""

repeat {
    print("비밀번호 입력: ")
    password = readLine() ?? ""
} while password != "1234"

print("비밀번호가 맞습니다!")
```

---

### 🔎 반복문 비교 요약

| 문법 | 사용 시점 | 특징 |
|------|-----------|------|
| `for-in` | 반복 횟수가 명확할 때 | 범위나 배열 순회에 적합 |
| `while` | 반복 조건이 중요할 때 | 먼저 조건 검사 후 실행 |
| `repeat-while` | 최소 한 번 실행이 필요할 때 | 실행 후 조건 검사 |


### 반복문 선택 가이드

- **반복 횟수가 정해져 있다면?** → `for-in` 문 사용  
- **조건을 먼저 확인한 후 실행해야 한다면?** → `while` 문 사용  
- **반드시 한 번은 실행해야 한다면?** → `repeat-while` 문 사용

---

## 🧠 함수(Function)란?

함수는 **코드 재사용성 증가**, **가독성 향상**을 위한 중요한 문법입니다.

### ✅ 기본 구조

```swift
func 함수이름(매개변수이름: 타입) -> 반환타입 {
    // 실행할 코드
    return 결과값
}
```

---

### 🙋 매개변수가 없는 함수

```swift
func sayHello() {
    print("안녕하세요!")
}

sayHello() // "안녕하세요!" 출력
```

---

### 🙋‍♂️ 매개변수가 있는 함수

```swift
func greet(name: String) {
    print("안녕하세요, \\(name)님!")
}

greet(name: "Alice") // "안녕하세요, Alice님!" 출력
greet(name: "Bob")   // "안녕하세요, Bob님!" 출력
```

---

### 🔁 반환값이 있는 함수

```swift
func add(a: Int, b: Int) -> Int {
    return a + b
}

let sum = add(a: 5, b: 3) // 8 반환
print(sum) // 8 출력
```

---

### 💡 꿀팁: 매개변수명 생략하기

```swift
func multiply(_ a: Int, _ b: Int) -> Int {
    return a * b
}

let result = multiply(2, 3) // 매개변수 이름 생략
```

---

# 과제

### 1부터 N 까지의 합 구하기(`for`문 사용)

```swift
var sum: Int = 0
print("정수 값 하나를 입력하세요 : ")
if let intput: String = readLine(), let n = Int(intput) {
    for i in 1...n {
      sum += i
    }
  print("1부터 \(n)까지의 합은 : \(sum) 입니다.")
}
else {
    print("잘못된 값입니다.")
}
```

### 짝수만 출력하기 (`for`문 & `if`문 사용)

```swift
for i in 1...20{
    if i%2==0{
        print(i)
    }
}
```

### 특정 숫자가 나올 때까지 반복(`while`문 사용)

```swift
var randomInt: Int = 0

while randomInt != 5 {
    randomInt = Int.random(in: 1...20)
    print(randomInt)
}

print("\(randomInt) 가 나왔습니다!")
```

### 비밀번호 맞출 때 까지 반복(`repeat-while`문 사용)


```swift
var input: String = ""

repeat {
    print("비밀번호를 입력하세요 : ",terminator: "")
    input = readLine() ?? ""
    if(input != "1234"){
        print("비밀번호가 틀렸습니다.")
    }
    else {
        break
    }
} while input != "1234"

print("올바른 비밀번호입니다!")
```

### 숫자 맞추기 게임 만들기

```swift
let comNum: Int = Int.random(in: 1...100)
var input: String = ""
var num: Int = 0
print("숫자를 맞춰보세요!")
while num != comNum {
    print("숫자를 입력하세요 : " , terminator: "")
    input = readLine()!
    num = Int(input)!
    if(num > comNum ){
        print("더 작은 숫자를 입력하세요!")
    }
    else if num < comNum {
        print("더 큰 숫자를 입력하세요!")
    }
    else if num == comNum {
        print("축하합니다!! 정답입니다!")
        break
    }
}
```

### 기본적인 함수 선언

```swift
func sayHello(){
    print("Hello Swift!!")
}
```

### 매개변수를 받는 함수 만들기

```swift
func greet(name: String){
    print("안녕하세요 [\(name)]님!")
}

var input: String = readLine() ?? ""
greet(name: input)
```
