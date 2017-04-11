jsBasic_prac
=====

Javascript/jQuery 기초 스터디 실습

## 실습

### 1. 실습 저장소를 clone 합니다.

```bash
git clone [url]
git clone [url] [foldername]

git clone https://github.com/lets-grow-together/jsBasic_prac jsBasic_prac
```

### 2. 자신의 브랜치를 생성합니다.

branch 이름 규칙

[nickname]/[step]_[optional]

```bash
# example
yolo/jsPrac
yolo/jsPrac_try
yolo/jsPrac_test
```

### 3. 자신의 브랜치에서 실습을 진행합니다.

`start/` 폴더는 그대로 두고 `try/` 같은 폴더로 이름을 변경하고 복사해서 진행합니다.

```
..
start/
try/
```

### 4. 실습 완료 후 커밋하고 원격저장소로 공유합니다.

```bash
# add
git add [file-name]
git add .

# commit
git commit -m '완성'

# push
git push [remote-name] [branch-name]
git push origin yolo/jsPrac
```

### 5 master 브랜치가 업데이트 되었을 경우 

새로운 실습파일을 merge 합니다.

```bash
# 1. master 브랜치로 이동
git checkout master

# 2. master 브랜치에서 pull
git pull
git pull origin master

# 3. 자신의 브랜치로 이동하고 master 소스 merge
git checkout yolo/jsPrac
git merge master
```

3 ~ 5 반복 진행합니다.

*****

## git 기본 사용법

### branch

브랜치 생성 / 이동 / 조회

```bash
# 브랜치 만들고 이동
git checkout -b [branch-name]

# 브랜치 생성
git branch [branch-name]
# 브랜치 삭제
git branch -d [branch-name]
# 브랜치 이름 변경
git branch -m [old-branch-name] [new-branch-name]
# 리모트 브랜치 삭제
git push [remote-name] --delete [branch-name]
git push [remote-name] :[branch-name]

# 브랜치 이동
git checkout [branch-name]
# [target] 과 같은 커밋을 가리키는 브랜치를 새로 만들고 이동
git checkout -b [branch-name] [target]

# 브랜치 목록보기 - local
git branch
# 브랜치 목록보기 - remote
git branch -r
```

### add

```bash
# 저장소의 변경상태 확인
git status

# 파일 새로 추적 / 변경된 파일 스테이징하기
git add [file-name]
git add README

# 모든파일
git add .
```

### commit

```bash
# 로컬저장소에 있는 파일 변경사항의 스냅샷 기록
git commit -m 'commit message'
```

### push

```bash
# 로컬저장소에서 원격저장소로 공유
git push [remote-name] [branch-name]
git push origin yolo/jsPrac
```

### pull

원격저장소의 데이터를 가져와 자동으로 현재 작업하는 코드와 merge 한다.

```bash
git pull [remote-name] [branch-name]
git pull
git pull origin master
```

### merge

합칠 branch(target)에서 합쳐질 branch(source)를 merge 한다.

```bash
# 1
git checkout [target]
# 2
git merge [source]

git checkout master
git merge iss53
```