---
layout: page
title: 한권희 — DevOps Engineer
subtitle: 이력서 (Resume) · CJ ENM DevOps Engineer 지원
---

<style>
  .rsm { font-size: 0.92rem; line-height: 1.62; }
  .rsm h2 { font-size: 1.02rem; font-weight: 700; color: #0069d9; border-bottom: 2px solid #008AFF;
            padding-bottom: 4px; margin: 1.5rem 0 0.7rem 0; }
  .rsm h3 { font-size: 0.95rem; margin: 0.9rem 0 0.15rem 0; }
  .rsm h3 .meta { font-weight: 400; color: #666; font-size: 0.85rem; }
  .rsm ul { margin: 0.25rem 0 0.6rem 0; padding-left: 17px; }
  .rsm li { margin-bottom: 0.2rem; }
  .rsm .head { border-bottom: 1px solid #dee2e6; padding-bottom: 10px; margin-bottom: 4px; }
  .rsm .head .name { font-size: 1.5rem; font-weight: 700; margin: 0; }
  .rsm .head .role { color: #0069d9; font-weight: 600; margin: 2px 0 6px 0; }
  .rsm .head .contact { font-size: 0.86rem; color: #444; }
  .rsm .stack { font-size: 0.88rem; }
  .rsm .stack b { color: #333; }
  @media print {
    .intro-header, nav, footer, .navbar { display: none !important; }
    body { font-size: 9.6pt; line-height: 1.45; }
    .rsm { font-size: 9.6pt; line-height: 1.45; }
    .rsm h2 { font-size: 11pt; margin: 11pt 0 5pt 0; }
    .rsm h3 { font-size: 10pt; }
    a { color: #333 !important; text-decoration: none !important; }
    h2, h3, ul { break-inside: avoid; }
    /* Bootstrap 그리드 리셋 — .row 음수 마진이 인쇄 시 좌측을 잘라내므로 함께 0으로 */
    .container-md, .container, .row, .col-xl-10, .col-lg-10, [class*="col-"] {
      max-width: 100% !important; width: 100% !important; flex: 0 0 100% !important;
      margin-left: 0 !important; margin-right: 0 !important;
      padding-left: 0 !important; padding-right: 0 !important;
    }
    html, body { width: auto !important; overflow: visible !important; }
    @page { margin: 12mm; }
  }
</style>

<div class="rsm" markdown="1">

<div class="head">
  <p class="name">한권희 <span style="font-size:1rem; font-weight:400; color:#666;">Gwonhee Han</span></p>
  <p class="role">DevOps Engineer · SRE</p>
  <p class="contact">
    lsfguni@gmail.com · 서울<br>
    포트폴리오 <a href="https://lsfguni.github.io/">lsfguni.github.io</a> ·
    경력기술서 <a href="https://lsfguni.github.io/career/">lsfguni.github.io/career</a> ·
    GitHub <a href="https://github.com/lsfGuni">github.com/lsfGuni</a>
  </p>
</div>

## 요약

Spring 백엔드 개발로 시작해 **AWS 컨테이너 기반 서비스 운영, CI/CD, 관측성, 백업·복구**로 역할을 확장한 3년차 DevOps 엔지니어입니다.
대국민 서비스(KBS 통합재난방송시스템)의 스테이징 인프라를 **ECS Fargate + CodeDeploy Blue/Green** 기반으로 단독 구축·검증했고,
현재 자사 블록체인 서비스의 AWS·온프레미스 하이브리드 인프라를 단독으로 운영하며 모니터링·백업·DR 체계까지 직접 책임지고 있습니다.
장애는 복구에서 멈추지 않고 근본 원인까지 내려가 문서로 남기며, 반복 작업은 스크립트와 IaC로 자동화합니다.

## 핵심 역량

- **AWS 컨테이너 기반 애플리케이션 운영** — ECS Fargate 태스크 정의·ALB 이중 리스너·ECR 연동 구성, Docker 기반 Web/WAS/DB 운영, Kubernetes(k3s) 클러스터 직접 구축 *(self-managed 기준, 관리형 EKS 경험 없음)*
- **CI/CD 파이프라인 구축·유지보수** — Jenkins·GitLab CI·Bitbucket Pipelines 파이프라인 구축, CodeDeploy Blue/Green 무중단 배포, ArgoCD app-of-apps GitOps
- **클라우드 인프라 운영 · 모니터링 · 백업·복구** — Prometheus·Grafana·Alertmanager·Blackbox 기반 모니터링 체계 구축, VM 백업·재해복구(DR) 체계 운영, 롤백 경로를 먼저 확보하는 이관 설계
- **인프라 자동화** — Terraform(VM 프로비저닝) + Ansible(설치·설정)로 클러스터 전체 재현, 공격 IP 자동 차단 등 운영 자동화 스크립트 개발·유지보수

## 경력

### 베리드코리아 <span class="meta">| DevOps · SRE · 인프라 단독 운영 | 2025.02 ~ 현재</span>

자사 블록체인 서비스(BaaS·지갑·익스플로러)의 AWS + 온프레미스 하이브리드 인프라를 단독으로 운영.

- **KBS 통합재난방송시스템 STG 인프라 단독 구축** — ECS Fargate + CodeDeploy Blue/Green 무중단 배포, ALB 이중 리스너·타겟그룹 2조·ECR 연동, Jenkins 배포 파이프라인 검증까지 완료. **PRD-STG 전 항목 CLI 대조 검증, 불일치 0건**
- 인수인계 없이 맡은 운영 환경에 모니터링·알림 체계를 구축하고 장애별 RCA를 문서화해 **트러블슈팅 소요 시간을 1주일에서 30분 이내로 단축**
- 봇·무차별 대입 트래픽에 WAF·Nginx·iptables **3계층 방어를 자동화 스크립트로 고도화** — 일 50GB 공격 로그에서 **하루 평균 1,000개 이상 IP 자동 차단, AWS 비용 20% 이상 절감**
- 대규모 트랜잭션 시 반복되던 메인넷 노드 다운을 **디스크 I/O 병목 + 체인 데이터 용량 부족**으로 특정, 장비 증설 없이 요청 분산 구조로 전환해 재발 방지
- **AWS 비용 절감을 위한 온프레미스 이관(FinOps) 진행 중** — 이관 순번을 리스크 기준으로 설계하고 롤백 경로를 먼저 확보한 뒤 전환. BaaS API 2노드 이중화 후 실트래픽 전환 완료 (**실적 약 20% 절감, 1단계 목표 56~70%**)
- **Kubernetes(k3s) 격리 실행 인프라 구축 중** — 에이전트 실행 1건 = Job 1개, 전용 네임스페이스·ServiceAccount·RBAC, ArgoCD app-of-apps로 Helm 차트 14종 선언적 배포 *(서비스 오픈 전 단계)*
- Jenkins·스크립트 기반 CI/CD 구축, Docker 기반 Web/WAS/DB 운영, 온프레미스 서버실 구축 및 **VM 백업·재해복구(DR) 체계 운영**

### 아이비즈소프트웨어 <span class="meta">| Backend Developer · DevOps (프로젝트 계약) | 2024.08 ~ 2025.01</span>

베리드코리아 관계사(동일 사업장)에서 NIPA 블록체인 정부과제 수행 후 2025.02 베리드코리아 정규 입사.

- NIPA 블록체인 정부과제 — **의약품 이력관리 시스템** 백엔드·인프라 1인 담당
- Spring Boot 기반 REST API 설계·개발 — Flutter 모바일 앱(iOS 개발자 협업) 연동
- 관리자 페이지(Thymeleaf) 개발, MariaDB 데이터 모델링, 블록체인 연계 이력 기록·조회 기능 개발
- AWS EC2 서버 구축·운영 및 배포 자동화 — 개발과 인프라 겸임

### 아이뱅크컨설턴츠 <span class="meta">| Developer | 2023.09 ~ 2024.07</span>

- React / Thymeleaf / Spring Boot 기반 풀스택 개발 및 운영 환경 정비
- **팀 최초의 CI/CD 파이프라인 도입** (GitLab + Jenkins) — 수작업 빌드·배포 제거
- **SVN → Git 형상관리 전환 주도** 및 브랜치 전략 수립, 사내 교육 진행

## 주요 프로젝트

- **KBS 통합재난방송시스템 STG 인프라 구축** (2026.04~06, 단독) — 검증 환경이 없던 대국민 서비스에 AWS CLI로 운영 리소스를 전수 조회해 ECS 태스크 정의·ALB·CloudFront·DynamoDB 구성을 복원하고, 운영과 동등한 스테이징을 신규 구축. **ECS Fargate + CodeDeploy Blue/Green, CloudFront 7경로 분기, IAM 최소권한**
- **홈랩 프라이빗 클라우드 & IaC 전환** (개인, 진행 중) — 물리 서버 3대에 Proxmox 구축, **Terraform + Ansible로 k8s 멀티노드 클러스터 전체를 명령 두 번으로 재현**. ZFS 스냅샷·증분 백업·UPS 연동 자동 종료로 DR 체계 확보
- **삼성디스플레이 폐쇄망 AI 플랫폼 구축** (2026.05~06, 인프라 단독) — 인터넷 차단 환경에 AI 서비스 5종 배포. ARM↔x86_64 멀티 아키텍처 빌드 등 반입 실패 요인을 제거해 **1사이클 5시간+ → 30분(약 90% 단축)**
- **하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터** (2026.05~07) — 업체가 각기 다른 금융권 망분리 다단계 연동에서 구간별 통신 검증으로 원인 구간 특정. **잔여 이슈 없이 7/15 정상 오픈**

## 기술 스택

<div class="stack" markdown="1">
**Cloud** AWS (ECS Fargate, ECR, CodeDeploy, EC2, ALB, CloudFront, CloudFront Functions, Route 53, ACM, S3, DynamoDB, Lambda, VPC, WAF, CloudWatch, OpenSearch, IAM)
**Container · Orchestration** Docker, Kubernetes(k3s), Helm, ArgoCD, Linkerd, NetworkPolicy·RBAC, Harbor
**IaC · CI/CD · 자동화** Terraform, Ansible, Proxmox, Jenkins, GitLab CI, Bitbucket Pipelines, CodeDeploy
**관측성** Prometheus, Grafana, Alertmanager, Blackbox Exporter, OpenTelemetry, Tempo
**Server · Network** Linux, Nginx, Apache, Tomcat, iptables, WireGuard
**Backend · Data** Java, Spring, JavaScript / Oracle, MySQL, MariaDB, Redis
</div>

## 학력

**중앙대학교** 경제학 학사

</div>
