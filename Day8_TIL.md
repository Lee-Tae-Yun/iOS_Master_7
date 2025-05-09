# 📘 Day 8 - Today I Learned

**🔑 핵심 키워드:**  
`Tuple`, `Array`, `Dictionary`, `Set`, `Closure`, `Optional`, `Optional Binding`, `if let`, `guard let`, `Optional Forced Unwrapping`, `Nil-Coalescing Operator`

---

## 📝 튜플 (`Tuple`)
> 튜플은 **여러 개의 데이터를 하나의 변수**로 관리할 수 있는 자료형 입니다.

**예시**
- 사용자의 이름과 나이를 함께 저장해야 할 때
- 좌표 (x, y) 값을 하나의 변수로 저장해야 할 때

**선언 방법**
```swift
let person = (name: "이태윤", age: 26)
```

**접근 방법**
```swift
print(person.name) // 이태윤
print(person.age)  // 26
```

👉 이름 없이 인덱스로도 접근할 수 있습니다.

---

## 📝 배열 (`Array`)

> 배열은 **같은 데이터 타입**의 여러 값을 **순차적으로 저장**하는 자료형입니다.  
배열의 요소들은 인덱스를 통해 접근할 수 있으며, 크기는 **동적으로 변경** 가능합니다.

**예시**
- 쇼핑몰에서 여러 상품의 가격을 관리할 때
- 학생들의 시험 성적을 한 번에 처리할 때
- 하루 동안 날씨 데이터를 기록할 때



**선언 방법**
```swift
var numbers: [Int] = [1, 2, 3, 4, 5]
```

**접근 방법**
```swift
print(numbers[0]) // 1
```

---

## 📝 딕셔너리 (`Dictionary`)

> 딕셔너리는 **키(Key)와 값(Value)의 쌍으로 데이터를 저장**할 수 있습니다.  
각 키가 고유해야 하며, 하나의 키에 하나의 값이 대응됩니다.  
**값은 중복될 수 있지만 키는 중복될 수 없습니다.** 데이터를 빠르게 찾고 관리할 때 유용합니다.

**예시**
- 학생들의 학번과 이름을 매칭하는 경우
- 쇼핑몰에서 상품의 ID와 이름을 매칭하는 경우
- 서버에서 사용자 정보를 키로 구분해 데이터를 조회하는 경우


**선언 방법**
```swift
var student: [Int: String] = [101: "태윤", 102: "이든", 103: "우성"]
```

**접근 방법**
```swift
print(student[101]) // 태윤
```

---

## 📝 셋 (`Set`)

> 셋은 **중복을 허용하지 않고 순서가 없는** 데이터 집합을 저장할 때 사용합니다. 
인덱스를 사용해 값을 접근할 수 없으며, 데이터를 효율적으로 관리하고, 중복 제거가 필요한 경우에 유용합니다.

**예시**
- 학생들의 고유한 ID를 저장하는 경우
- 쇼핑몰에서 사용자가 좋아요를 누른 상품 목록을 저장하는 경우

**선언 방법**
```swift
var uniqueNumbers: Set<Int> = [1, 2, 3]
```

**접근 방법**
```swift
print(uniqueNumbers) // [1, 2, 3] (순서 보장 안됨)
```

---

## 📝 클로저 함수 (`Closure`)

> **이름이 없는 함수(익명 함수)를 의미합니다.**

**기본 문법**
```swift
{ (매개변수) -> 반환타입 in
    실행할 코드
}
```

**예시**
```swift
let multiply = { (a: Int, b: Int) -> Int in
    return a * b
}

let result = multiply(3, 4)
print(result) // 12
```

---

## 📝 옵셔널 (`Optional`)

> 옵셔널(`Optional`)이란 값이 있을 수도 없을 수도 있는 타입을 의미합니다.  
값이 없을 경우 `nil`이 저장됩니다.
**예시**
- 사용자 입력값이 없을 가능성이 있는 경우
- 배열에서 특정 인덱스의 값이 없을 가능성이 있는 경우
- 서버에서 데이터를 받아올 때 값이 없을 가능성이 있는 경우

**선언 방법**
```swift
var name: String? = "TaeYun"
```

**사용 방법**
```swift
print(name) // Optional("TaeYun")
```

---

## 📝 옵셔널 바인딩

> 옵셔널 타입에 값이 있는지 확인하고, 값이 있다면 안전하게 사용합니다.

### if let
```swift
if let unwrapped = optionalValue {
    print(unwrapped) // unwrapped 값 (if 블록 안에서만 사용 가능)
} else {
    print("값이 없습니다.")
}
```

### guard let
```swift
func doSomething(optionalValue: String?) {
    guard let unwrapped = optionalValue else {
        print("값이 없습니다.")
        return
    }
    print(unwrapped) // unwrapped 값 (함수 전체에서 사용 가능)
}
```

👉 `if let`: 조건 만족 시 **블록 안**에서만 사용 가능  
👉 `guard let`: 조건 불만족 시 함수 종료, 만족 시 **함수 전체에서 사용 가능**

**옵셔널 강제 해제**
```swift
var name: String? = "Bob"
print(name!) // Bob (nil일 경우 런타임 오류 발생)
```

**병합 연산자 (Nil-Coalescing Operator)**
```swift
let userName: String? = nil
let displayName = userName ?? "Guest"
print(displayName) // Guest
```

---

## 📚 옵셔널은 왜 존재할까? 오늘 깨달은 이유
오늘 **옵셔널**에 대해 공부하면서 처음에는 어려움을 느꼈다.  
다른 언어들은 그냥 `null` 값을 `if`문이나 `try-catch`문으로 처리하면 되는데,  
**왜 Swift는 굳이 옵셔널을 사용해야 하는 걸까?** 라는 의문이 들었다.

## 왜 if문만으로는 안 될까?

또한, 어차피 옵셔널 바인딩을 할 때도 `if let`, `guard let`을 사용해서  
값이 있는지 확인해야 한다면,  
**그냥 다른 언어처럼 `if (a == nil)` 방식으로 하면 안 되는 걸까?**  
라는 궁금증이 생겼다.

## 공부 후 깨달음

더 공부해보니, 옵셔널은 단순히 `nil` 체크용이 아니라  
> **값이 없을 수 있음을 타입에 명시적으로 포함시키고,  
컴파일 단계에서 강제 체크하여 런타임 에러를 예방하고,  
개발자의 실수를 방지하며,  
앱을 더 안전하고 예측 가능한 범위 안에서 동작하도록 한다**

는 이유로 설계되었다는 걸 깨달았다.

Swift가 다른 언어와 다르게 **안전성**을 중요하게 생각하기 때문에  
이렇게 타입 시스템에서부터 `nil` 처리를 강제하는구나… 라는 걸 알게 됐다.
