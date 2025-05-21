# 📘 Day 13 - TIL

**🔑 Keywords**: Git, Git 명령어, GitHub 협업, 브랜치, 커밋, push, pull, SSH

---

## 🧭 Git 시작 및 설정

| 명령어 | 설명 |
|--------|------|
| `git init` | 현재 폴더를 Git 저장소로 초기화 |
| `git clone [URL]` | 원격 저장소 복제 (복사) |
| `git config --global user.name "이름"` | 사용자 이름 설정 |
| `git config --global user.email "이메일"` | 사용자 이메일 설정 |

---

## 📋 저장소 정보 확인

| 명령어 | 설명 |
|--------|------|
| `git status` | 현재 상태 확인 (추적 여부, 변경 여부 등) |
| `git log` | 커밋 기록 확인 |
| `git remote -v` | 연결된 원격 저장소 확인 |
| `git branch` | 로컬 브랜치 목록 확인 |
| `git branch -r` | 원격 브랜치 목록 확인 |
| `git show` | 특정 커밋 상세 보기 |

---

## 🌿 브랜치 관련

| 명령어 | 설명 |
|--------|------|
| `git branch 브랜치명` | 새 브랜치 생성 |
| `git checkout 브랜치명` | 브랜치 이동 |
| `git checkout -b 브랜치명` | 새 브랜치 생성 + 이동 |
| `git switch 브랜치명` | 브랜치 이동 (신규 방식) |
| `git merge 브랜치명` | 다른 브랜치를 병합 |
| `git branch -d 브랜치명` | 병합된 브랜치 삭제 |
| `git branch -D 브랜치명` | 강제 삭제 |
| `git push origin --delete 브랜치명` | 원격 브랜치 삭제 |

---

## ✅ 커밋 관련

| 명령어 | 설명 |
|--------|------|
| `git add .` | 전체 변경 파일 스테이징 |
| `git add 파일명` | 특정 파일만 스테이징 |
| `git commit -m "메시지"` | 커밋 생성 |
| `git commit -am "메시지"` | 수정된 파일을 add + commit 한 번에 |
| `git reset HEAD 파일명` | staged 취소 |
| `git restore --staged 파일명` | staged 상태 해제 |

---

## 🔄 원격 저장소 (Push / Pull)

| 명령어 | 설명 |
|--------|------|
| `git remote add origin [URL]` | 원격 저장소 등록 |
| `git push -u origin 브랜치명` | 첫 push (브랜치 연결 포함) |
| `git push` | 원격 브랜치에 push |
| `git pull origin 브랜치명` | 원격에서 최신 내용 가져오기 |
| `git fetch origin` | 정보만 받아오기 (병합 X) |

---

## 🧹 기타 명령어

| 명령어 | 설명 |
|--------|------|
| `git diff` | 변경된 내용 비교 |
| `git stash` | 변경사항 임시 저장 |
| `git stash pop` | 임시 저장 내용 복원 |
| `git clean -fd` | 추적되지 않은 파일/폴더 삭제 |
| `git reset --hard` | 전체 변경사항 초기화 |

---

## 🔐 인증 관련 (토큰, SSH)

| 명령어 | 설명 |
|--------|------|
| `ssh-keygen -t ed25519 -C "이메일"` | SSH 키 생성 |
| `git remote set-url origin [SSH_URL]` | SSH 주소로 변경 |
| `git credential-osxkeychain erase` | macOS 인증 초기화 |

---

## 🕵️ 기록 조회

| 명령어 | 설명 |
|--------|------|
| `git log --oneline --graph` | 커밋 로그 요약 (그래프 포함) |
| `git reflog` | HEAD 이동 기록 보기 |
| `git show 커밋ID` | 특정 커밋 상세 내용 보기 |

---

## 🤝 GitHub 협업 흐름

1. `git clone URL` → 원격 저장소 복제  
2. `git checkout -b 브랜치명` → 작업할 브랜치 생성 및 이동  
3. `git add .` → 변경사항 스테이징  
4. `git commit -m "메시지"` → 커밋  
5. `git push -u origin 브랜치명` → push 및 원격 브랜치 연결  
6. GitHub에서 PR(Pull Request) 생성  
7. 리뷰 완료 후 `merge`  
8. `git push origin --delete 브랜치명` → 원격 브랜치 삭제  
9. `git branch -d 브랜치명` → 로컬 브랜치 삭제  
10. `git pull origin 브랜치명` → 최신 내용 동기화  
