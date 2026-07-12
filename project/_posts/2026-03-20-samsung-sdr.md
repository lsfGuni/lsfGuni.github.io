---
layout: post
title: "삼성SDR 내방객 관리시스템"
subtitle: "Spring MVC 기반 풀스택 개발 · 카드사 연동 REST API 설계·개발 · JBoss 배포"
date: 2026-03-20 00:00:00 +0900
categories: [project]
tags: [Java, Spring MVC, JBoss, REST API, Full-Stack]
period: "2025.09 ~ 2026.03"
role: "Full-Stack Developer · 배포 담당"
contribution: "핵심 개발 및 배포 전담"
summary: "삼성SDR에 파견되어 내방객 관리시스템을 Spring MVC 기반으로 풀스택 개발하고, 카드사 연동 REST API 설계·개발과 JBoss 배포 전략 수립·운영 안정화까지 담당한 프로젝트입니다."
tech:
  - Java
  - Spring MVC
  - JSP
  - JavaScript
  - JBoss
  - REST API
---

# 삼성SDR 내방객 관리시스템

## Summary

- **기간:** 2025.09 ~ 2026.03
- **역할:** Full-Stack Developer · 배포 담당
- **기여도:** 핵심 개발 및 배포 전담
- **목표:** 삼성SDR 사업장의 내방객 출입 관리 프로세스를 시스템화하고, 카드 발급/회수 연동을 통해 보안 관리를 자동화

---

## Background

삼성SDR 사업장에서 내방객의 출입을 수기/반자동으로 관리하던 기존 방식을 개선하기 위해,
내방객 등록부터 카드 발급, 출입 이력 관리까지 통합된 웹 기반 관리시스템이 필요했습니다.

요구사항 분석부터 설계·개발·배포·운영까지 전 과정을 수행하며,
레거시 환경(JSP + MyBatis)에서 발생하는 실제 운영 이슈를 해결하고 시스템 안정성을 높였습니다.

---

## What I Did

### Backend 개발
- **Spring MVC 패턴** 기반 서버 아키텍처 설계 및 구현
- **카드사 연동 REST API 설계·개발**
  - 외부 카드사 시스템과의 연동 인터페이스 구현
  - 카드 발급/회수 상태 실시간 동기화로 데이터 정합성 확보
  - API 요청/응답 처리 및 에러 핸들링, 연동 장애 대응
- 요구사항 분석을 통한 내방객 등록, 조회, 승인, 이력 관리 등 핵심 비즈니스 로직 설계·개발

### Frontend 개발
- JSP 기반 사용자 화면 개발
- JavaScript를 활용한 동적 UI 처리 및 입력값 유효성 검증 로직 구현

### 배포 및 서버 운영
- **JBoss WAS** 환경 설정 및 구성
- **배포 전략 수립** 및 실행
  - 배포 프로세스 정립 및 배포 절차 문서화·표준화
  - 서버 안정성 확보를 위한 배포 절차 관리
- 운영 환경 트러블슈팅 및 장애 원인 분석·안정화
- 운영/인수인계 문서 작성 및 해외 개발자 협업 지원

---

## Outcome

- 카드사 연동 REST API 기반 카드 발급/회수 자동화로 수기 관리 대비 내방객 처리 효율 향상
- UI–DB 간 데이터 흐름 정합성을 확보하여 유지보수성 향상
- 배포 절차 문서화·표준화로 레거시 환경(JSP + MyBatis)에서 안정적인 운영 구조 확립
- 운영/인수인계 문서화로 해외 개발자 협업·온보딩 지원

---

## Tech Stack

Java, Spring MVC, JSP, JavaScript, JBoss, REST API

---

## Navigation

### [← Project 목록으로 돌아가기]({{ '/project/' | relative_url }})

### [Home]({{ '/' | relative_url }})
자기소개와 핵심 역량 요약

### [Career]({{ '/career/' | relative_url }})
경력 요약, 주요 역할, 강점, 커리어 방향

### [Work Method]({{ '/blog/' | relative_url }})
문제 해결 방식, 운영 철학, 협업과 문서화 방식
