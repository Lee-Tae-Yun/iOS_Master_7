# 📘 Day 19 - Today I Learned

**🔑 Keywords**: `String`, `Index`, `Character`, `Array 변환`

 ## 🔍 Today Error or Issues  
> Error: No exact matches in call to subscript
Swift에서 String 타입을 정수 인덱스로 바로 접근하려 하자 위와 같은 에러가 발생했다.

Swift의 String은 단순한 Character의 배열처럼 보이지만, 내부적으로는 Unicode 스칼라(문자 단위) 기반으로 동작하므로 String[index]처럼 숫자 인덱스로 직접 접근이 불가능하다. 이는 다른 언어들과 달리 Swift가 문자열의 정확성과 안정성을 중시하기 때문이다.

## 🛠️ Troubleshooting
이 문제를 해결하기 위해 String을 먼저 Array로 변환한 후 인덱스를 통해 접근하는 방식으로 해결하였다.
```swift
let str = "123"
let chars = Array(str)
print(chars[0]) // '1'
```
이렇게 하면 배열 인덱스 방식을 활용할 수 있어서 String 내 특정 문자에 직접 접근할 수 있다.

## 📝 Learning Summary
- Swift의 String은 단순 인덱스 접근을 허용하지 않는다.
- Unicode-compliant한 문자열 처리를 위해 Swift는 index 타입을 사용하거나, 배열로 변환해서 다루는 방식이 필요하다.
- 문자열을 배열로 변환하면 [Character] 타입이 되며, 인덱스를 통해 안전하게 접근 가능하다.
- 에러 메시지를 잘 읽고 해당 타입이 실제로 어떤 형태인지 파악하는 습관이 중요하다.

## 📘 Lesson Learned
문자열을 다룰 때 Swift는 타입 안정성과 문자 정확성을 보장하기 위해 인덱스 접근을 엄격하게 제한한다는 것을 배웠다.
이 경험을 통해 Swift의 타입 시스템이 얼마나 강력하고 안전 지향적인지 느낄 수 있었고, 단순한 실수에서 시작된 에러가 더 깊은 언어 철학을 이해하게 해준 계기가 되었다.