# \# Social Commerce Backend

# 

# \## 프로젝트 소개

# 

# Social Commerce Backend는 사용자가 상품을 조회하고 구매할 수 있을 뿐만 아니라, 리뷰, 좋아요, 팔로우 같은 소셜 기능도 함께 사용할 수 있는 소셜 커머스 플랫폼 백엔드 프로젝트입니다.

# 

# 이 프로젝트는 Java/Spring 기반 백엔드 개발 역량을 기르기 위해 회원, 인증, 상품, 장바구니, 주문, 결제, 정산, 리뷰, 좋아요, 팔로우 기능을 설계하고 구현하는 것을 목표로 합니다.

# 

# \---

# 

# \## 프로젝트 목표

# 

# \* Java/Spring 기반 백엔드 프로젝트 설계 및 구현

# \* REST API 설계 연습

# \* 회원, 상품, 주문, 결제, 정산 도메인 이해

# \* 리뷰, 좋아요, 팔로우 등 소셜 기능 설계

# \* GitHub 커밋 기록을 통한 포트폴리오 관리

# \* README 기반 설계 문서 작성 경험 쌓기

# 

# \---

# 

# \## 사용자 역할

# 

# \### Customer

# 

# 일반 구매자입니다.

# 

# \* 회원가입

# \* 로그인

# \* 상품 조회

# \* 장바구니 관리

# \* 주문 생성

# \* 결제

# \* 주문 내역 조회

# \* 리뷰 작성

# \* 상품 좋아요

# \* 판매자 팔로우

# 

# \### Seller

# 

# 상품을 판매하는 사용자입니다.

# 

# \* 상품 등록

# \* 상품 수정

# \* 상품 삭제

# \* 주문 확인

# \* 배송 상태 변경

# \* 판매 내역 조회

# \* 정산 내역 조회

# 

# \### Admin

# 

# 서비스 관리자입니다.

# 

# \* 회원 관리

# \* 상품 관리

# \* 주문 관리

# \* 신고 리뷰 관리

# \* 정산 관리

# 

# \---

# 

# \## 주요 기능

# 

# \### 1. 회원 기능

# 

# \* 회원가입

# \* 로그인

# \* 로그아웃

# \* 내 정보 조회

# \* 회원 정보 수정

# \* 권한 관리

# 

# \### 2. 인증/인가 기능

# 

# \* 로그인 인증

# \* 사용자 권한별 API 접근 제어

# \* JWT 기반 인증 방식 적용 예정

# 

# \### 3. 상품 기능

# 

# \* 상품 등록

# \* 상품 목록 조회

# \* 상품 상세 조회

# \* 상품 수정

# \* 상품 삭제

# \* 상품 재고 관리

# \* 카테고리별 상품 조회

# 

# \### 4. 장바구니 기능

# 

# \* 장바구니 상품 추가

# \* 장바구니 조회

# \* 상품 수량 변경

# \* 장바구니 상품 삭제

# 

# \### 5. 주문 기능

# 

# \* 주문 생성

# \* 주문 목록 조회

# \* 주문 상세 조회

# \* 주문 취소

# \* 주문 상태 변경

# 

# 주문 상태 예시:

# 

# ```text

# ORDER\_CREATED

# PAID

# PREPARING

# SHIPPED

# DELIVERED

# CANCELED

# ```

# 

# \### 6. 결제 기능

# 

# 초기 버전에서는 실제 결제 API 연동 대신 가짜 결제 흐름으로 구현합니다.

# 

# \* 결제 요청

# \* 결제 성공 처리

# \* 결제 실패 처리

# \* 결제 취소

# 

# 결제 상태 예시:

# 

# ```text

# READY

# SUCCESS

# FAILED

# CANCELED

# ```

# 

# \### 7. 정산 기능

# 

# 판매자별 판매 금액을 기준으로 플랫폼 수수료를 제외한 정산 금액을 계산합니다.

# 

# \* 판매자별 매출 집계

# \* 플랫폼 수수료 계산

# \* 정산 예정 금액 계산

# \* 정산 완료 처리

# \* 정산 내역 조회

# 

# 정산 예시:

# 

# ```text

# 상품 판매 금액: 100,000원

# 플랫폼 수수료: 5%

# 수수료 금액: 5,000원

# 판매자 정산 금액: 95,000원

# ```

# 

# \### 8. 리뷰 기능

# 

# \* 상품 리뷰 작성

# \* 상품 리뷰 목록 조회

# \* 리뷰 수정

# \* 리뷰 삭제

# \* 별점 등록

# 

# \### 9. 좋아요 기능

