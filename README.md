# fashion-promotion-backend (이름 미정)
> 패션관련 프로젝트입니다. (아무것도 모르지만 박치기하면서 하고싶은거 하기)

## 프로젝트 소개
- **프로젝트 명**: (이름 미정)
- **프로젝트 기간**: 2024.12.01 ~ .
- **프로젝트 목표**:
  - 부족한 기술 스택의 숙련도를 높이며, A부터 Z까지 백엔드 개발 프로세스를 직접 경험.
    - 기획, 요구사항 분석부터 API 설계, 구현, 배포, 유지보수
  - 기술 스택의 효율적인 사용법과 문제 해결 능력을 강화. 

<br>

## 기술 스택:
- Java(or Kotlin), Spring Boot
- Spring Web
- Spring Data JPA
    - Lombok
    - PostgreSQL Driver
- Spring Security
    - OAuth2 Client
- Validation
- Spring REST Docs
- **추후 도입 예정**: FCM, Coolsms, Spring Batch, Spring Cloud AWS, Redis

<br>

## 프로젝트 구조
### 디렉터리 구조
```plantuml
src/
├── domain/                          
│   ├── users/                       // 사용자 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── profiles/                    // 프로필 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── products/                    // 제품 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── collections/                 // 컬렉션 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── posts/                       // 게시글 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── comments/                    // 댓글 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── events/                      // 이벤트 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   ├── follows/                     // 팔로우 관리 도메인
│   │   ├── domain/                  
│   │   ├── service/                 
│   │   ├── facade/                  
│   │   └── presentation/            
│   └── reviews/                     // 리뷰 관리 도메인
│       ├── domain/                  
│       ├── service/                 
│       ├── facade/                  
│       └── presentation/            
└── global/                          // 공통 모듈
    ├── config/                      
    ├── error/      
    │   ├── exception/
    │   └── handler/                 
    ├── utils/                       
    └── security/   
        └── jwt/
           ├── filter/
           └── exception/                      
```

### 아키텍처 구조
**다이어그램으로 수정 예정.**
```plantuml
[ Presentation Layer ]    -> 컨트롤러, 요청/응답 DTO
         ↓
[  Facade Layer  ]        -> 단일 진입점, 여러 서비스 조합
         ↓
[ Domain Layer ]          -> 엔티티, 비즈니스 로직, 서비스, 리포지토리
         ↓
[ Infrastructure Layer ]  -> 데이터베이스 연동, 외부 API 통신
         ↓
[ Global Layer ]          -> 전역 설정, 예외 처리, 유틸리티
```

<br>

## 알게된 점