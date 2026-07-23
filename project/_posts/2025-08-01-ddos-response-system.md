---
layout: post
title: "DDoS 대응체계 구축"
subtitle: "AWS WAF · Nginx · iptables 기반 3계층 방어 아키텍처"
date: 2025-08-01 00:00:00 +0900
categories: [project]
tags: [AWS, WAF, Nginx, iptables, SRE, Security]
period: "2025.08"
role: "SRE"
contribution: "100%"
summary: "AWS WAF, Nginx, iptables를 결합한 3계층 방어 아키텍처를 구축하여 비정상 트래픽을 하루 평균 1,000개 이상 IP 규모로 자동 차단하고, 2일 1회 서버 중단을 장애 제로화하며 AWS 비용을 20% 이상 절감한 프로젝트입니다."
tech:
  - AWS WAF
  - ALB
  - CloudWatch
  - EC2
  - Nginx
  - Tomcat
  - iptables
  - Shell Script
---

# DDoS 대응체계 구축

<img src="{{ '/assets/ddos_arc.drawio.png' | relative_url }}"
     alt="Cloud-Web-WAS 3계층 방어 아키텍처"
     width="980">

## Summary

- **기간:** 2025.08
- **역할:** SRE
- **기여도:** 100%
- **목표:** 로그인 관련 핵심 API를 대상으로 한 비정상 HTTP 요청을 선제 차단하고, 재발 방지까지 가능한 지속 가능한 방어 체계 구축

---

## Background

분산된 L7 공격으로 봇/스캐너 트래픽이 폭증하여 **WAS CPU 사용률이 140%까지 치솟고, 로그가 하루 100GB 이상** 쌓이며 **2일에 1회꼴로 서버가 중단**되는 상황이었습니다.

단일 지점 차단은 임시 조치에 그쳐 공격 패턴이 바뀔 때마다 장애가 재발했고,  
트래픽이 지나는 경로 전체를 따라 Cloud, Web, WAS를 아우르는 다층 방어 아키텍처가 필요했습니다.

---

## What I Did

### Cloud Layer
- **AWS WAF** 구성 및 **ALB** 연동
- AWS Managed Rule 적용
- 로그인 관련 특정 엔드포인트에 대해 Rate-based Custom Rule 추가
- WAF 로그를 CloudWatch와 연결하여 운영 가시성 확보

### Web Layer
- **User-Agent 필터링** 적용
- **Rate Limiting** 설정
- 공격 대상 엔드포인트를 Nginx 레벨에서 직접 제어

### WAS Layer
- Tomcat Access Log 분석으로 공격 패턴의 근본 원인 분석(RCA)
- **iptables 기반 자동 차단 스크립트** 작성 및 운영으로 반복 대응 자동화
- 단일 IP 차단 방식에서 분산 공격 대응 방식으로 확장

### Operations
- 의미 있는 차단 로그만 남기도록 로그 운영 방식 정리 (관측성 확보)
- 대응 가이드, 차단 템플릿, 재사용 가능한 스크립트로 대응 절차 문서화·표준화

---

## Outcome

- 2일 1회 서버 중단 → 방어 체계 구축 후 **장애 제로화**, WAS CPU 140% → 정상 범위로 안정화
- 단일 IP 차단에서 다수 IP 로테이션 공격 대응으로 고도화 — **하루 평균 1,000개 이상의 공격 IP 자동 차단**
- 비정상 트래픽을 Cloud 레벨에서 선제 차단하여 WAS 자원 소모 방지, 핵심 API 서비스 안정성 확보
- 봇/스캐너 요청 차단으로 **AWS 비용 20% 이상 절감** (비용 최적화)
- Cloud, Web, WAS를 아우르는 재사용 가능한 방어 패턴과 표준 대응 절차 확보

---

## Tech Stack

AWS WAF, ALB, CloudWatch, EC2, Nginx, Tomcat, iptables, Shell Script

---

## Navigation

### [← Project 목록으로 돌아가기]({{ '/project/' | relative_url }})

### [Home]({{ '/' | relative_url }})
자기소개와 핵심 역량 요약

### [Career]({{ '/career/' | relative_url }})
경력 요약, 주요 역할, 강점, 커리어 방향

### [Work Method]({{ '/blog/' | relative_url }})
문제 해결 방식, 운영 철학, 협업과 문서화 방식
