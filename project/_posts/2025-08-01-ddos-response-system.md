---
layout: post
title: "DDoS 대응체계 구축"
subtitle: "AWS WAF · Nginx · iptables 기반 3계층 방어"
date: 2025-08-01 00:00:00 +0900
categories: [project]
tags: [AWS, WAF, Nginx, iptables, SRE, Security]
period: "2025.08"
role: "SRE"
contribution: "100%"
summary: "AWS WAF, Nginx, iptables를 결합한 3계층 방어 체계를 구축하여 비정상 트래픽을 차단하고 핵심 API의 안정성을 높인 프로젝트입니다."
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

<img src="{{ '/assests/ddos_arc.drawio.png' | relative_url }}"
     alt="Cloud-Web-WAS 3계층 방어 아키텍처"
     width="980">

## Summary

- **기간:** 2025.08
- **역할:** SRE
- **기여도:** 100%
- **목표:** 로그인 관련 핵심 API를 대상으로 한 비정상 HTTP 요청에 대응할 수 있는 지속 가능한 방어 체계 구축

---

## Background

분산된 L7 공격으로 인해 비정상 요청이 급격히 증가했고,  
그 결과 WAS CPU 사용률 상승, 로그 급증, 로그인 지연, 클라우드 트래픽 비용 증가 문제가 발생했습니다.

단일 지점 차단만으로는 대응이 어려워  
Cloud, Web, WAS를 포함한 다층 방어 체계가 필요했습니다.

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
- Tomcat Access Log 분석
- **iptables 기반 자동 차단 스크립트** 작성 및 운영
- 단일 IP 차단 방식에서 분산 공격 대응 방식으로 확장

### Operations
- 의미 있는 차단 로그만 남기도록 로그 운영 방식 정리
- 대응 가이드, 차단 템플릿, 재사용 가능한 스크립트 문서화

---

## Outcome

- 비정상 트래픽이 WAS 자원을 소모하기 전에 선제적으로 차단
- 핵심 API를 큰 장애 없이 안정화
- 봇/스캐너 요청으로 인한 불필요한 클라우드 트래픽 비용 감소
- Cloud, Web, WAS를 아우르는 재사용 가능한 방어 패턴 확보

---

## Tech Stack

AWS WAF, ALB, CloudWatch, EC2, Nginx, Tomcat, iptables, Shell Script

---

## Navigation

### [← Project 목록으로 돌아가기]({{ '/project/' | relative_url }})

### [Home]({{ '/' | relative_url }})
자기소개와 핵심 역량 요약

### [Career]({{ '/carreer/' | relative_url }})
경력 요약, 주요 역할, 강점, 커리어 방향

### [Work Method]({{ '/blog/' | relative_url }})
문제 해결 방식, 운영 철학, 협업과 문서화 방식
