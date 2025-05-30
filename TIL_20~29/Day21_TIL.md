# 📘 Day 21 - Today I Learned

**🔑 Keywords**: ` SwiftLint`, `Xcode`, `CodeStyle`, `CodeConvention`

 ## 🔍 Today Error or Issues  
 > **`Issues`** : Xcode 프로젝트에서 코드 스타일 규칙을 자동으로 검사하고 싶은데, SwiftLint 적용 방식이 명확하지 않았다.

## 🛠️ Troubleshooting
1. Homebrew로 SwiftLint 설치
    ```
    brew install swiftlint
    ```
2.	Xcode 프로젝트에 실행 스크립트 추가  
	•	Xcode > Project > Target > Build Phases > + > New Run Script Phase  
	•	아래 스크립트를 입력:

    ``` swift
    if which swiftlint > /dev/null; then
        swiftlint
    else
        echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"  
    fi
    ```

## 📝 Learning Summary
SwiftLint는 Swift 코드의 스타일과 일관성을 유지하기 위한 도구로, 간단한 설정으로 Xcode에서 바로 적용할 수 있었다.
특히 협업 시 코드 컨벤션을 유지하고, 리뷰 시간을 줄이는 데 도움이 될 수 있다.

## 📘 Lesson Learned
개발 초기부터 코드 스타일을 도구로 자동 검사하는 습관을 들이는 것이 중요하다고 느꼈다.
이번 기회를 통해 Lint 도구를 적용하는 것 자체가 좋은 개발 문화의 시작이라는 걸 실감했다.
앞으로 팀 프로젝트에도 SwiftLint를 적용하여 일관된 코드 품질을 유지해야겠다.