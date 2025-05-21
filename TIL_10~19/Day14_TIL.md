# 📘 Day 14 - Today I Learned


 **🔑 Keywords**  
 `Storyboard 제거`, `코드베이스 UI`, `SceneDelegate`, `Info.plist`, `AppDelegate`
 
---

## ✅ 1. Main.storyboard 파일 삭제
- `Main.storyboard`를 프로젝트에서 삭제 (`Move to Trash`)
- Info.plist와 Build Settings에서의 참조도 함께 제거해야 함

---

## ✅ 2. Info.plist 설정 수정
```xml
<!-- 제거할 항목 -->
<key>UIMainStoryboardFile</key>
<string>Main</string>
```
📌 또는 Xcode UI에서:
- Info 탭 → `Main Interface` 항목을 **비워둔다**

---

## ✅ 3. SceneDelegate.swift 수정
```swift
func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
    guard let windowScene = (scene as? UIWindowScene) else { return }
    
    window = UIWindow(windowScene: windowScene)
    window?.rootViewController = PuddingVC() // 시작 뷰컨트롤러 지정
    window?.makeKeyAndVisible()
}
```

---

## ✅ 4. AppDelegate.swift 수정 (iOS 12 이하 대응 시)
```swift
window = UIWindow(frame: UIScreen.main.bounds)
window?.rootViewController = PuddingVC()
window?.makeKeyAndVisible()
```

---

## ✅ 5. Build Settings 확인
- `Project` > `Target` > `Build Settings` 검색창에 `storyboard` 입력
- `UIKit Main Storyboard File Base Name` 항목이 있다면 삭제

---

## ✅ 6. 앱 실행 테스트
- 시뮬레이터에서 정상 실행되는지 확인
- 코드 기반으로 레이아웃이 잘 적용되는지 확인

---

## 📌 정리

| 항목 | 해야 할 일 |
|------|-------------|
| Storyboard 삭제 | `.storyboard` 파일 및 관련 설정 제거 |
| Info.plist 수정 | `UIMainStoryboardFile` 제거 |
| SceneDelegate / AppDelegate 설정 | 루트 뷰 수동 설정 |
| Build Settings 정리 | Storyboard 참조 삭제 |

이 과정을 거치면 완전히 **스토리보드 없는 코드 기반 UI** 프로젝트가 된다 💪
