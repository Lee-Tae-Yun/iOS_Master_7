# 📘 Day 18 - Today I Learned

**🔑 Keywords**: `enum`, `Associated Values`, `Raw Values`, `MVC`, `리팩토링`, `코드 설계`

 ## 🔍 Today Error or Issues  
> **`Issues`** : 기존에 전역 변수로 선언한 데이터 흐름을 컴포넌트 기반으로 리팩토링하려고 했는데, Model과 View의 책임 구분이 애매하다.
## 🛠️ Troubleshooting
기존에 작성한 코드가 기능별로 나뉘지 않고 한 파일에 뭉쳐 있어 유지보수가 어려웠다.  
이를 개선하기 위해 `MVC 패턴`을 기반으로 구조 재설계를 시도했다.

- Model: 사용자 정보와 관련된 구조체 및 데이터 로직
- View: UI 요소들을 ViewController와 분리하려고 시도함
- Controller: 현재 ViewController가 Model과 View의 역할까지 모두 담당하고 있어, 이 부분을 분리하는 데 어려움을 겪음

⚠️ 하지만 구체적으로 어떤 클래스/파일로 나눠야 할지 기준을 잡지 못해서 구조 설계를 마무리하지 못했다.  
→ 내일은 코드 베이스 MVC 예제 프로젝트를 참고해 분리 기준을 좀 더 명확히 할 예정.

## 📝 Learning Summary
### 📌 열거형 (Enum)
- 관련된 값을 그룹화할 수 있는 데이터 타입
- 두 가지 주요 특징:
  - **`Associated Values` (연관값)**: (예: case success(data: String))
  - **`Raw Values` (원시값)**: case에 기본값 지정, 옵셔널로 반환 가능


### 📌 Class vs Struct (요약)
- 저장 방식: 참조 타입 vs 값 타입
- 복사 방식, 상속 가능 여부 등은 추후 학습 예정

# 📘 Lesson Learned
다음부턴 반드시 설계 흐름을 간단히 도식화한 뒤 코드를 시작하고, 최소한의 책임 구분(MVC 기준)을 해보고 시작하자.

