# lottogen-web
로또번호 생성 App

## 목차
- [개요](#개요)
- [기능](#기능)
- [기술 스택](#기술-스택)
- [아키텍처](#아키텍처)
- [빠른 시작](#빠른-시작)
- [환경 변수](#환경-변수)
- [실행/빌드](#실행빌드)
- [배포](#배포)
- [API 문서](#api-문서)
- [트러블슈팅](#트러블슈팅)
- [기여](#기여)
- [라이선스](#라이선스)

## 개요
- 목적: 회사 자산(IT장비)을 효과적으로 관리하기 위한 WEB 기반 APP 
- 대상 사용자: 자산관리자
- 범위/제약: 

## 기능
- [ ] IT자산 관리(등록/수정/삭제)

## 기술 스택
- Backend: Java 17, Spring Boot 3.x, Spring Security, JPA
- Frontend: Next.js
- DB: PostgreSQL
- Infra: Nginx, Docker, k3s, Jenkins
- Observability: (예: Prometheus, Grafana, Loki)

## 아키텍처
```text
Client
  │
  ├─ Host Nginx (TLS termination, rate limit, routing)
  │
  └─ k3s Ingress (Traefik/nginx-ingress)
        │
        └─ Service → Pod (App)
