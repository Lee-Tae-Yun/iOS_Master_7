# 📘 Day 11 - Today I Learned

**🔑 핵심 키워드:**  
`데이터 모델`, `Entity`, `Attribute`, `Relationship`, `Struct`, `Class`, `MVC 패턴`, `Model`, `View`, `Controller`

---

## 📌 데이터 모델의 개념과 중요성

- **데이터 모델**: 데이터를 표현하는 **논리적 구조**로, 데이터 간의 관계를 정의함.
- **구성 요소**:
  - **Entity (엔티티)**: 데이터의 주요 단위, 객체 또는 개념을 나타냄
  - **Attribute (속성)**: 엔티티가 가지는 정보
  - **Relationship (관계)**: 엔티티 간의 연관성

### ✅ 데이터 모델의 중요성
- **데이터의 일관성 유지**: 구조화된 데이터를 통해 **중복 최소화** 및 정합성 확보
- **효율적인 데이터 관리**: 설계가 잘 된 모델은 **저장 및 검색 효율**이 높음

---

## 🧱 구조체(Struct)와 클래스(Class)를 활용한 데이터 모델

### ✅ 구조체는 값 타입 (Value Type)
- **복사하여 전달되며**, 변하지 않는 데이터에 적합
- 간단한 데이터 모델에 주로 사용

### ✅ 구조체 기본 문법

```swift
struct User {
    let id: Int
    var name: String
    var email: String
}
```

### ✅ 구조체 사용 예

```swift
var user1 = User(id: 1, name: "TaeYun", email: "abc001@naver.com")
print(user1.name) // TaeYun

user1.name = "LeeTaeYun"
print(user1.name) // LeeTaeYun
```

### ✅ 메서드 정의 및 사용

```swift
mutating func updateEmail(newEmail: String) {
    self.email = newEmail
}
```

- `mutating` 키워드를 통해 구조체 내부 프로퍼티 변경 가능

---

## 🧩 MVC 패턴과 데이터 모델의 역할

### ✅ Model (모델)
- **데이터 및 비즈니스 로직 처리**
- 역할:
  - 데이터 저장 (예: 사용자 정보, 상품 정보)
  - 데이터 가공, 비즈니스 로직 수행
  - 데이터 변경 감지 및 알림
  - API/DB 통신 등 외부 데이터 관리
- 구현 도구: `Struct`, `Class`, `Database`, `API` 등

### ✅ View (뷰)
- **UI 표시** 역할
- 사용자가 보는 화면 (예: `UILabel`, `UIButton`, `UITableView`)
- **데이터를 직접 다루지 않음**
- Controller를 통해 데이터 전달받음

### ✅ Controller (컨트롤러)
- **Model ↔ View 연결 역할**
- 사용자 입력 처리 → 모델 업데이트 → 뷰에 반영
- 주로 `UIViewController`로 구현

---

## ✅ MVC 패턴을 사용하는 이유

- 코드 분리를 통해 **유지보수가 쉬움**
- 한 부분 수정 시 **다른 영역에 영향 최소화**
- **모델과 뷰 재사용 가능 → 코드 중복 감소**

---

📚 오늘은 데이터 모델의 개념부터 Swift에서의 구조체 활용,  
그리고 MVC 아키텍처에서 데이터 모델이 어떤 역할을 하는지에 대해 학습했습니다.
