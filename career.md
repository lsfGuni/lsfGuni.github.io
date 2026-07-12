---
layout: page
title: Career
subtitle: Experience, Strengths, and Engineering Direction
---

# Career

안녕하세요.  
저는 **배포 자동화와 근본 원인 분석(RCA)으로 안정적인 인프라를 만드는 엔지니어** 한권희입니다.

Spring 기반 백엔드 개발자로 커리어를 시작해,  
실무에서는 **Linux 서버 구축·운영, AWS·온프레미스 하이브리드 인프라, CI/CD 파이프라인 구축·개선, 모니터링·알림 체계 구축을 통한 관측성(Observability) 확보, 보안 대응, 장애 대응 및 재발 방지, 운영 절차 문서화·표준화**까지 역할을 확장해 왔습니다.

최근에는 **폐쇄망(air-gapped) 환경의 LLM 서빙 인프라 구축**, 금융권 망분리 환경 연동 트러블슈팅 등  
**제약이 큰 환경에서 서비스를 안정적으로 동작시키는 문제**를 주로 다루고 있습니다.

문제가 발생했을 때는 단순 복구에 그치지 않고,  
**근본 원인 분석 → 해결 → 고도화 → 문서화**로 이어지는 방식으로  
재발을 방지하고 재현 가능한 운영 체계를 만드는 것을 중요하게 생각합니다.

---

## Featured Projects

### 🔒 삼성디스플레이 폐쇄망 LLM 서빙 인프라 구축 (AI POC)

**2026.05 ~ 2026.06 · 폐쇄망 인프라 담당 (인프라 1인 / 총 5인)**

인터넷이 완전히 차단된(air-gapped) 삼성디스플레이 폐쇄망 환경에서 LLM 서빙 스택(LLM 게이트웨이, Text-to-SQL 엔진, STT, 임베딩 서버 등 5개 서비스)의 오프라인 배포 파이프라인을 설계·운영하고 POC를 완수했습니다.

#### 주요 수행 내용
- 외부 빌드 서버 → 오프라인 번들링 → USB 물리 반입 → 폐쇄망 워크스테이션 배포로 이어지는 **3단계 반입 아키텍처 설계 및 운영** (총 번들 규모 1TB 이상)
- CI/CD 구성이 불가능한 환경에서 빌드·배포 파이프라인 전 과정을 직접 수행하고, 반입 이력·시행착오를 체계적으로 문서화하여 **재현 가능한 반복 배포 절차로 표준화**
- Python 기반 애플리케이션과 IBM watsonx API 연동 구성: LLM 게이트웨이(litellm) 설정, 토큰 만료(12h) 대응 체계, SSL 인증서 체인 구성 등 **연동 장애의 원인 분석과 설정 레벨 해결**
- 오프라인 환경 특화 문제 해결: Yarn Berry 기반 프런트엔드 오프라인 빌드, GPU 드라이버 사전 빌드 반입, deb/wheel 오프라인 패키지 번들링
- 프로젝트 초기 현장의 도입 반대와 제한적 협조 상황에서 **이해관계자와의 신뢰 관계를 먼저 구축**하고, 고객사 PM·기존 개발진 사이의 커뮤니케이션을 조율하여 프로젝트를 정상 궤도로 복원

#### 핵심 성과
- **POC 성공적 완료** — 전 애플리케이션 정상 동작 시연, 고객사 임원 보고에서 긍정 평가를 받아 후속 AI 프로젝트 협업으로 연결
- 반입-배포 1사이클 소요 시간 **1일 → 30분으로 단축** (이력관리 기반 절차 개선)
- 폐쇄망 5개 서비스 스택 전체를 단독으로 배포·운영

---

### 🏦 하나금융그룹(하나증권) 그룹웨어 어댑터 엔지니어링

**2026.05 ~ 진행중 (2026.07.15 오픈 확정) · 어댑터 엔지니어 (총 6인)**

하나증권 그룹웨어(SaaS) 도입 프로젝트에서 금융권 망분리·접근통제 환경의 SSO·DRM·인사연동 어댑터 배포와 연동 장애 트러블슈팅을 담당하고, 5개 이상 외부 조직 간 기술 조율을 리드했습니다.

