---
layout: post
title: "온프레미스 VM 관리 시스템"
subtitle: "Claude MCP 기반 웹 브라우저 VM 제어 · 백업 자동화"
date: 2025-04-01 00:00:00 +0900
categories: [project]
tags: [Claude MCP, VM, Infrastructure, Automation, AI, Linux]
period: "2025.03 ~ 진행중"
role: "설계 및 개발 전체"
contribution: "100%"
summary: "Claude MCP(Model Context Protocol)를 활용하여 웹 브라우저에서 온프레미스 VM을 생성·조회·수정·삭제하고, 스냅샷 기반 백업을 자동화하는 인프라 관리 시스템입니다."
tech:
  - Claude MCP
  - Linux
  - VM (KVM/Proxmox)
  - Shell Script
  - Web Interface
---

# 온프레미스 VM 관리 시스템

<img src="{{ '/assets/VM_SERVER.drawio.png' | relative_url }}"
     alt="VM 관리 시스템 아키텍처"
     width="980">

## Summary

- **기간:** 2025.03 ~ 진행중
- **역할:** 설계 및 개발 전체
- **기여도:** 100%
- **목표:** 온프레미스 VM 환경을 웹 브라우저에서 직관적으로 제어하고, AI 기반 자동화로 인프라 운영 효율을 높이는 시스템 구축

---

## Background

온프레미스 환경의 VM을 관리하기 위해 매번 SSH 접속이나 하이퍼바이저 콘솔에 직접 접근해야 하는 불편함이 있었습니다.

반복적인 인프라 작업(VM 생성, OS 설치, 백업 등)을 자동화하고,
**웹 브라우저 하나로 전체 VM 라이프사이클을 관리**할 수 있는 시스템이 필요했습니다.

**Claude MCP(Model Context Protocol)**를 활용하여 AI가 인프라 작업을 자동화하는 새로운 접근 방식을 적용했습니다.

---

## What I Did

### VM OS CRUD
- 웹 인터페이스를 통한 VM 생성(Create), 조회(Read), 수정(Update), 삭제(Delete)
- VM 상태 모니터링 및 실시간 관리 대시보드

### 백업 시스템
- 스냅샷 기반 VM 백업 구현
- 백업 스케줄링 및 이력 관리
- 장애 시 복원 절차 자동화

### Claude MCP 연동
- AI 기반 인프라 작업 자동화
- 자연어 명령을 통한 VM 제어
- MCP 프로토콜을 활용한 외부 시스템 통합

---

## Technical Highlights

- **Claude MCP**: AI 모델과 외부 시스템을 연결하는 프로토콜을 활용하여, 기존 스크립트 기반 자동화를 넘어선 지능형 인프라 관리 구현
- **웹 기반 제어**: 별도 클라이언트 설치 없이 브라우저만으로 전체 VM 라이프사이클 관리
- **온프레미스 최적화**: 클라우드 의존 없이 자체 인프라에서 동작하는 독립적 시스템

---

## Outcome

- SSH/콘솔 직접 접근 없이 웹에서 VM 전체 라이프사이클 관리 가능
- AI 기반 자동화로 반복 인프라 작업 시간 단축
- 스냅샷 기반 백업으로 개발 자산 보호 체계 확립

---

## Tech Stack

Claude MCP, Linux, VM (KVM/Proxmox), Shell Script, Web Interface

---

## Navigation

### [← Project 목록으로 돌아가기]({{ '/project/' | relative_url }})

### [Home]({{ '/' | relative_url }})
자기소개와 핵심 역량 요약

### [Career]({{ '/career/' | relative_url }})
경력 요약, 주요 역할, 강점, 커리어 방향

### [Work Method]({{ '/blog/' | relative_url }})
문제 해결 방식, 운영 철학, 협업과 문서화 방식
