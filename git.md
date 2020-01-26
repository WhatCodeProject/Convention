# Git Convention

> 소규모 인원에서 협업하기 적합한 Feature Branch Workflow 방식을 사용한다.  
> [참고 링크](https://gmlwjd9405.github.io/2017/10/27/how-to-collaborate-on-GitHub-1.html)

-   원격 저장소, 로컬 저장소의 차이에 대해 이해한다.
-   기본적인 git 사용법(init, add, commit, push, pull, clone)에 대해 이해한다.
-   협업에 필요한 기능인 branch, checkout에 대해 이해한다.
-   pull fetch의 차이에 대해 이해한다.
-   Pull Request에 대해 이해한다.

### 초기 설정

-   [https://github.com/WhatCodeProject](https://github.com/WhatCodeProject) 이하의 Repository를  
    중앙원격 저장소로 지정
-   git-flow는 master branch와 feature branch로 구분한다.

### Repository

-   [Spring Boot](https://github.com/WhatCodeProject/SpringBoot)
-   [Vue.js](https://github.com/WhatCodeProject/Vue)

### git-flow

#### 1.Clone

-   개발자는 해당 Repository를 clone 하여 초기 설정이 완료된 프로젝트를 자신의 로컬 저장소로 가져온다.

```bash
# SpringBoot
git clone https://github.com/WhatCodeProject/SpringBoot.git

# Vue
git clone https://github.com/WhatCodeProject/Vue.git
```

#### 2.Brach, Checkout

-   현재 자신의 branch를 확인한다.
-   feature 개발을 위한 branch를 feature/\[기능 이름\]으로 만든다.
-   해당 branch로 checkout 한다.

```bash
# branch 확인
git branch

# feature 개발을 위한 branch 생성
git branch feature/init-table

# 해당 branch로 이동
git checkout feature/init-table

# 이동이 되었는지 한번 더 확인
git branch
```

#### 3\. Add, Commit, Push

-   feature branch에서 개발이 완료된 후 add, commit, push를 통해 중앙 원격 저장소에 올린다.

```bash
git add .

git commit -m "commit message"

git push origin feature/init-table
```

#### 4\. Pull Request

-   중앙 원격 저장소에 자신이 개발한 branch를 push 한 개발자는 Pull Request를 한다.

#### 5\. Merge

-   회의 날에 팀원들과 리뷰 후 merge가 결정 났다면 Pull Request 한 개발자가 merge를 한다.

#### 6\. Pull

-   merge가 되었다면 개발자들은 자신의 local 저장소의 branch를 master로 checkout 한다.
-   그 후 merge 된 commit을 pull 하여 최신 상태로 동기화한다.

```bash
git checkout master

git pull origin master
```