#### 주요 수행 내용
- 금융권 망분리·접근통제 환경에서 SSO 어댑터(Spring Boot) 배포 및 연동 장애 분석
- 운영 서버 SSO 초기화 실패의 근본 원인을 **DNS 미해석 + 방화벽 미개방**으로 특정하고, 권한 제약 환경에서 `-Djdk.net.hosts.file` 기반 사전 검증 등 **비침습적 진단 기법**으로 인프라팀 조치 요청의 근거를 확보
- SaaS 개발사(PM only), 그룹웨어 인프라사(Dooray), 하나증권 인프라팀(이중화/방화벽 별도 조직), VPN사(대신네트워크), 기존 DRM사(Softcamp) 등 **다자간 이해관계자의 상이한 정보를 취합·조율하는 기술 리드** 역할 수행
- 고객사 IT 현업과 주간 정례 미팅으로 이슈·일정 직접 협의

#### 핵심 성과
- 전 테스트 통과, 잔여 이슈 없이 **오픈 일정(7/15) 확정**
- 조직 간 정보 불일치로 정체되던 인프라 이슈(DNS/방화벽/VPN 설정)를 주도적으로 해소하여 일정 지연 방지
- 금융권 보안 제약 하에서의 장애 진단·조율 프로세스 경험 확보

---

### 📡 KBS 통합재난방송시스템 STG(스테이징) 인프라 구축

**2026.04 ~ 2026.05 · 인프라 설계·구축 단독 담당 (1인)**

KBS 통합재난방송시스템 클라우드 플랫폼의 스테이징 환경을 AWS 상에 단독으로 설계·구축하고, ECS·CodeDeploy 기반 Blue/Green 무중단 배포 구성과 Jenkins 배포 파이프라인 검증까지 완료했습니다.

#### 주요 수행 내용
- 기존 운영(PRD) 인프라 분석 후 STG 환경 신규 구축: 보안그룹/네트워크, ECR, ECS 클러스터·태스크·서비스, ALB·타겟그룹·CodeDeploy(Blue/Green), CloudFront·S3(IP 접근 제한), DynamoDB, IAM 개발자 계정 권한 설계
- **아키텍처 의사결정 주도**: 계정 분리 대신 단일 계정 + 네이밍/태그 분리 방식 제안·확정 (계정 분리 시 발생하는 trust relationship 추가 작업 회피)
- **인증서 비용 회피 판단**: 기존 `*.kbs.co.kr` 와일드카드 인증서가 커버되는 `devg.kbs.co.kr` 도메인 체계를 검토·제안하여 추가 인증서 발급 없이 진행, 폐쇄망 환경의 인증서 신뢰 오류 리스크까지 사전 검토
- KBS 인프라팀과 직접 미팅·유선·메일로 도메인 발급, DNS(A/CNAME) 신청, 일정 협의 수행 — 무리한 일정에 대해 근거를 들어 재조정을 건의하고 관철

#### 핵심 성과
- 분석 10일 + 구축 4일, **실 작업 2주 내 STG 전 리소스 구축 완료**
- Jenkins 배포 테스트 정상 동작 확인으로 프로젝트 마무리
- 인수인계 최소화 상황에서 기존 운영 환경을 역분석하여 동등 환경 재현

---

## Career Summary

- **총 경력:** 2년 11개월+
- **핵심 분야:** DevOps, AI Platform Infrastructure(LLM Serving), Backend Development
- **중심 역량:** CI/CD 파이프라인 구축·개선, Air-gapped(폐쇄망) 배포, Hybrid Infrastructure, 관측성(Observability), 장애 대응·RCA, 운영 절차 문서화·표준화
- **관심 방향:** AI 플랫폼 인프라(LLM 서빙, GPU), 배포 자동화, 신뢰성 엔지니어링(SRE), 플랫폼 엔지니어링

---

## Professional Experience

### 베리드코리아
**개발팀 / 주임**  
**2024.08 ~ Present**  
**Role:** Developer · DevOps · SRE

