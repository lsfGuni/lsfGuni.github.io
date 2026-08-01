---
layout: page
title: 한권희 — Software Engineer
subtitle: 이력서 (Resume) · Blue Garage Full Stack
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
  <p class="role">Software Engineer · Full Stack &amp; AI Platform</p>
  <p class="contact">
    lsfguni@gmail.com · 서울<br>
    포트폴리오 <a href="https://lsfguni.github.io/">lsfguni.github.io</a> ·
    경력기술서 <a href="https://lsfguni.github.io/career/">lsfguni.github.io/career</a> ·
    GitHub <a href="https://github.com/lsfGuni">github.com/lsfGuni</a>
  </p>
</div>

## 요약

React·Spring 풀스택 개발로 시작해 **AI 서비스 구축·LLM 연동, 배포, 운영·모니터링까지 서비스 전 과정**을 다뤄 온 3년차 엔지니어입니다.
최근 1년은 **AI 서비스를 실제로 동작시키는 문제**를 주로 풀었습니다 — 폐쇄망 환경에 LLM 게이트웨이·STT 등 AI 서비스 5종을 단독 배포했고, AI 에이전트 실행 플랫폼의 실행 인프라를 구축하고 있습니다.
개발만 하고 넘기는 것이 아니라 **기획 → 구축 → 배포 → 운영·모니터링 전 과정에 참여**해 서비스가 안정적으로 살아있게 만드는 것을 강점으로 합니다.

## 핵심 역량

- **풀스택 개발 · REST API 설계** — React·Spring Boot 풀스택 개발, 외부 기관(카드사) 연동 REST API 설계·개발, RDB 데이터 모델링 (Oracle·MySQL·PostgreSQL)
- **AI 모델 연동 · 추론 파이프라인** — litellm(LLM Gateway)을 단일 창구로 둔 멀티 서비스 LLM 연동 설계, IBM watsonx API 연동 챗봇 구축, GPU 제약 환경에서 STT 모델 로컬 서빙, AI 에이전트 격리 실행 인프라(Kubernetes) 구축
- **배포 · DevOps** — Docker, AWS(ECS Fargate·CodeDeploy Blue/Green·CloudFront·ALB), Jenkins·GitLab CI 파이프라인, 검증 이미지를 그대로 승격하는 Build Once-Promote 배포 체계 설계
- **서비스 품질 · 성능 모니터링** — Prometheus·Grafana·Alertmanager 모니터링·알림 체계 구축, 장애별 RCA 문서화로 트러블슈팅 소요 1주일 → 30분 이내 단축

## 경력

### 베리드코리아 <span class="meta">| Software Engineer · DevOps | 2025.02 ~ 현재</span>

AI 플랫폼 구축 프로젝트와 자사 블록체인 서비스(B2B BaaS · B2C 지갑·익스플로러)의 개발·운영을 담당.

- **폐쇄망 AI 플랫폼 구축 (삼성디스플레이 POC)** — LLM 게이트웨이(litellm)·Text-to-SQL·보안검토 에이전트·STT 등 AI 서비스 5종을 단독 배포·기동. watsonx API 연동 챗봇의 연동·배포 담당. 반입-배포 1사이클 5시간+ → 30분(약 90% 단축), 후속 단계 확정
- **AI 에이전트 실행 플랫폼 구축 중** — AI가 생성한 코드를 안전하게 실행하는 격리 인프라. 실행 1건 = Kubernetes Job 1개, 전용 네임스페이스·RBAC, ArgoCD GitOps로 Helm 차트 14종 선언적 배포
- **내방객 관리시스템 풀스택 개발 (삼성SDR 파견, 2025.09~2026.03)** — Spring MVC 기반 화면·백엔드 개발, 카드사 연동 REST API 설계·개발, Oracle 데이터 모델링, JBoss 배포 전략 수립
- **B2C 지갑·익스플로러 서비스 운영** — 계정 탈취를 노리는 무차별 대입·봇 트래픽에 WAF·Nginx·iptables 3계층 방어 구축, 하루 평균 1,000개 이상 IP 자동 차단·AWS 비용 20% 이상 절감. 모니터링·RCA 체계 구축으로 트러블슈팅 1주일 → 30분
- **KBS 통합재난방송시스템 STG 인프라 구축** — 대국민 서비스에 운영과 동등한 스테이징 신규 구축, ECS Fargate + CodeDeploy Blue/Green 무중단 배포, PRD-STG 전 항목 대조 검증 불일치 0건
- 사내 문서관리 시스템 CI/CD 구축 — 스테이징 검증 이미지를 재빌드 없이 운영으로 승격(Build Once-Promote), 배포 직전 DB 자동 백업, 프론트 typecheck·lint·test 자동화

