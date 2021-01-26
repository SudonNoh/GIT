## git 기본 사용법

### 1. git config(최초 1회 실행)
```git
// git commit에 사용될 username
git config --global user.name "uername"

// git commit에 사용될 email
git config --global user.email "id@email.com"

// 내용 확인
git config --list
```
   
   
### 2. git init
```git
// 로컬저장소로 설정할 프로젝트 위치로 이동
cd D:/PythonProject/Django

// 로컬저장소로 설정
// (main or master) 브랜치로 보이면 성공
git init

// 만약 init을 취소하려면 아래 명령어 입력
rm -r .git
```
   
   
### 3. git status
```git
// 로컬저장소 상태 확인
git status
```
   
   
### 4. git add
파일을 준비영역(Staging Area)으로 옮긴다. <b>GitHub와 연동하려면 git remote로 원격 저장소와 연결해야 한다.</b>
```git
// a.html 파일 추가
git add a.html

// 워킹 디렉토리 내 모든 파일을 추가
git add .

// 명령 프롬프트에서 상호작용하면서 추가
git add -i

// 진행중인 파일일 경우, Staging Area에서 워킹 디렉토리로 옮겨옴
git rm --cached a.html
git rm -r --cached .
```
   
   
### 5. git commit
Staging Area의 파일을 로컬저장소에 저장한다.
```git
// 에디터가 출력되고, 에디터에서 커밋 메시지 입력 후 저장하면 커밋됨
git commit

// 간단한 커밋 메시지를 입력 후 커밋
git commit -m "message"

// Staging Area에 들어간 파일에 대해서만
git commit -a -m "message"
```
   
   
### 6. git log
로컬저장소의 커밋 이력을 조회한다.
```git
// 커밋 이력 상세조회
git log

// 커밋 이력 중 커밋ID, 타이틀 메시지만 조회
git log --oneline

// 모든 브랜치 커밋 이력 조회
git log --oneline --decorate --graph --all

// 특정 파일의 변경 커밋 조회
git log -- a.html
```
   
   
### 7. git remote
로컬저장소와 원격저장소를 연결
```git
// GitHub 원격저장소와 연결
git remote add origin [원격저장소 주소]

// 연결된 원격저장소 확인
git remote -v
```
   
   
### 8. git push
원격저장소에 저장
```git
// 원격저장소에 저장
git push -u origin master

// 에러 - ! [rejected] master -> master (fetch first)
git pull origin master

// 에러 - ! [rejected] master -> master (non-fast-forward)
git push origin +master
   
   
### 9.git branch
브랜치를 생성, 수정, 삭제
```git
// 브랜치 확인
git branch

// 브랜치 생성
git branch [branch name]

// 브랜치 수정
git branch -m [old name] [new name]

// 브랜치 삭제
git branch -d [branch name]
```
   
   
### 10. git checkout
워킹 디렉토리의 소스를 특정 커밋 또는 특정 브랜치로 변경한다.
```git
// 특정 브랜치로 워킹 디렉토리 변경
git checkout [branch name]

// 특정 커밋으로 워킹 디렉터리 변경
git checkout [commit ID]
```
