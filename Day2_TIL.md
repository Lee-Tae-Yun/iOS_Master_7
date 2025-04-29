# 📘 Day 2 Today I Learned - Swift와 iOS생태계 이해하기

<br>

## 🧑‍💻 Swift란?
Apple이 개발한 **프로그래밍 언어**로,  
2014년 WWDC에서 처음 공개되었습니다.  

macOS, iOS, watchOS, tvOS 등 Apple 플랫폼 앱 개발에 사용됩니다.

<br>

## 🍏 iOS 생태계를 구성하는 주요 요소

| 구성 요소       | 설명                                             |
|----------------|--------------------------------------------------|
| **App Store**  | 앱을 배포하고 다운로드할 수 있는 플랫폼         |
| **iOS**        | iPhone과 iPad에서 실행되는 운영체제             |
| **Xcode**      | iOS 앱을 개발하는 데 사용하는 통합 개발 환경    |
| **Swift**      | iOS 앱을 개발할 때 사용하는 프로그래밍 언어     |

<br>

## 🧪 Swift Playgrounds란?

- Apple 제공의 **무료 코딩 학습 앱 (iPad, Mac)**
- Xcode 없이도 Swift 코드 실행 가능
- SwiftUI 앱 제작도 가능 (iPadOS 15 이상)

<br>

# 과제

<br>

## ✅ Swift의 주요 특징 (3가지)

1. **안전성 (Safety)**  
   → 엄격한 문법을 통해 프로그래머의 실수를 방지

2. **신속성 (Fast)**  
   → C 언어 수준의 성능으로 빠른 실행 속도 제공

3. **표현력 (Expressive)**  
   → 간결하면서도 표현력이 풍부한 구문 제공

## 📱 Swift가 iOS 개발에 중요한 이유

Swift는 Apple이 직접 개발하고 최적화한 언어로, **iOS 개발에 가장 적합한 언어**입니다.  

1. 🍎 Apple 생태계에 최적화
2. ⚡ 뛰어난 성능 & 메모리 효율 향상
3. ✍️ 간결하고 현대적인 문법
4. ✅ 안전성과 가독성
5. 🌐 오픈소스 & 상호 운용성  

## 💻 Xcode의 역할

Xcode는 Apple 공식 **통합 개발 환경(IDE)** 으로, 다음과 같은 역할을 수행합니다:

- Swift 및 Objective-C로 앱 코드 작성
- UI 설계: Storyboard 또는 SwiftUI
- 시뮬레이터를 통한 디버깅 및 테스트
- 앱 서명 및 배포 (App Store 연동 포함)

## 🚀 App Store 배포 순서

1. **Apple Developer 등록**
2. **앱 준비 및 설정**  
   - App ID, 인증서, Provisioning Profile
3. **앱 아카이브 및 업로드**
4. **TestFlight (선택)**  
   - 베타 테스트 및 피드백 수집
5. **App Review (심사)**  
   - 보통 1~3일
6. **출시**
7. **배포 후 유지보수**

### ✏️ Swift Playground에서 작성 가능한 코드 예시

- Swift 기본 문법
- 애니메이션 기반 미션
- SwiftUI 기반 간단한 앱 UI
- 실시간 실행 및 피드백


## 🆚 Swift Playgrounds vs Xcode

| 항목              | Swift Playgrounds     | Xcode                         |
|-------------------|------------------------|-------------------------------|
| 🎯 대상           | 입문자, 학생           | 개발자, 실무자                |
| 💻 플랫폼         | iPad, Mac              | Mac 전용                      |
| 🔧 기능 범위       | Swift 학습, 앱 연습     | Apple 플랫폼 전체 앱 개발     |
| 🛠 UI 도구        | SwiftUI 위주           | SwiftUI + Storyboard          |
| 🚀 배포           | 제한적 (iPad에서만)     | 정식 App Store 배포 가능     |
| 🐞 디버깅         | 실시간 결과 확인       | 고급 디버깅 도구 제공         |
| 📦 확장성         | 패키지 제한 있음        | 외부 프레임워크 완전 지원     |

---