# 

# \* 상품 좋아요

# \* 상품 좋아요 취소

# \* 내가 좋아요한 상품 목록 조회

# 

# \### 10. 팔로우 기능

# 

# \* 판매자 팔로우

# \* 판매자 팔로우 취소

# \* 내가 팔로우한 판매자 목록 조회

# 

# \---

# 

# \## 주요 도메인

# 

# \### User

# 

# 회원 정보를 담당합니다.

# 

# \* id

# \* email

# \* password

# \* name

# \* role

# \* createdAt

# \* updatedAt

# 

# \### Product

# 

# 상품 정보를 담당합니다.

# 

# \* id

# \* sellerId

# \* name

# \* description

# \* price

# \* stockQuantity

# \* category

# \* status

# \* createdAt

# \* updatedAt

# 

# \### Cart

# 

# 사용자의 장바구니를 담당합니다.

# 

# \* id

# \* userId

# 

# \### CartItem

# 

# 장바구니에 담긴 상품 정보를 담당합니다.

# 

# \* id

# \* cartId

# \* productId

# \* quantity

# 

# \### Order

# 

# 주문 전체 정보를 담당합니다.

# 

# \* id

# \* userId

# \* totalPrice

# \* orderStatus

# \* createdAt

# 

# \### OrderItem

# 

# 주문에 포함된 개별 상품 정보를 담당합니다.

# 

# \* id

# \* orderId

# \* productId

# \* orderPrice

# \* quantity

# 

# \### Payment

# 

# 결제 정보를 담당합니다.

# 

# \* id

# \* orderId

# \* paymentAmount

# \* paymentStatus

# \* paidAt

# 

# \### Settlement

# 

# 판매자 정산 정보를 담당합니다.

# 

# \* id

# \* sellerId

# \* totalSalesAmount

# \* commissionAmount

# \* settlementAmount

# \* settlementStatus

# \* settledAt

# 

# \### Review

# 

# 상품 리뷰 정보를 담당합니다.

# 

# \* id

# \* userId

# \* productId

# \* rating

# \* content

# \* createdAt

# \* updatedAt

# 

# \### Like

# 

# 상품 좋아요 정보를 담당합니다.

# 

# \* id

# \* userId

# \* productId

# \* createdAt

# 

# \### Follow

# 

# 판매자 팔로우 정보를 담당합니다.

# 

# \* id

# \* followerId

# \* sellerId

# \* createdAt

# 

# \---

# 

# \## 아키텍처 초안

# 

# ```text

# Client

# &#x20; |

# &#x20; v

# Controller

# &#x20; |

# &#x20; v

# Service

# &#x20; |

# &#x20; v

# Repository

# &#x20; |

# &#x20; v

# Database

# ```

# 

# \### 계층별 역할

# 

# \* Controller: 클라이언트의 HTTP 요청을 받고 응답을 반환합니다.

# \* Service: 비즈니스 로직을 처리합니다.

# \* Repository: 데이터베이스 접근을 담당합니다.

# \* Database: 회원, 상품, 주문, 결제, 정산 등의 데이터를 저장합니다.

# 

# \---

# 

# \## 모듈 구조 초안

# 

# ```text

# auth

# user

# product

# cart

# order

# payment

# settlement

# review

# like

# follow

# ```

# 

# \---

# 

# \## API 설계 초안

# 

# \### 회원 API

# 

# ```text

# POST   /api/users/signup        회원가입

# POST   /api/users/login         로그인

# GET    /api/users/me            내 정보 조회

# PATCH  /api/users/me            내 정보 수정

# ```

# 

# \### 상품 API

# 

# ```text

# POST    /api/products           상품 등록

# GET     /api/products           상품 목록 조회

# GET     /api/products/{id}      상품 상세 조회

# PUT     /api/products/{id}      상품 수정

# DELETE  /api/products/{id}      상품 삭제

# ```

# 

# \### 장바구니 API

# 

# ```text

# POST    /api/cart/items         장바구니 상품 추가

# GET     /api/cart               장바구니 조회

# PATCH   /api/cart/items/{id}    장바구니 상품 수량 변경

# DELETE  /api/cart/items/{id}    장바구니 상품 삭제

# ```

# 

# \### 주문 API

# 

# ```text

# POST    /api/orders             주문 생성

# GET     /api/orders             주문 목록 조회

# GET     /api/orders/{id}        주문 상세 조회

# PATCH   /api/orders/{id}/cancel 주문 취소

# ```

# 

# \### 결제 API

# 

# ```text

# POST    /api/payments/request   결제 요청

