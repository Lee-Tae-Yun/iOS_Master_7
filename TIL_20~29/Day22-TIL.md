# 📘 Day 22 - Today I Learned

**🔑 Keywords**: `Memory Management`, `ARC`, `Generic`  

## 🔍 Today Error or Issues  
오늘은 Swift의 메모리 구조와 ARC, 제네릭에 대해 개념을 정리했지만,  
ARC의 strong, weak, unowned 차이가 처음에는 다소 헷갈렸다.

## 🛠️ Troubleshooting
헷갈린 개념들을 다시 정리하면서 이해를 명확히 했다.  
- 메모리 구조  
    - Code 영역: 컴파일된 코드 저장  
    - Data 영역: 전역/정적 변수 저장  
    - Heap 영역: 클래스와 같은 참조 타입 인스턴스 저장  
    - Stack 영역: 지역변수, 매개변수 등 값 타입 저장  
- ARC (Automatic Reference Counting)  
    - 참조 타입의 인스턴스를 자동으로 메모리 관리  
    - 참조 카운트 증가/감소는 컴파일 타임에 삽입됨  
- 참조 방식  
    - strong: 기본값, 참조 시 카운트 +1  
    - weak: 카운트 증가 없이 참조, 해제 시 자동으로 nil  
    - unowned: 카운트 증가 없이 참조, 해제된 객체 접근 시 crash
- Generic (제네릭)
    - 코드의 재사용성과 유연성을 높이기 위해 사용
    - 함수나 타입에서 타입을 미리 정의하지 않고 사용하는 시점에 결정

```swift
func swap<T>(_ a: inout T, _ b: inout T) {
    let temp = a
    a = b
    b = temp
}
```

## 📝 Learning Summary
Swift의 메모리 구조를 다시 살펴보며 ARC의 동작 원리와 참조 방식의 차이를 이해했다.  
제네릭의 개념과 활용 방식도 다시 정리함으로써, 더 유연하고 재사용 가능한 코드를 작성할 수 있는 기반을 다졌다.

## 📘 Lesson Learned
기본 문법을 넘어서 메모리 관리와 제네릭까지 이해하면서 **Swift 언어가 왜 안전하고 강력한지** 다시 체감했다.  
`ARC`의 `weak`, `unowned`는 앞으로 클로저나 `ViewModel` 설계 시 꼭 고려해야 할 포인트이고, `제네릭은 코드를 추상화`하는 데 매우 중요한 도구라 더 많이 연습해 봐야겠다.  
작은 개념이라도 명확히 이해하고 넘어가는 습관을 계속 유지해야겠다. 💪