#### 주요 업무
- AWS(Route 53, ALB, EC2)와 온프레미스를 연동하는 하이브리드 인프라 설계·구축·운영 및 운영 절차 표준화
- Docker 기반 Web / WAS / DB 컨테이너 운영 체계 구축·운영
- AWS WAF, Nginx, iptables를 활용한 다층 보안 아키텍처 구축 및 비정상 트래픽 대응
- 외부 헬스체크와 내부 지표를 결합한 모니터링·알림 체계 구축으로 관측성(Observability) 확보, Slack 실시간 알림 운영
- Jenkins 및 스크립트 기반 CI/CD 파이프라인 구축과 빌드·테스트·배포 자동화
- 장애 대응 시 로그 기반 근본 원인 분석(RCA) 및 재발 방지 대책 수립
- 해외 개발자 온보딩을 위한 서버 접근, 레포지토리, 배포 절차 문서화
- MCP, OpenSearch, S3, Lambda, EC2를 연동한 AI 실행 인프라 구축·운영
- 온프레미스 서버실 구축 및 VM 백업·재해복구(DR) 체계 운영
- **삼성SDR 파견 (2025.09 ~ 2026.03):** Spring MVC 기반 내방객 관리시스템 풀스택 개발, 카드사 연동 REST API 설계·개발, JBoss 배포 전략 수립
- 삼성디스플레이 폐쇄망 LLM 서빙 인프라 구축 — AI POC (2026.05~06)
- 하나증권 그룹웨어 어댑터 엔지니어링 — 금융권 망분리 환경 SSO/DRM/인사연동 (2026.05~)
- KBS 통합재난방송시스템 STG 인프라 단독 구축 — ECS·CodeDeploy Blue/Green (2026.04~05)

#### 핵심 성과
- 하이브리드 인프라 운영 기준 정립 및 운영 절차 문서화·표준화
- 다층 보안 방어 체계 구축으로 비정상 트래픽 선제 차단, 서비스 안정성 확보
- 모니터링·알림 자동화로 장애 인지·대응 시간 단축
- 재현 가능한 배포 파이프라인과 운영 절차 확립
- 원격·해외 협업 환경의 온보딩 시간 단축
- 삼성SDR 내방객 관리시스템 카드연동 API 자동화 및 배포 안정화

---

### 아이뱅크컨설턴츠
**개발팀 / 대리**  
**2023.09 ~ 2024.07**  
**Role:** Developer

#### 주요 업무
- React / Thymeleaf / Spring Boot 기반 풀스택 개발 및 운영 환경 정비
- GitLab과 Jenkins를 활용한 CI/CD 파이프라인 도입
- SVN에서 Git으로의 형상관리 전환 및 사내 교육 진행
- 고객 미팅, 시연 자료, 화면 정의서, 기능 정의서 작성 등 기획·기술영업 지원

#### 핵심 성과
- 개발과 운영을 함께 고려하는 실무 기반 형성
- 배포 절차 표준화와 협업 방식 개선
- 형상관리 체계 전환으로 팀 생산성 향상
- 고객 커뮤니케이션과 요구사항 정리 역량 확보

---

## Core Strengths

### Air-gapped / 폐쇄망 Deployment & AI Platform
- 폐쇄망(망분리) 환경에서 LLM 서빙 스택(게이트웨이·Text-to-SQL·STT·임베딩) 오프라인 배포·운영 경험
- 오프라인 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 사전 빌드, 물리 반입(내부망 반입 프로세스) 절차 설계
- LLM 게이트웨이(litellm)·IBM watsonx API 연동 구성, 토큰 만료·SSL 인증서 체인 등 제약 환경 특화 트러블슈팅

### CI/CD & Automation
- Jenkins, GitLab CI, Bitbucket Pipelines 기반 CI/CD 파이프라인 구축·개선 및 배포 자동화 경험
- AWS CodeDeploy 기반 Blue/Green 무중단 배포 구성 경험
- 반복 작업의 스크립트 자동화, 배포 절차 표준화, 운영 문서화로 팀 누구나 동일하게 운영 가능한 체계 구축

### Hybrid Infrastructure
- AWS와 온프레미스를 연동하는 인프라 설계·구축·운영 경험
- Route 53, ALB, EC2, ECS, Docker, Nginx, On-Premise WAS를 연결한 서비스 아키텍처 운영
- 클라우드와 내부망을 함께 고려한 실제 운영형 인프라, 비용을 고려한 아키텍처 의사결정 경험

### Observability & Reliability
- Prometheus, Grafana, Alertmanager, Blackbox Exporter, CloudWatch 기반 모니터링·로깅·알림 체계 구축
- 헬스체크, 알림, 대시보드로 관측성(Observability) 확보 및 장애 인지 시간 단축
- 대응 가능한 경보만 남기는 알림 튜닝으로 노이즈 없는 운영 방식 지향

### Security & Troubleshooting
- AWS WAF, Nginx, iptables 기반 다층 방어 아키텍처 구축 경험
- 로그 분석과 요청 흐름 추적을 통한 근본 원인 분석(RCA) 및 재발 방지 대책 수립
- 금융권 망분리·접근통제 환경에서의 비침습적 장애 진단 경험

