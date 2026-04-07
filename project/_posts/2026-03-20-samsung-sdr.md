---
layout: post
title: "삼성SDR 내방객 관리시스템"
subtitle: "Spring MVC 기반 풀스택 개발 · 카드연동 API · JBoss 배포"
date: 2026-03-20 00:00:00 +0900
categories: [project]
tags: [Java, Spring MVC, JBoss, REST API, Full-Stack]
period: "2025.09 ~ 2026.03"
role: "Full-Stack Developer · 배포 담당"
contribution: "핵심 개발 및 배포 전담"
summary: "삼성SDR에 파견되어 내방객 관리시스템을 Spring MVC 기반으로 풀스택 개발하고, 카드사 연동 API 구현 및 JBoss 서버 배포 전략을 수립한 프로젝트입니다."
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

---

## What I Did

### Backend 개발
- **Spring MVC 패턴** 기반 서버 아키텍처 설계 및 구현
- **카드연동 API** 설계 및 개발
  - 외부 카드사 시스템과의 연동 인터페이스 구현
  - 카드 발급/회수 상태 동기화 처리
  - API 요청/응답 처리 및 에러 핸들링
- 내방객 등록, 조회, 승인, 이력 관리 등 핵심 비즈니스 로직 개발

### Frontend 개발
- JSP 기반 사용자 화면 개발
- JavaScript를 활용한 동적 UI 처리 및 유효성 검증

### 배포 및 서버 운영
- **JBoss 웹서버** 설정 및 환경 구성
- **배포 전략 수립** 및 실행
  - 배포 프로세스 정립 및 절차 문서화
  - 서버 안정성 확보를 위한 배포 절차 관리
- 운영 환경 트러블슈팅 및 안정화

---

## Outcome

- 카드사 연동 API를 통한 내방객 출입 관리 자동화 실현
- 안정적인 배포 전략 수립으로 서비스 운영 안정화
- Spring MVC 패턴을 활용한 유지보수성 높은 코드 구조 확립
- 수기 관리 대비 내방객 처리 효율 향상

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