# POST    /api/payments/success   결제 성공 처리

# POST    /api/payments/fail      결제 실패 처리

# POST    /api/payments/cancel    결제 취소

# ```

# 

# \### 정산 API

# 

# ```text

# GET     /api/settlements             정산 목록 조회

# GET     /api/settlements/{id}        정산 상세 조회

# POST    /api/settlements/calculate   정산 계산

# ```

# 

# \### 리뷰 API

# 

# ```text

# POST    /api/products/{productId}/reviews       리뷰 작성

# GET     /api/products/{productId}/reviews       리뷰 목록 조회

# PATCH   /api/reviews/{reviewId}                 리뷰 수정

# DELETE  /api/reviews/{reviewId}                 리뷰 삭제

# ```

# 

# \### 좋아요 API

# 

# ```text

# POST    /api/products/{productId}/likes         상품 좋아요

# DELETE  /api/products/{productId}/likes         상품 좋아요 취소

# GET     /api/users/me/likes                     내가 좋아요한 상품 조회

# ```

# 

# \### 팔로우 API

# 

# ```text

# POST    /api/sellers/{sellerId}/follow          판매자 팔로우

# DELETE  /api/sellers/{sellerId}/follow          판매자 팔로우 취소

# GET     /api/users/me/follows                   내가 팔로우한 판매자 조회

# ```

# 

# \---

# 

# \## ERD 초안

# 

# ```text

# User 1 ─ N Product

# User 1 ─ 1 Cart

# Cart 1 ─ N CartItem

# Product 1 ─ N CartItem

# 

# User 1 ─ N Order

# Order 1 ─ N OrderItem

# Product 1 ─ N OrderItem

# 

# Order 1 ─ 1 Payment

# User 1 ─ N Settlement

# 

# User 1 ─ N Review

# Product 1 ─ N Review

# 

# User 1 ─ N Like

# Product 1 ─ N Like

# 

# User 1 ─ N Follow

# User 1 ─ N Follow

# ```

# 

# \### 관계 설명

# 

# \* 한 명의 판매자는 여러 상품을 등록할 수 있습니다.

# \* 한 명의 고객은 하나의 장바구니를 가집니다.

# \* 하나의 장바구니에는 여러 상품이 담길 수 있습니다.

# \* 한 명의 고객은 여러 주문을 할 수 있습니다.

# \* 하나의 주문에는 여러 주문 상품이 포함됩니다.

# \* 하나의 주문에는 하나의 결제 정보가 연결됩니다.

# \* 한 명의 판매자는 여러 정산 내역을 가질 수 있습니다.

# \* 한 명의 사용자는 여러 리뷰를 작성할 수 있습니다.

# \* 한 명의 사용자는 여러 상품에 좋아요를 누를 수 있습니다.

# \* 한 명의 사용자는 여러 판매자를 팔로우할 수 있습니다.

# 

# \---

# 

# \## 기술 스택 예정

# 

# \* Language: Java

# \* Framework: Spring Boot

# \* Database: MySQL

# \* ORM: JPA

# \* Build Tool: Gradle

# \* Version Control: Git, GitHub

# \* API Test: Postman

# 

# \---

# 

# \## 개발 순서

# 

# \### 1단계: 설계

# 

# \* 프로젝트 주제 정리

# \* 요구사항 정리

# \* 주요 기능 목록 작성

# \* 도메인 설계

# \* API 설계

# \* ERD 초안 작성

# 

# \### 2단계: 프로젝트 생성

# 

# \* Spring Boot 프로젝트 생성

# \* GitHub 저장소 연동

# \* 기본 패키지 구조 생성

# \* README 정리

# 

# \### 3단계: 핵심 기능 구현

# 

# \* 회원 기능

# \* 로그인 기능

# \* 상품 기능

# \* 장바구니 기능

# \* 주문 기능

# 

# \### 4단계: 확장 기능 구현

# 

# \* 결제 기능

# \* 정산 기능

# \* 리뷰 기능

# \* 좋아요 기능

# \* 팔로우 기능

# 

# \### 5단계: 포트폴리오 정리

# 

# \* API 문서 정리

# \* ERD 이미지 추가

# \* 아키텍처 그림 추가

# \* 실행 방법 작성

# \* 트러블슈팅 정리

# 

# \---

# 

# \## 향후 추가할 내용

# 

# \* ERD 이미지

# \* 아키텍처 다이어그램

# \* API 명세서

# \* 예외 처리 전략

# \* 인증/인가 방식

# \* 테스트 코드

# \* 배포 방법

# \* 트러블슈팅 기록

# 

