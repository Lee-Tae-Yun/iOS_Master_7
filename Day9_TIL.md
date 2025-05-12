# 📘 Day 9 - Today I Learned

오늘은 Swift에서의 **클래스(Class)** 와 **구조체(Struct)** 에 대해 학습하였습니다.

---

## 🏷️ 클래스 (`Class`)

> 클래스를 사용하면 **현실 세계의 개념을 코드로 표현**할 수 있으며,  
> **속성(프로퍼티)** 과 **기능(메서드)** 을 정의하는 사용자 정의 참조 타입입니다.

### 🔍 클래스가 필요한 이유
- 사용자 정보 관리  
  → 이름, 나이, 이메일 등을 묶어서 다룰 수 있음
- 게임 캐릭터 설계  
  → 체력, 공격력, 방어력 등 속성과 기능 포함 가능
- 데이터베이스 연결 관리  
  → 연결을 재사용하거나 관리하는 객체로 표현

### 📚 클래스 기본 문법
```swift
class 클래스이름 {
    var 속성이름: 타입

    init(초기화할값) {
        self.속성이름 = 초기화할값
    }

    func 메서드이름() {
        // 실행할 코드
    }
}
```

### ✅ 예시
```swift
class Person {
    var name: String 
    var age: Int 

    init(name: String, age: Int) { 
        self.name = name
        self.age = age 
    } 

    func introduce() {
        print("안녕하세요, 저는 \\(name)이고 \\(age)살이에요.") 
    }
}

let person1 = Person(name: "태윤", age: 26)
person1.introduce() // 안녕하세요, 저는 태윤이고 26살이에요.
```

### 💡 클래스의 특성: 참조 타입
- 클래스는 **참조 타입(reference type)** 입니다.
- 객체를 변수에 할당하거나 함수에 전달하면 **값이 복사되지 않고 참조가 전달**됩니다.

---

## 🏷️ 구조체 (`Struct`)

> 구조체는 **간단한 데이터 집합**을 표현할 때 적합하며,  
> **값이 복사되어 독립적으로 사용**되는 **값 타입(value type)**입니다.

### 🔍 구조체가 필요한 이유
- 좌표 데이터 관리  
  → 2D 좌표 `(x, y)` 등을 저장할 때
- 네트워크 응답 데이터 저장  
  → API 응답 값을 임시로 저장할 때
- 설정값 저장  
  → 사용자 설정값을 안전하게 보존할 때

### 📚 구조체 기본 문법
```swift
struct 구조체이름 {
    var 속성: 타입

    func 메서드이름() {
        // 실행할 코드
    }
}
```

### ✅ 예시
```swift
struct Rectangle {
    var width: Double
    var height: Double

    func area() -> Double {
        return width * height
    }
}

let rect = Rectangle(width: 5.0, height: 10.0)
print("면적은 \\(rect.area())입니다.") // 면적은 50.0입니다.
```

### 💡 구조체의 특성: 값 타입
- 구조체는 **값 타입(value type)** 입니다.
- 변수에 할당되거나 함수에 전달될 때 **값이 복사**되어 독립적으로 동작합니다.

🧩 구조체는 **멤버와이즈 이니셜라이저**를 자동으로 제공합니다.

---

📚 오늘은 클래스와 구조체의 문법과 차이를 이해하고,  
각각의 특성과 사용하는 이유에 대해 학습하였습니다.
