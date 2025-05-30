# 📘 Day 15 - Today I Learned

**🔑 Keywords**: `git branch 삭제`, `UserDefaults`, `CoreData`, `파일저장`, `Keychain`, `iOS 데이터 저장`, `보안 저장 방식`

 ## 🔍 Today Error or Issues  
> **Error** git merge후 원격 저장소에서 브랜치를 삭제하려고 git branch -d branch name 명령어 실행하니 error: The branch branch name is not fully merged.발생
원격 저장소에 merge가 안되어있다고 로컬에서 브랜치가 삭제가 안되는 문제.

## 🛠️ Troubleshooting
원격 저장소에 브랜치 목록을 확인 결과 브랜치가 삭제가 안돼있는걸 발견
git fetch --prune 를 사용하여 원격 저장소의 내용을 최신화 한 후 
다시 pull 하고 git branch -d branch name 실행하여 문제 해결

## 📝 Learning Summary
데이터 저장 방법 UserDefaults, CoreData, 파일저장, Keychain 이렇게 4가지가 있다.  
**UserDefaults** - 간단한 키-값 (Key - Value)저장소 - 간단한 설정값 저장 가능, 보안이 취약하고 대량 데이터 저장에 부적합 - 앱 설정값, 로그인 상태  
**CoreData** - 데이터를 객체 단위로 저장하고 관리하는 데이터베이스 프레임워크 - 대량의 데이터 저장가능, 관계형 데이터 처리, 설정이 복잡, 최적화 필요 - 사용자 정보, 데이터 관리앱  
**파일저장** - 데이터를 파일형태로 저장하는 방식 - 다양한 파일 포맷 저장 가능, 검색 및 관리 어려움 - JSON,CSV,이미지,텍스트 저장  
**Keychain** - 보안이 중요한 데이터를 저장하는 방식(apple의 Security.fraemwork를 사용한다.) - 민감한 정보 저장가능, 암호화 지원, 사용법이 어렵고 속도가 느림 - 비밀번호, API키, 인증토큰  

**간단한 설정값:** Uesr-Defaults
**대량의 데이터 및 관계형 데이터:** CoreData
**문서, 이미지등 파일저장:** 파일저장
**보안이 중요한 데이터:** Keychain

## 📘 Lesson Learned
팀 프로젝트를 완성하였는데 밋밋한 부분이 많았는데 조금 더 열심히 공부해서 이쁜 UI를 만들어 보자!
