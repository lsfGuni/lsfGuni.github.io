---
layout: post
title: "온프레미스 VM 관리 웹페이지"
subtitle: "웹 기반 VM 라이프사이클 관리 · Blue/Green 무중단 배포 · 백업 자동화"
date: 2026-04-01 00:00:00 +0900
categories: [project]
tags: [React, Spring Boot, Docker, Jenkins, Claude MCP, VirtualBox, ZFS, Infrastructure, Automation]
period: "2026.04 ~ 2026.04"
role: "설계 및 개발 전체"
contribution: "100%"
summary: "VM 복제 수작업 30분을 웹 클릭 한 번으로 단축한 풀스택 인프라 관리 시스템입니다. 7단계 자동 프로비저닝, ZFS 백업·재해복구(DR) 자동화, Jenkins 기반 Blue/Green 무중단 배포 파이프라인까지 포함합니다."
tech:
  - React 19
  - TypeScript
  - Spring Boot 3
  - Java 21
  - MariaDB
  - Docker
  - Jenkins CI/CD
  - Claude MCP
  - VirtualBox
  - ZFS
---

# 온프레미스 VM 관리 웹페이지

<img src="{{ '/assets/VM_SERVER.drawio.png' | relative_url }}"
     alt="VM 관리 시스템 아키텍처"
     width="980">

## Summary

- **기간:** 2026.04 ~ 2026.04
- **역할:** 설계 및 개발 전체
- **기여도:** 100%
- **목표:** 온프레미스 VM 환경의 반복 운영 작업(생성·복제·백업)을 웹 인터페이스로 자동화하여, 누구나 안전하게 인프라를 운영할 수 있는 관리 도구 구축

---

## Background

개발팀의 VirtualBox VM 서버를 운영하면서, VM 생성·복제·백업을 매번 SSH 접속 후 CLI 명령어로 수행하는 비효율을 경험했습니다.

특히 VM 복제 시 호스트명 변경, 고정 IP 할당, SSH 키 재생성 등 **7단계를 수작업으로 처리**해야 했고, 백업 역시 cron과 쉘 스크립트에 의존해 이력 추적과 실패 감지가 어려웠습니다.

이러한 반복 작업을 자동화하고 **웹 브라우저 하나로 전체 VM 라이프사이클을 관리**할 수 있는 시스템을 구축했습니다.

---

## What I Did

### VM 라이프사이클 관리 자동화
- VBoxManage CLI를 파싱하여 VM 생성, 시작/중지, 리소스 변경(CPU·RAM·디스크), 삭제를 웹에서 수행
- VM 복제: 소스 검증 → 클론 → 부팅 감지 → 호스트명 → 고정 IP → SSH 키 재생성 → 네트워크 검증의 **7단계 비동기 Job 설계**, 단계별 진행률 실시간 제공
- 템플릿 VM 기반 프로비저닝, VRDE 원격 데스크톱 포트 자동 할당

### 네트워크 관리
- IP 할당 전 다단계 검증: IPv4 형식 → 서브넷·게이트웨이 계산 → 예약 IP 필터링 → ARP 테이블 조회 → Ping 테스트
- Netplan YAML 자동 생성·배포로 고정 IP 설정, 사용 중인 IP 현황 대시보드 제공

### 백업·재해복구(DR) 자동화
- 전체/DB전용/일반전용/개별 VM의 4가지 백업 모드, 백업 서버 2대 비동기 실행
- ZFS 스냅샷 기반 복원, 장기 아카이브, DR 서버 동기화
- 백업 이력 DB 영속화로 실패 자동 감지 — 실패한 백업을 즉시 파악·대응

### CI/CD 파이프라인 및 무중단 배포
- Jenkins 파이프라인으로 **Blue/Green 무중단 배포** 구현, Health Check 실패 시 자동 롤백
- Docker 멀티스테이지 빌드(Node 22 → Gradle 8 → JRE 21 Alpine)로 단일 이미지 패키징, 비root 사용자 실행으로 컨테이너 보안 확보

### Claude MCP 기반 개발 워크플로우
- Claude Code CLI와 MCP(Model Context Protocol) 서버를 연동해 Redmine 이슈 기반 개발 워크플로우 구축
- 독립 평가자 에이전트와 QA 자동 사이클을 커스텀 스킬로 구현, 코드 검증·버그 수정을 자동 반복 실행

---

## Technical Highlights

- **비동기 Job 트래커**: 장시간 작업(VM 복제·삭제)의 7단계 진행률을 API로 제공, 완료 Job 자동 정리
- **관측 가능한 백업 운영**: 백업 이력을 DB에 영속화하고 상태를 자동 감지하여, 스크립트 의존 운영의 실패 사각지대 제거
- **온프레미스 최적화**: 클라우드 의존 없이 자체 인프라에서 동작하는 독립적 시스템

---

## Outcome

- VM 복제를 수작업 30분 이상에서 **웹 클릭 한 번으로 단축**, 7단계 자동 프로비저닝으로 휴먼 에러 제거
- 백업 이력 영속화·상태 자동 감지로 **실패한 백업 즉시 파악·대응** 가능
- Blue/Green 무중단 배포와 Health Check 자동 롤백으로 **서비스 중단 없는 배포 체계** 확립
- Claude MCP 기반 QA 자동화로 코드 검증·수정·재검증을 자동 반복, 개발 생산성과 코드 품질 동시 향상

---

## Tech Stack

React 19, TypeScript, Vite, Spring Boot 3, Java 21, Spring Data JPA, MariaDB, Flyway, Docker, Jenkins CI/CD, Nginx, ZFS, VirtualBox, Claude MCP, Redmine API

---

## Navigation

### [← Project 목록으로 돌아가기]({{ '/project/' | relative_url }})

### [Home]({{ '/' | relative_url }})
자기소개와 핵심 역량 요약

### [Career]({{ '/career/' | relative_url }})
경력 요약, 주요 역할, 강점, 커리어 방향

### [Work Method]({{ '/blog/' | relative_url }})
문제 해결 방식, 운영 철학, 협업과 문서화 방식
