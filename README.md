# Cos-House-Backend

'오늘의 집'을 벤치마킹한 MZ세대 타겟 인테리어 커뮤니티 + 쇼핑 통합 플랫폼입니다.
Spring Boot 기반의 E-Commerce 플랫폼으로, 상품 관리/주문/결제/커뮤니티 기능을 제공합니다.

## 프로젝트 개요

- 프로젝트명: Co's House (COS)
- 개발 기간: 2025.09 ~ 2025.10
- 팀 구성: 5명
- 담당 역할: Backend

## 담당 업무

### 마이페이지
- 개인정보 관리를 위해 회원정보 수정 기능 구현 (이메일, 비밀번호, 주소 등)
- 구매 후기 공유를 위해 마이페이지 리뷰 기능 구현
- 사용자 경험 개선을 위해 마이페이지 UI 리팩토링
- 계정 정리를 위해 회원 탈퇴 처리 구현

### 관리자 페이지
- 상품 운영을 위해 상품 관리 및 검색 기능 구현
- 주문 처리를 위해 주문 관리 기능 구현

### 커뮤니티
- 사용자 소통을 위해 댓글 기능 구현
- 게시글 수정 기능 구현

### 공통
- 이벤트 페이지 디자인 리팩토링
- CSS 리팩토링 및 메인 페이지 수정

## 기술 스택

- Language: Java 21
- Framework: Spring Boot 3.5.5
- ORM: Spring Data JPA, Querydsl 5.0.0
- Security: Spring Security 6 (Session-based)
- Template Engine: Thymeleaf
- DB: MySQL 8.4
- Infrastructure: Docker Compose, Prometheus, Grafana
- Payment: Toss Payments API
- OAuth2: Kakao, Naver

## 실행 방법

### 1) 인프라 실행
```bash
docker-compose up -d
```

### 2) 데이터베이스 초기화
```bash
mysql -h 127.0.0.1 -P 13306 -u root -proot cos
source document/sql/1_table_insert.sql;
source document/sql/0_user_role_migration.sql;
source document/sql/2_basic_data_insert.sql;
```

### 3) 애플리케이션 실행
```bash
./gradlew bootRun
```

## 관련 레포지토리

- GitHub: [KernelSevenBird](https://github.com/KernelSevenBird)
