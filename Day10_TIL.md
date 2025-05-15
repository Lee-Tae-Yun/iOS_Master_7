# 📘 Day 10 - Today I Learned

**🔑 핵심 키워드:**  
`배열 추가`, `배열 삭제`, `filter`, `sort`, `딕셔너리 순회`, `updateValue`, `removeValue`

---

## 📌 배열(Array) 심화

### ✅ 요소 추가

```swift
var numbers = [1, 2, 3]

numbers.append(4)
numbers.insert(0, at: 0)
numbers += [5, 6]
```

- `append(_:)`: 배열 끝에 요소 추가
- `insert(_:at:)`: 특정 위치에 요소 삽입
- `+= 연산자`: 여러 요소를 한꺼번에 추가

---

### ✅ 요소 삭제

```swift
numbers.remove(at: 2)
numbers.removeFirst()
numbers.removeLast()
numbers.removeAll()
```

- `remove(at:)`: 특정 인덱스 요소 삭제
- `removeFirst()`, `removeLast()`: 맨 앞/뒤 요소 삭제
- `removeAll()`: 전체 요소 삭제

---

### ✅ 필터링 (filter)

```swift
let numbers = [1, 2, 3, 4, 5, 6]
let evenNumbers = numbers.filter { $0 % 2 == 0 }
print(evenNumbers) // [2, 4, 6]
```

- `filter(_:)`: 조건을 만족하는 요소만 남긴 새 배열 반환

---

### ✅ 정렬

```swift
let numbers = [3, 1, 4, 2, 5]

let sortedAsc = numbers.sorted()             // [1, 2, 3, 4, 5]
let sortedDesc = numbers.sorted(by: >)       // [5, 4, 3, 2, 1]

var mutableNumbers = [3, 1, 4, 2, 5]
mutableNumbers.sort()                        // [1, 2, 3, 4, 5]
mutableNumbers.sort(by: >)                   // [5, 4, 3, 2, 1]
```

- `sorted()`: 정렬된 새 배열 반환
- `sort()`: 원본 배열 정렬

---

## 📌 딕셔너리(Dictionary) 심화

### ✅ 요소 추가 및 수정

```swift
var studentScores: [String: Int] = [:]

studentScores["태윤"] = 95
studentScores["태윤"] = 100 // 기존 값 수정

let oldValue = studentScores.updateValue(80, forKey: "이든")
print(oldValue) // Optional(100) 또는 nil
```

- `[]`: 새 키 추가 또는 기존 값 변경
- `updateValue(_:forKey:)`: 값 수정 + 이전 값 반환

---

### ✅ 요소 삭제

```swift
studentScores.removeValue(forKey: "태윤")
studentScores.removeAll()
```

- `removeValue(forKey:)`: 삭제 + 기존 값 반환
- `removeAll()`: 전체 삭제

---

### ✅ 순회 (for-in)

```swift
for (name, score) in studentScores {
    print("\(name): \(score)")
}

for name in studentScores.keys {
    print(name)
}

for score in studentScores.values {
    print(score)
}
```

- `for-in`: 모든 키와 값을 반복
- `keys`, `values`: 키 또는 값만 반복

---

### ✅ 필터링 (filter)

```swift
let highScores = studentScores.filter { $0.value > 90 }
print(highScores) // 조건을 만족하는 (key, value) 쌍만 남김
```

- `filter(_:)`: 조건 만족하는 요소만 필터링 가능

---

📚 오늘은 배열과 딕셔너리의 고급 기능인  
**요소 추가, 삭제, 정렬, 필터링, 순회, 값 변경/반환 처리** 등을 학습했습니다.