### 아이비즈소프트웨어 <span class="meta">| Backend Developer · DevOps (프로젝트 계약) | 2024.08 ~ 2025.01</span>

베리드코리아 관계사(동일 사업장)에서 NIPA 블록체인 정부과제 수행 후 2025.02 베리드코리아 정규 입사.

- NIPA 블록체인 정부과제 — **의약품 이력관리 시스템** 백엔드·인프라 1인 담당
- **Spring Boot 기반 REST API 설계·개발 — Flutter 모바일 앱(iOS 개발자 협업) 연동** · 모바일 클라이언트와 협업하는 백엔드 경험
- 관리자 페이지(Thymeleaf) 개발, MariaDB 데이터 모델링, 블록체인 연계 이력 기록·조회 기능 개발
- AWS EC2 서버 구축·운영 및 배포 자동화 — 개발과 인프라 겸임

### 아이뱅크컨설턴츠 <span class="meta">| Full Stack Developer | 2023.09 ~ 2024.07</span>

- **React / Thymeleaf / Spring Boot 기반 웹 서비스 풀스택 개발** — 화면 설계부터 API·DB까지 담당
- 팀 최초의 CI/CD 파이프라인 도입 (GitLab + Jenkins) — 수작업 빌드·배포 제거
- SVN → Git 형상관리 전환 주도, 브랜치 전략 수립 및 사내 교육
- 고객 미팅·시연·화면 정의서·기능 정의서 작성 — 기획 단계부터 참여

## 주요 프로젝트

- **삼성디스플레이 폐쇄망 AI 플랫폼 구축** (2026.05~06, 단독) — 인터넷 차단 환경에서 LLM 추론은 watsonx API로 위임하고 16GB GPU는 STT 서빙 전용으로 배분하는 워크로드 설계. litellm을 모델 호출 단일 창구로 두어 서비스 5종의 연동 코드를 분리. watsonx 연동 챗봇 배포 담당
- **AI 에이전트 실행 플랫폼** (2026.05~, 사내) — 신뢰할 수 없는 AI 생성 코드의 격리 실행 환경. MCP·OpenSearch·S3·Lambda 연동 AI 실행 인프라 구축·운영
- **하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터** (2026.05~07) — Spring Boot 어댑터 구축, 금융권 망분리 다단계 연동 장애를 구간별 통신 검증으로 특정. 잔여 이슈 없이 정상 오픈
- **내방객 관리시스템** (2025.09~2026.03, 삼성SDR) — 카드사 연동 REST API 설계·개발, Spring MVC·Oracle 풀스택
- **홈랩 프라이빗 클라우드** (개인, 진행 중) — 물리 서버 3대에 Proxmox·Kubernetes 구축, Terraform + Ansible로 전체 재현

## 기술 스택

<div class="stack" markdown="1">
**Frontend** React, JavaScript, Thymeleaf
**Backend** Java, Spring Boot·Spring MVC, REST API 설계, JPA/MyBatis
**Database** Oracle, MySQL, MariaDB, PostgreSQL(Flyway), Redis, OpenSearch, DynamoDB
**AI** litellm(LLM Gateway), IBM watsonx API, STT 모델 서빙, MCP, 오프라인 모델·패키지 번들링
**DevOps** Docker, AWS(ECS Fargate, EC2, CodeDeploy, ALB, CloudFront, S3, Lambda, WAF, IAM), Kubernetes(k3s), Helm, ArgoCD, Jenkins, GitLab CI, Terraform, Ansible
**Observability** Prometheus, Grafana, Alertmanager, OpenTelemetry
</div>

## 학력

**중앙대학교** 경제학 학사

</div>
