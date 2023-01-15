# git

## git은 버전관리와 협업의 도구

우리는 문서를 작성하거나 공유할 때 파일의 이름만을 바꿔 카톡이나 디스코드에 파일을 올리곤 한다.

하지만 이 방법은 몇가지 문제점들이 있다.
1. 어떤 부분이 바뀌었는지 알 수 없다. 
2. 문서의 내용을 되돌리기도 어렵다.
3. 용량을 많이 차지한다.
4. 계속 다운로드 받아야 해서 협업할 때 불편하다.

이러한 불편한 점들 때문에 버전관리 시스템이라는 것이 등장한다.

버전관리 시스템(VCS, Version Control System)은 파일의 변경사항를 저장하고 원하는 시점의 버전을 다시 꺼내올 수 있는 시스템이다.

버전관리 시스템은 snapshot과 delta라는 개념을 이용해 버전을 관리한다.
- snapshot: 특정 시점에서의 파일 상태(현재 상태의 모든 정보)
- delta: 파일의 이전 상태와 비교한 변경사항

그 중에서 git은 분산 버전관리 시스템(DVCS, Distributed VCS)) 중 하나이다.

## 분산 버전관리 시스템

![image](https://user-images.githubusercontent.com/82245973/212524232-a78f274a-fb83-45ea-bea1-36a5c05cffdb.png)  

분산 버전관리 시스템에서는 메인 서버에 파일과 파일의 수정사항을 가지고 있고 사용자는 메인 서버에서 모든 복사본을 가져옵니다.

메모리 낭비가 있긴 하지만 서버의 문제가 발생하더라도 복제물로 작업을 진행할 수 있고 버전을 내 컴퓨터에서 관리하고 원할때마다 원격으로 서버에 올릴 수도 있고 서로 참조해가면서 협업도 가능합니다.

## git의 특징

git은 리눅스의 창시자, 리누스 토발즈가 만들었고 다음과 같은 특징을 가진다.

- 빠른 속도
- 단순한 구조
- 비선형적인 개발(수천 개의 동시 다발적인 브랜치)
- 완벽한 분산
- Linux 커널과 같은 대형 프로젝트에도 유용할 것(속도나 데이터 크기 면에서)

## git의 세가지 상태

git은 파일을 세가지 상태로 관리한다.

![image](https://user-images.githubusercontent.com/82245973/212529015-d015790b-76f3-4051-b3f5-9bdd9e27720b.png)  

- Committed: 데이터가 로컬 데이터베이스에 안전하게 저장됐다는 것을 의미한다.
- Modified: 수정한 파일을 아직 로컬 데이터베이스에 커밋하지 않은 것을 의미한다.
- Staged: 현재 수정한 파일을 곧 커밋할 것이라고 표시한 상태를 의미한다.

## git 사용법

0. 사용자 설정

```
git config --global user.name "username"
git config --global user.email user-eamil@email.com
```

1. local repository 만들기

    git으로 관리할 프로젝트 폴더를 만든다.

2. git init

    git init을 하게되면 프로젝트 폴더 내에 .git 폴더가 생성되며 해당 프로젝트 폴더의 모든 버전 관리 정보가 저장된다.

3. git add [file_name]

    변경 사항을 staging 영역으로 올린다.

4. git commit -m "commit message"

    staging 영역으로 올린 파일을 커밋한다.

5. git remote add orign [url]

    원격 저장소와 연결한다.

6. git push origin master

    연결된 원격 저장소에 변경사항을 올린다.

## 원격 저장소 받아오기

1. git clone [url]

    원격 저장소를 복제한다.

2. git add ~ git push

    이후 프로젝트 파일을 수정하고 add-commit-push의 과정을 거친다.

## 협업하기

보통 master 브랜치는 배포용이기 때문에 바로 master 브랜치에 커밋하는 경우는 없다.

master 브랜치와 독립적으로 개발하기 위해 branch라는 가지를 만들어 개발을 진행할 수 있다.

1. git branch [branch-name]

    새로운 브랜치를 만든다.

2. git checkout [branch-name]

    해당 브랜치로 git의 HEAD를 옮긴다. HEAD란 현재 git이 가리키는 브랜치이다.

2. git add ~ commit

    이후 새 기능을 개발하고 테스트해보고 master 브랜치와 합칠 준비가 되면 commit한다.

3. git merge [branch-name]

    두개의 브랜치를 합친다.

4. git branch -d [branch-name]

    다 쓴 브랜치는 지운다.

## 변경사항 받아오기

push하기 전에 원격 저장소의 내용이 바뀌면 버전이 달라 충돌이 일어난다.

push하기 위해선 원격저장소의 변경된 부분을 받아 merge 해주고 push 해야한다.

1. git fetch origin

    원격 저장소의 변경된 부분을 받아온다.

2. git pull origin master

    원격 저장소의 변경된 부분을 받아와 알아서 merge해준다.

## 실수 했을 경우

프로젝트 진행 도중 파일을 지워버리거나 덮어버린 경우 되돌리는 방법이 있다.

1. git reset [commit-hash]

    reset은 해당 커밋으로 버전을 되돌리고 이후 커밋 이력을 없앤다.

2. git revert [commit-hash]

    revert는 해당 커밋의 내용을 되돌리고 지우는 커밋을 추가한다.

## 오픈소스에 기여하기

오픈소스에 기여하기 위해서는 오픈소스 레포를 포크하여 내 원격 레포로 복제하고 원하는 기능을 추가하거나 성능을 개선한 후  내 원격 래포(origin)에 커밋, 푸쉬한 후 오픈소스 레포(upstream)에 Pull Request 요청을 보내면 오픈소스 레포 관리자가 해당 내용을 검토 후 merge를 하게된다. 그러면 내 수정사항이 오픈소스 레포에 반영이 된다.

Pull Request를 하는 법
1. Fork
2. Clone + Remote 설정
3. Branch 생성
4. add, commit, push
5. Pull Request(PR) 생성
6. Code Review
7. Merge PR
8. Merge 이후 branch 삭제 및 동기화