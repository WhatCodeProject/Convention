# Spring Boot Convention
## [Repository](https://github.com/WhatCodeProject/SpringBoot)
## 프로젝트 구조

-   main
    -   java
        -   config
        -   domain
            -   Member
                -   member
                -   MemberRepository (Querydsl 사용 시 패키지로 변경 후 사용)
                -   MemberService
                -   MemberController
                -   dto
                    -   Dtos..
                -   team
                -   code
                -   chat(좋은 이름 생각나면 변경)
                -   common
                    -   error
                    -   aop
        -   SpringBootApplication.java
    -   resource
        -   application.yml

## 코딩 컨벤션

### 메서드명

-   동사로 시작하고 가능한 전치사를 통해 의미를 확실히 전달
-   ex) validateCommentMember X, validateCommentOfMember O

### Layer

#### Repository

-   findBy(Long memberId) X
-   findByMemberId(Long id) O

#### Service

-   Create
    -   save
-   Update
    -   update
-   Read
    -   단일: findById, findByname
    -   복수: findMembers
-   Delete
    -   delete

#### Controller

-   REST API 규칙에 맞게 url 리소스 주소를 명시적으로 작성한다
-   /api/members/