### Collaboration
- 풀스택 개발 경험을 바탕으로 개발팀과 소통하며 인프라 요구사항을 정의·반영하는 협업 역량
- 고객사·유관부서·벤더 등 다자간 이해관계자 기술 조율 및 일정 협의 리드 경험
- 문서화, 알림 자동화, 온보딩 가이드 정비로 투명하게 상태를 공유하는 협업 방식

---

## Representative Work

### 폐쇄망 LLM 서빙 인프라 구축
인터넷이 차단된 폐쇄망에 LLM 서빙 스택 5종을 오프라인 배포하고,  
반입-배포 사이클을 1일에서 30분으로 단축하는 표준 절차를 확립했습니다.

### DDoS 대응체계 구축
AWS WAF, Nginx, iptables를 결합한 3계층 방어 아키텍처를 구축하여  
비정상 트래픽을 선제 차단하고 핵심 API의 안정성을 확보했습니다.

### 모니터링 · 알림 체계 구축
Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반  
외부 헬스체크 결합 모니터링과 Slack 실시간 알림으로 관측성을 확보했습니다.

### 글로벌 개발 인프라 구축
AWS와 온프레미스를 연결한 하이브리드 개발 인프라를 구축하고,  
Jenkins 기반 CI/CD 파이프라인과 Slack 연동 협업 환경을 정비했습니다.

### VM 서버 백업 시스템 구축
ZFS 스냅샷, 증분 백업, UPS 연동 자동 종료 체계를 설계하여  
개발 자산 보호와 재해복구(DR) 대응 역량을 높였습니다.

### AI 실행 인프라 구축
MCP, OpenSearch, S3, Lambda, EC2를 연결해  
질의응답 실행과 데이터 인덱싱·검색이 가능한 재현형 AI 실행 인프라를 구축했습니다.

---

## Technical Environment

### Cloud / Infra
AWS, Route 53, ALB, EC2, ECS, ECR, CodeDeploy(Blue/Green), CloudFront, Lambda, VPC, WAF, CloudWatch, OpenSearch, S3, DynamoDB, IAM

### AI / LLM Infrastructure
litellm(LLM Gateway), IBM watsonx, MCP, 오프라인 모델·패키지 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 반입

### Server / Network
Linux, Ubuntu, Docker, Apache HTTP Server, Apache Tomcat, Nginx, iptables, WireGuard

### CI/CD / DevOps
Jenkins, GitLab CI, Bitbucket Pipelines, Docker Compose, Git

### Monitoring / Observability
Prometheus, Grafana, Alertmanager, Blackbox Exporter, CloudWatch

### Backend / Development
Java, JavaScript, Spring

### Data Stores
Oracle, MySQL, MariaDB, Redis

---

## Work Style

- 문제를 단편적으로 보지 않고 **서비스 흐름 전체**를 따라가며 원인을 좁혀갑니다.
- 장애 대응 시 **임시 복구보다 재발 방지**를 더 중요하게 생각합니다.
- 반복 작업은 자동화하고, 운영 절차는 문서화하여 **재현 가능한 운영 환경**을 만듭니다.
- 개발, 운영, 네트워크를 분리하지 않고 **하나의 시스템**으로 이해하려고 합니다.
- 팀 내 역할을 존중하면서도, 필요한 경우 직접 구조를 정리하고 실행하는 편입니다.

---

## Career Direction

앞으로는 단순히 서버를 운영하는 엔지니어가 아니라,  
**AI 플랫폼 인프라(LLM 서빙·GPU), 하이브리드 인프라, 배포 자동화, 관측성, 신뢰성 개선**을 함께 다룰 수 있는 엔지니어로 성장하고자 합니다.

특히 아래 영역을 지속적으로 강화하고 있습니다.

- AI Platform / LLM Serving Infrastructure
- CI/CD and Deployment Automation
- Hybrid & Air-gapped Infrastructure Architecture
- Observability and Incident Response
- Security Hardening & Compliance
- DevOps / SRE / Platform Engineering
- Documentation and Operational Standardization

---

## Navigation

### [Home](/)
자기소개와 핵심 역량 요약

### [Project](/project)
대표 프로젝트, 아키텍처, 수행 내용, 성과

### [Work Method](/blog)
문제 해결 방식, 운영 철학, 협업과 문서화 방식
