---
layout: page
title: 한권희 | DevOps Engineer
subtitle: 근본 원인까지 해결하는 DevOps 엔지니어
---

<style>
  /* 헤더 타이틀 크기 축소 */
  .intro-header .page-heading h1 { font-size: 1.6rem; }
  .intro-header .page-heading .page-subheading { font-size: 1rem; }

  .profile-summary { margin-bottom: 2rem; }
  .badge-skill {
    display: inline-block;
    padding: 5px 13px;
    margin: 4px 5px;
    border-radius: 20px;
    font-size: 0.85rem;
    background: #e8f4fd;
    color: #0069d9;
    border: 1px solid #b8daff;
  }
  .badge-skill.infra { background: #e2f0e8; color: #1a7a3a; border-color: #b8dfc8; }
  .badge-skill.monitor { background: #fff3e0; color: #e65100; border-color: #ffe0b2; }
  .badge-skill.security { background: #fce4ec; color: #c62828; border-color: #f8bbd0; }
  .badge-skill.dev { background: #f3e5f5; color: #6a1b9a; border-color: #e1bee7; }
  .stat-box {
    display: inline-block;
    text-align: center;
    padding: 14px 22px;
    margin: 8px 10px;
    border: 1px solid #dee2e6;
    border-radius: 10px;
    min-width: 130px;
  }
  .stat-box .stat-num { font-size: 1.4rem; font-weight: 700; color: #008AFF; }
  .stat-box .stat-label { font-size: 0.8rem; color: #666; margin-top: 2px; }
  .exp-card {
    border-left: 3px solid #008AFF;
    padding: 14px 18px;
    margin-bottom: 24px;
    background: #fafbfc;
    border-radius: 0 8px 8px 0;
  }
  .exp-card h4 { margin: 0 0 6px 0; font-size: 1.05rem; }
  .exp-card .exp-meta { font-size: 0.85rem; color: #666; margin-bottom: 8px; }
  .exp-card ul { margin: 6px 0 0 0; padding-left: 18px; font-size: 0.9rem; line-height: 1.8; }
  .project-toggle {
    cursor: pointer;
    padding: 18px 22px;
    margin-bottom: 14px;
    border: 1px solid #dee2e6;
    border-radius: 10px;
    transition: all 0.2s;
    background: #fff;
  }
  .project-toggle:hover { border-color: #008AFF; background: #f8f9ff; }
  .project-toggle h4 { margin: 0 0 6px 0; font-size: 1.05rem; }
  .project-toggle .proj-meta { font-size: 0.85rem; color: #555; margin: 0; }
  .project-toggle .proj-summary { font-size: 0.9rem; margin: 6px 0 0 0; color: #333; }
  .project-toggle .toggle-wrap {
    float: right;
    font-size: 0.8rem;
    color: #008AFF;
    margin-top: 4px;
  }
  .project-toggle .toggle-arrow {
    display: inline-block;
    transition: transform 0.3s;
  }
  .project-toggle[aria-expanded="true"] .toggle-arrow { transform: rotate(180deg); }
  .project-detail {
    display: none;
    padding: 16px 20px;
    border: 1px solid #e0e8f0;
    border-top: none;
    border-radius: 0 0 10px 10px;
    margin-top: -9px;
    margin-bottom: 16px;
    background: #fdfdfe;
    font-size: 0.92rem;
  }
  .project-detail h5 { font-size: 1rem; margin-top: 16px; color: #0069d9; }
  .project-detail h6 { font-size: 0.92rem; margin-top: 12px; color: #333; }
  .project-detail ul { padding-left: 18px; }
  .project-detail img { max-width: 100%; border-radius: 8px; margin: 12px 0; }
  .tech-tag {
    display: inline-block;
    padding: 2px 10px;
    margin: 2px 3px;
    border-radius: 4px;
    font-size: 0.8rem;
    background: #f1f3f5;
    color: #495057;
  }
  .section-title {
    font-size: 1.2rem;
    font-weight: 700;
    border-bottom: 2px solid #008AFF;
    padding-bottom: 6px;
    margin: 2.5rem 0 1.2rem 0;
  }
  .strength-item { margin-bottom: 16px; line-height: 1.7; }
  .strength-item strong { color: #0069d9; }
  .open-to-work {
    display: inline-block;
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 600;
    background: #e8f5e9;
    color: #2e7d32;
    border: 1px solid #a5d6a7;
    margin-bottom: 1rem;
  }
  .hook-text {
    font-size: 1.05rem;
    font-weight: 600;
    color: #2C3E50;
    margin-bottom: 0.5rem;
    line-height: 1.6;
  }
  .contact-bar {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
    margin: 1rem 0;
  }
  .contact-bar a {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 8px 18px;
    border-radius: 8px;
    font-size: 0.88rem;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    border: 1px solid #dee2e6;
    color: #333;
  }
  .contact-bar a:hover { border-color: #008AFF; color: #008AFF; background: #f8f9ff; }
  .contact-bar .btn-primary-contact {
    background: #008AFF;
    color: #fff;
    border-color: #008AFF;
  }
  .contact-bar .btn-primary-contact:hover { background: #0069d9; color: #fff; }
  /* PDF 인쇄용 */
  @media print {
    .intro-header, nav, footer, .contact-bar, .toggle-wrap { display: none !important; }
    .project-toggle { border: 1px solid #ccc !important; break-inside: avoid; }
    .project-detail { display: block !important; height: auto !important; }
    .project-detail { border: 1px solid #ccc !important; break-inside: avoid; }
    .project-detail svg { max-height: 300px; }
    .badge-skill, .tech-tag { border: 1px solid #999 !important; }
    body { font-size: 11pt; }
    a { color: #333 !important; text-decoration: none !important; }
    .open-to-work { print-color-adjust: exact; -webkit-print-color-adjust: exact; }
  }
  /* 모바일 반응형 */
  @media (max-width: 576px) {
    .stat-box { min-width: 90px; padding: 10px 12px; margin: 4px; }
    .stat-box .stat-num { font-size: 1.1rem; }
    .stat-box .stat-label { font-size: 0.7rem; }
    .badge-skill { font-size: 0.75rem; padding: 3px 8px; margin: 2px; }
    .tech-tag { font-size: 0.72rem; padding: 2px 6px; }
    .project-toggle { padding: 12px 14px; }
    .project-toggle h4 { font-size: 0.95rem; }
    .project-detail { padding: 12px 14px; }
    .exp-card { padding: 10px 12px; }
    .section-title { font-size: 1.05rem; }
    .hook-text { font-size: 0.95rem; }
    .contact-bar { gap: 8px; }
    .contact-bar a { padding: 6px 12px; font-size: 0.8rem; }
    .strength-item { font-size: 0.88rem; }
  }
</style>

<!-- ====== 핵심 요약 ====== -->
<div class="profile-summary">

<div style="text-align:center;">
  <span class="open-to-work">DevOps · AI 플랫폼 / SRE 포지션에 관심이 있습니다</span>
</div>

<div style="text-align:center; margin-bottom: 1.2rem;">
  <div class="stat-box">
    <div class="stat-num">2년 11개월+</div>
    <div class="stat-label">총 경력</div>
  </div>
  <div class="stat-box">
    <div class="stat-num">13개</div>
    <div class="stat-label">프로젝트</div>
  </div>
  <div class="stat-box">
    <div class="stat-num">DevOps · SRE</div>
    <div class="stat-label">현재 역할</div>
  </div>
</div>

<p class="hook-text" style="text-align:center;">
자사 블록체인 서비스를 AWS·온프레미스 하이브리드로 상시 운영하며,<br>
폐쇄망 LLM 서빙 인프라부터 DDoS 3계층 방어, Blue/Green 무중단 배포까지 단독 수행해 온 DevOps 엔지니어
</p>

Spring 백엔드 개발로 시작하여 Linux 서버 구축·운영, 하이브리드 인프라, CI/CD 파이프라인 구축·개선, 모니터링·알림 체계(관측성), 보안 대응까지 확장했습니다. 장애 발생 시 근본 원인 분석(RCA) → 해결 → 고도화 → 문서화까지 이어가며, 재현 가능한 운영 체계를 만듭니다. 사내 AI 에이전트 실행 플랫폼에서는 쿠버네티스 클러스터(k3s)와 ArgoCD GitOps 배포 체계를 구축하여, Job·NetworkPolicy·RBAC로 신뢰할 수 없는 워크로드를 격리하는 실행 인프라를 운영하고 있습니다.

</div>

<!-- ====== 핵심 기술 ====== -->
<div class="section-title">Core Skills</div>

<span class="badge-skill infra">AWS</span>
<span class="badge-skill infra">Route 53</span>
<span class="badge-skill infra">ALB</span>
<span class="badge-skill infra">EC2</span>
<span class="badge-skill infra">ECS</span>
<span class="badge-skill infra">Docker</span>
<span class="badge-skill infra">Kubernetes (k3s)</span>
<span class="badge-skill infra">Helm</span>
<span class="badge-skill infra">ArgoCD (GitOps)</span>
<span class="badge-skill infra">Linkerd</span>
<span class="badge-skill security">NetworkPolicy · RBAC</span>
<span class="badge-skill infra">Terraform</span>
<span class="badge-skill infra">Ansible</span>
<span class="badge-skill infra">Linux</span>
<span class="badge-skill infra">Nginx</span>
<span class="badge-skill infra">Air-gapped 배포</span>
<span class="badge-skill dev">litellm</span>
<span class="badge-skill dev">IBM watsonx</span>
<span class="badge-skill">Jenkins</span>
<span class="badge-skill">CodeDeploy (Blue/Green)</span>
<span class="badge-skill">GitLab CI</span>
<span class="badge-skill">Bitbucket Pipelines</span>
<span class="badge-skill monitor">Prometheus</span>
<span class="badge-skill monitor">Grafana</span>
<span class="badge-skill monitor">Alertmanager</span>
<span class="badge-skill monitor">CloudWatch</span>
<span class="badge-skill monitor">OpenSearch</span>
<span class="badge-skill security">AWS WAF</span>
<span class="badge-skill security">iptables</span>
<span class="badge-skill security">WireGuard</span>
<span class="badge-skill dev">Java</span>
<span class="badge-skill dev">Spring</span>
<span class="badge-skill dev">JavaScript</span>
<span class="badge-skill dev">Oracle</span>
<span class="badge-skill dev">MySQL</span>
<span class="badge-skill dev">Redis</span>

<!-- ====== 핵심 역량 ====== -->
<div class="section-title">Core Strengths</div>

<div class="strength-item">
  <strong>Air-gapped / AI Platform</strong> — 폐쇄망(망분리) 환경 LLM 서빙 스택 오프라인 배포·운영. deb/wheel/Docker/Yarn Berry 번들링, GPU 드라이버 반입, litellm·watsonx 연동
</div>
<div class="strength-item">
  <strong>CI/CD & Automation</strong> — Jenkins, GitLab CI, Bitbucket Pipelines 기반 CI/CD 파이프라인 구축·개선, CodeDeploy Blue/Green 무중단 배포, 반복 작업 자동화 및 절차 표준화
</div>
<div class="strength-item">
  <strong>Kubernetes &amp; GitOps</strong> — 쿠버네티스 클러스터 직접 구축·운영(경량 배포판 k3s, Linkerd mTLS, Sealed Secrets), ArgoCD app-of-apps로 클러스터 상태를 Git에서 선언적 관리, Job + RBAC + egress NetworkPolicy 기반 워크로드 격리. 관리형(EKS·GKE)이 아닌 self-managed 클러스터를 직접 구성한 경험
</div>
<div class="strength-item">
  <strong>IaC (전환 진행 중)</strong> — Proxmox 3대 홈랩을 Terraform(VM 프로비저닝) + Ansible(k3s 설치·설정)로 코드화, 명령 두 번으로 클러스터 전체 재현
</div>
<div class="strength-item">
  <strong>Hybrid Infrastructure</strong> — AWS + On-Premise 연동 인프라 설계·구축·운영. Route 53, ALB, EC2, ECS, Docker, Nginx 기반 서비스 아키텍처
</div>
<div class="strength-item">
  <strong>Observability & Reliability</strong> — Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반 모니터링·로깅·알림 체계 구축으로 관측성 확보
</div>
<div class="strength-item">
  <strong>Security & Troubleshooting</strong> — AWS WAF, Nginx, iptables 다층 방어. 로그 기반 근본 원인 분석(RCA)과 재발 방지, 금융권 망분리 환경 장애 진단
</div>

<!-- ====== 경력 ====== -->
<div class="section-title">Experience</div>

<div class="exp-card">
  <h4>(주)베리드코리아 <small style="color:#008AFF;">Developer · DevOps · SRE</small></h4>
  <div class="exp-meta">개발팀 / 주임 · 2024.08 ~ Present</div>
  <ul>
    <li>자사 블록체인 서비스(BaaS·Wallet·Scan) AWS·온프레미스 하이브리드 인프라 상시 운영 — 장애 트러블슈팅 1주일 → 30분 단축, 봇 트래픽 하루 평균 1,000+ IP 차단으로 AWS 비용 20%+ 절감</li>
    <li>사내 AI 에이전트 실행 플랫폼 인프라 구축(2026.05~): <strong>AI가 스스로 작성한 코드를 안전하게 실행</strong>하기 위한 격리 환경 구축 — 실행 1건마다 일회용 컨테이너로 분리하고 외부로 나가는 통신을 차단해 <strong>API 키 유출 경로 제거</strong>, 쿠버네티스 클러스터 직접 구축 + ArgoCD GitOps 배포 자동화</li>
    <li>하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터(2026.05~07, 완료): 금융권 망분리 환경 SSO·DRM 어댑터 구축, 다단계 연동 구간의 통신 장애 진단 및 다자간 업무 조율</li>
    <li>삼성디스플레이 폐쇄망 LLM 서빙 인프라 구축(2026.05~06): 5개 서비스 오프라인 배포, 반입-배포 사이클 1일 → 30분 단축</li>
    <li>KBS 재난방송 STG 인프라(2026.04~05): ECS·CodeDeploy Blue/Green 기반 AWS 스테이징 환경 단독 설계·구축</li>
    <li>AWS + 온프레미스 하이브리드 인프라 운영 절차 표준화 → 팀 누구나 동일한 절차로 배포·운영 가능</li>
    <li>AWS WAF + Nginx + iptables 3계층 방어 아키텍처 구축 → 2일 1회 서버 중단을 장애 제로화</li>
    <li>Prometheus/Grafana 모니터링·알림 체계 구축(관측성 확보) + Slack 실시간 알림 → 장애 인지 시간 대폭 단축</li>
    <li>Jenkins 기반 CI/CD 파이프라인 구축 + Blue/Green 무중단 배포 → 서비스 중단 없는 배포 체계 확립</li>
    <li>온프레미스 서버실 구축, VM 백업·복원 자동화 → 재해복구(DR) 체계 확립</li>
    <li>MCP + OpenSearch + Lambda 기반 AI 실행 인프라 → 재현 가능한 질의응답 파이프라인 구축</li>
    <li>삼성SDR 파견(2025.09~2026.03): 내방객 관리시스템 풀스택 개발 + 카드사 연동 REST API 설계·개발</li>
  </ul>
</div>

<div class="exp-card">
  <h4>(주)아이뱅크컨설턴츠 <small style="color:#008AFF;">Developer</small></h4>
  <div class="exp-meta">개발팀 / 대리 · 2023.09 ~ 2024.07</div>
  <ul>
    <li>React / Thymeleaf / Spring Boot 기반 풀스택 개발 및 운영 환경 정비</li>
    <li>GitLab + Jenkins CI/CD 파이프라인 도입 → 배포 절차 표준화</li>
    <li>SVN → Git 전환 주도 및 사내 교육 → 팀 형상관리 체계 현대화</li>
  </ul>
</div>

<!-- ====== 프로젝트 (아코디언) ====== -->
<div class="section-title">Projects</div>

<p style="font-size:0.88rem; color:#666;">각 프로젝트를 클릭하면 상세 내용을 확인할 수 있습니다.</p>

<div id="projectAccordion">

  <!-- 프로젝트 0-0: Berith 서비스 상시 운영 (2024.08 ~ 현재) -->
  <div class="project-toggle" data-target="#proj-berith-ops" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>⛓️ Berith 블록체인 서비스 하이브리드 인프라 상시 운영</h4>
    <p class="proj-meta">2024.08 ~ 현재 · DevOps / SRE</p>
    <p class="proj-summary">자사 서비스(BaaS·Wallet·Scan)를 AWS(EC2 7대 + RDS + OpenSearch) + 온프레미스 이중화로 상시 운영 — 트러블슈팅 1주일 → 30분, 봇 트래픽 일평균 1,000+ IP 차단, AWS 비용 20%+ 절감</p>
    <div>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">EC2</span>
      <span class="tech-tag">RDS</span>
      <span class="tech-tag">OpenSearch</span>
      <span class="tech-tag">Route 53</span>
      <span class="tech-tag">Nginx</span>
      <span class="tech-tag">On-Premise</span>
      <span class="tech-tag">Blockchain Node</span>
    </div>
  </div>
  <div id="proj-berith-ops" class="project-detail">
    <h5>Background</h5>
    <p>기업용 블록체인 기록 서비스 <strong>BaaS</strong>(삼성디스플레이 보안서약서, 롯데이노베이츠 물품관리 이력)와 B2C 서비스(<strong>Berith Wallet·Berith Scan</strong>)를 AWS와 온프레미스를 연동한 하이브리드 구성으로 상시 운영합니다. 부트노드 2대·메인넷 노드(이더리움 계열 자체 메인넷) 포함 EC2 7대, RDS, OpenSearch(체인 데이터 인덱싱), 온프레미스 이중화 서버로 구성되며, 지갑 서비스 특성상 <strong>계정 탈취를 노리는 무차별 대입·봇 공격이 상시 유입</strong>되는 환경입니다.</p>

    <h5>What I Did</h5>
    <ul>
      <li>메인넷·부트노드 노드 운영, Nginx 웹 계층(Route 53 기반 AWS·온프레미스 요청 라우팅) 운영</li>
      <li>모니터링·알림 체계 구축과 장애별 RCA 문서화 — "뭔가 안 된다" 수준의 신고에서 시작하던 트러블슈팅을 체계화</li>
      <li>단일 봇 차단 후 다수 IP가 로테이션하며 공격하는 패턴으로 진화하자 WAF·Nginx·iptables 3계층 차단 룰을 단계적으로 고도화</li>
      <li>메인넷 노드 다운의 근본 원인을 디스크 I/O 병목 + 체인 데이터 용량 부족으로 특정 — EBS 증설과 함께, 장비 증설 없이 BaaS 요청을 온프레미스 메인넷으로 분산(Wallet은 AWS 유지)하는 구조 변경으로 해소</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>장애 트러블슈팅 소요 시간 <strong>1주일 → 30분 이내 단축</strong></li>
      <li>봇 트래픽 <strong>하루 평균 1,000개 이상 IP 자동 차단</strong>, <strong>AWS 비용 20% 이상 절감</strong></li>
      <li>이중화 일부 온프레미스 이관으로 AWS 비용 추가 절감, 비용 증설 없이 I/O 병목 해소</li>
    </ul>
  </div>

  <!-- 프로젝트 0-0b: AI 에이전트 실행 플랫폼 (진행 중) -->
  <div class="project-toggle" data-target="#proj-ai-agent" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>🤖 AI 에이전트 실행 플랫폼 — Kubernetes 기반 격리 실행 인프라</h4>
    <p class="proj-meta">2026.05 ~ 진행 중 · 사내 프로젝트 · 클러스터 구축·GitOps 배포 파이프라인 담당</p>
    <p class="proj-summary">스스로 코드를 수정하는 AI 에이전트를 안전하게 실행하기 위해, 실행 건당 Job 1개로 격리하는 쿠버네티스 기반 인프라 구축</p>
    <div>
      <span class="tech-tag">Kubernetes</span>
      <span class="tech-tag">k3s</span>
      <span class="tech-tag">ArgoCD</span>
      <span class="tech-tag">Helm</span>
      <span class="tech-tag">NetworkPolicy</span>
      <span class="tech-tag">RBAC</span>
      <span class="tech-tag">Linkerd</span>
      <span class="tech-tag">Sealed Secrets</span>
    </div>
  </div>
  <div id="proj-ai-agent" class="project-detail">
    <h5>Background</h5>
    <p>이전 POC에서 에이전트가 호스트 파일을 건드려 자기 실행 환경을 망가뜨리는 일이 있었습니다. 에이전트에는 모델 API 키와 사내 서비스 토큰이 주입되기 때문에, <strong>격리 실패는 곧 시크릿 유출</strong>이었습니다.</p>

    <h5>What I Did</h5>
    <ul>
      <li>사내 VM에 <strong>쿠버네티스 클러스터 구축</strong>(경량 배포판 k3s) — 기본 traefik을 ingress-nginx로 교체하고, Linkerd 서비스 메시로 서비스 간 mTLS 적용</li>
      <li><strong>에이전트 실행 1건 = Job 1개</strong>로 격리. 전용 네임스페이스와 최소 권한 ServiceAccount를 부여하고, 실패 재실행·무한 대기·잔여 리소스를 Job 옵션으로 차단</li>
      <li><strong>egress NetworkPolicy</strong>로 에이전트 Pod의 아웃바운드를 사내 서비스와 모델 API로만 제한해 시크릿이 밖으로 나갈 경로를 차단. API 키는 Sealed Secrets로 Git에 암호문 보관</li>
      <li><strong>ArgoCD app-of-apps</strong>로 클러스터 상태를 Git에서 관리(Helm 차트). Bitbucket Pipelines + self-hosted runner로 배포하고, 배포 후 스모크검증 자동 실행</li>
      <li>레지스트리(Harbor·Kellnr·Verdaccio)를 전량 self-host하고, Prometheus·Grafana·Tempo로 관측성 확보</li>
    </ul>

  </div>

  <!-- 프로젝트 0-1: 하나증권 그룹웨어 어댑터 (2026.05 ~ 진행중) -->
  <div class="project-toggle" data-target="#proj-hana" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>🏦 하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터 엔지니어링</h4>
    <p class="proj-meta">2026.05 ~ 2026.07 (완료) · 2026.07.15 정상 오픈 · 어댑터 엔지니어 (총 6인)</p>
    <p class="proj-summary">업체가 모두 다른 시스템이 다단계로 이어지는 금융권 망분리 환경에서 SSO·DRM 어댑터를 구축하고, 구간별 통신 검증으로 연동 장애 원인을 특정·조율하여 해결</p>
    <div>
      <span class="tech-tag">Spring Boot</span>
      <span class="tech-tag">SSO</span>
      <span class="tech-tag">DRM</span>
      <span class="tech-tag">DNS</span>
      <span class="tech-tag">방화벽</span>
      <span class="tech-tag">VPN</span>
      <span class="tech-tag">금융권 망분리</span>
    </div>
  </div>
  <div id="proj-hana" class="project-detail">
    <h5>Background</h5>
    <p>하나증권 <strong>AI 협업솔루션 POC</strong> 프로젝트의 세부 과제로, 그룹웨어(SaaS) 연동용 SSO·DRM 어댑터의 구축과 연동 트러블슈팅을 담당했습니다. <strong>Dooray(외부망) → VPN → 하나증권 인프라 → SSO·DRM 어댑터 → 내부 SSO·DRM 애플리케이션</strong>으로 이어지는 다단계 연동 구간에서 통신 장애가 발생했는데, 구간마다 담당 업체가 모두 달라 어느 한 곳도 전체 흐름을 알지 못하는 상태로 원인 규명이 정체되는 상황이었습니다.</p>

    <h5>What I Did</h5>
    <h6>어댑터 구축 및 구간별 장애 진단</h6>
    <ul>
      <li>SSO·DRM 어댑터 설치 및 구동 스크립트 구축</li>
      <li>장애 발생 시 전체 통신 경로를 구간별로 나누어 검증 — 각 주체의 설정 파일 확인 → 테스트 요청 → 로그 분석 → 원인 구간 특정 → 해당 업체 조치 요청의 사이클을 반복하며 원인을 좁혀가는 방식으로 해결</li>
      <li>운영 서버 SSO 초기화 실패를 DNS 미해석 + 방화벽 미개방으로 특정한 사례 등, 서버 권한 제약 환경에서 비침습적 진단으로 조치 요청의 근거 확보</li>
    </ul>
    <h6>다자간 업무 조율</h6>
    <ul>
      <li>HA 업체, VPN 업체, 하나증권 인프라팀·현업, Dooray 등 구간별 담당 업체 간 업무 조율</li>
      <li>고객사 IT 현업과 주간 정례 미팅으로 이슈·일정 직접 협의</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>전 테스트 통과, <strong>잔여 이슈 없이 7/15 정상 오픈 — 담당 업무 완료</strong></li>
      <li>여러 업체에 걸쳐 있던 연동 장애를 구간별 검증으로 해소하여 일정 지연 방지</li>
      <li>애플리케이션·OS·네트워크를 관통하는 통신 구조 분석과 장애 진단·조율 프로세스 경험 확보</li>
    </ul>
  </div>

  <!-- 프로젝트 0-2: 삼성디스플레이 폐쇄망 AI POC (2026.05 ~ 2026.06) -->
  <div class="project-toggle" data-target="#proj-sdc-poc" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>🔒 삼성디스플레이 폐쇄망 LLM 서빙 인프라 구축 (AI POC)</h4>
    <p class="proj-meta">2026.05 ~ 2026.06 · 폐쇄망 인프라 담당 (인프라 1인 / 총 5인)</p>
    <p class="proj-summary">인터넷 완전 차단(air-gapped) 망분리 환경에 LLM 서빙 스택 5종을 오프라인 배포. 반입-배포 사이클 1일 → 30분 단축, POC 성공 완료</p>
    <div>
      <span class="tech-tag">Air-gapped</span>
      <span class="tech-tag">Python</span>
      <span class="tech-tag">litellm</span>
      <span class="tech-tag">IBM watsonx</span>
      <span class="tech-tag">Docker</span>
      <span class="tech-tag">Yarn Berry</span>
      <span class="tech-tag">Linux</span>
      <span class="tech-tag">GPU Driver</span>
    </div>
  </div>
  <div id="proj-sdc-poc" class="project-detail">
    <h5>Background</h5>
    <p>인터넷이 완전히 차단된(air-gapped) 삼성디스플레이 폐쇄망 환경에서 LLM 서빙 스택(LLM 게이트웨이, Text-to-SQL 엔진, STT, 임베딩 서버 등 5개 서비스)의 오프라인 배포 파이프라인을 설계하고 POC를 완수해야 했습니다. CI/CD 구성이 불가능하고, 모든 산출물은 내부망 반입 프로세스(물리 반입)로만 전달할 수 있는 환경이었습니다.</p>

    <h5>What I Did</h5>
    <h6>3단계 반입 아키텍처 설계·운영</h6>
    <ul>
      <li>외부 빌드 서버 → 오프라인 번들링 → USB 물리 반입 → 폐쇄망 워크스테이션 배포로 이어지는 반입 체계 설계 (총 번들 규모 1TB 이상)</li>
      <li>빌드·배포 파이프라인 전 과정을 직접 수행하고, 반입 이력·시행착오를 체계적으로 문서화하여 반복 배포 절차 표준화</li>
    </ul>
    <h6>연동 장애 분석·해결</h6>
    <ul>
      <li>Python 애플리케이션과 IBM watsonx API 연동: LLM 게이트웨이(litellm) 설정, 토큰 만료(12h) 대응 체계, SSL 인증서 체인 구성</li>
      <li>연동 장애의 원인 분석과 설정 레벨 해결</li>
    </ul>
    <h6>오프라인 환경 특화 문제 해결</h6>
    <ul>
      <li>Yarn Berry 기반 프런트엔드 오프라인 빌드</li>
      <li>GPU 드라이버 사전 빌드 반입, deb/wheel 오프라인 패키지 번들링</li>
    </ul>
    <h6>이해관계자 조율</h6>
    <ul>
      <li>프로젝트 초기 현장의 도입 반대와 제한적 협조 상황에서 신뢰 관계를 먼저 구축</li>
      <li>고객사 PM·기존 개발진 사이의 커뮤니케이션을 조율하여 프로젝트를 정상 궤도로 복원</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li><strong>POC 성공적 완료</strong> — 전 애플리케이션 정상 동작 시연, 고객사 임원 보고 긍정 평가 → 후속 AI 프로젝트 협업으로 연결</li>
      <li>반입-배포 1사이클 소요 시간 <strong>1일 → 30분으로 단축</strong> (이력관리 기반 절차 개선)</li>
      <li>폐쇄망 5개 서비스 스택 전체를 단독으로 배포·운영</li>
    </ul>
  </div>

  <!-- 프로젝트 0-3: KBS 재난방송 STG 인프라 (2026.04 ~ 2026.05) -->
  <div class="project-toggle" data-target="#proj-kbs-stg" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>📡 KBS 통합재난방송시스템 STG 인프라 구축</h4>
    <p class="proj-meta">2026.04 ~ 2026.05 · 인프라 설계·구축 단독 담당 (1인)</p>
    <p class="proj-summary">ECS·CodeDeploy Blue/Green 기반 AWS 스테이징 환경 단독 설계·구축, 실 작업 2주 내 전 리소스 구축 완료 및 Jenkins 배포 파이프라인 검증</p>
    <div>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">ECS</span>
      <span class="tech-tag">ECR</span>
      <span class="tech-tag">ALB</span>
      <span class="tech-tag">CodeDeploy</span>
      <span class="tech-tag">Blue/Green</span>
      <span class="tech-tag">CloudFront</span>
      <span class="tech-tag">S3</span>
      <span class="tech-tag">DynamoDB</span>
      <span class="tech-tag">IAM</span>
      <span class="tech-tag">Jenkins</span>
    </div>
  </div>
  <div id="proj-kbs-stg" class="project-detail">
    <h5>Background</h5>
    <p>KBS 통합재난방송시스템 클라우드 플랫폼의 스테이징(STG) 환경을 AWS 상에 신규 구축해야 했습니다. 인수인계가 최소화된 상황에서 기존 운영(PRD) 인프라를 역분석하여 동등한 환경을 재현하는 것이 과제였습니다.</p>

    <h5>What I Did</h5>
    <h6>STG 환경 신규 구축</h6>
    <ul>
      <li>기존 운영(PRD) 인프라 분석 후 보안그룹/네트워크, ECR, ECS 클러스터·태스크·서비스 구축</li>
      <li>ALB·타겟그룹·CodeDeploy(Blue/Green), CloudFront·S3(IP 접근 제한), DynamoDB 구성</li>
      <li>IAM 개발자 계정 권한 설계</li>
    </ul>
    <h6>아키텍처 의사결정 주도</h6>
    <ul>
      <li>환경 분리 방식, 도메인·인증서 체계 등 비용과 운영 부담에 직결되는 사안을 대안 비교로 직접 검토·제안하여, 불필요한 추가 비용과 관리 복잡도 없이 구축 방향 확정</li>
    </ul>
    <h6>고객사 직접 협의</h6>
    <ul>
      <li>KBS 인프라팀과 직접 미팅·유선·메일로 도메인 발급, DNS(A/CNAME) 신청, 일정 협의 수행</li>
      <li>무리한 일정에 대해 근거를 들어 재조정을 건의하고 관철</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>분석 10일 + 구축 4일, <strong>실 작업 2주 내 STG 전 리소스 구축 완료</strong></li>
      <li>Jenkins 배포 테스트 정상 동작 확인으로 프로젝트 마무리</li>
      <li>인수인계 최소화 상황에서 기존 운영 환경을 역분석하여 동등 환경 재현</li>
    </ul>
  </div>

  <!-- 프로젝트 1: VM 관리 웹페이지 (2026.04) -->
  <div class="project-toggle" data-target="#proj-vm-web" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>온프레미스 VM 관리 웹페이지</h4>
    <p class="proj-meta">2026.04 ~ 2026.04 · 설계 및 개발 전체 · 기여도 100%</p>
    <p class="proj-summary">VM 복제 수작업 30분 → 웹 클릭 한 번으로 단축. Blue/Green 무중단 배포, QA 자동화까지 포함한 풀스택 인프라 관리 시스템</p>
    <div>
      <span class="tech-tag">React 19</span>
      <span class="tech-tag">TypeScript</span>
      <span class="tech-tag">Spring Boot 3</span>
      <span class="tech-tag">Java 21</span>
      <span class="tech-tag">MariaDB</span>
      <span class="tech-tag">Docker</span>
      <span class="tech-tag">Jenkins CI/CD</span>
      <span class="tech-tag">Claude MCP</span>
      <span class="tech-tag">VirtualBox</span>
      <span class="tech-tag">ZFS</span>
    </div>
  </div>
  <div id="proj-vm-web" class="project-detail">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 520" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:12px 0;">
      <defs>
        <filter id="shadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="arrowhead" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <linearGradient id="gBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="gGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="gOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
        <linearGradient id="gPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
        <linearGradient id="gGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
      </defs>
      <rect width="900" height="520" fill="#FAFBFC" rx="12"/>
      <text x="450" y="35" text-anchor="middle" font-size="18" font-weight="700" fill="#2C3E50">On-Premise VM Management Web System</text>
      <rect x="340" y="55" width="220" height="50" rx="8" fill="url(#gBlue)" filter="url(#shadow)"/>
      <text x="450" y="76" text-anchor="middle" font-size="13" font-weight="600" fill="#fff">Web Browser (User)</text>
      <text x="450" y="93" text-anchor="middle" font-size="10" fill="#D6EAF8">VM OS / Network / Snapshot Control</text>
      <path d="M450,105 L450,135" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <text x="465" y="123" font-size="9" fill="#7F8C8D">HTTPS</text>
      <rect x="280" y="140" width="340" height="60" rx="8" fill="url(#gPurple)" filter="url(#shadow)"/>
      <text x="450" y="164" text-anchor="middle" font-size="14" font-weight="600" fill="#fff">Claude MCP Server</text>
      <text x="450" y="182" text-anchor="middle" font-size="10" fill="#E8DAEF">Model Context Protocol — AI Interface Layer</text>
      <path d="M450,200 L450,230" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <text x="465" y="218" font-size="9" fill="#7F8C8D">MCP Tools</text>
      <rect x="70" y="235" width="760" height="75" rx="8" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1"/>
      <text x="450" y="255" text-anchor="middle" font-size="12" font-weight="600" fill="#2C3E50">Control Layer</text>
      <rect x="95" y="262" width="160" height="38" rx="6" fill="url(#gGreen)" filter="url(#shadow)"/>
      <text x="175" y="278" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">OS Management</text>
      <text x="175" y="293" text-anchor="middle" font-size="9" fill="#D5F5E3">Create / Clone / Start / Stop</text>
      <rect x="275" y="262" width="160" height="38" rx="6" fill="url(#gGreen)" filter="url(#shadow)"/>
      <text x="355" y="278" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Network Config</text>
      <text x="355" y="293" text-anchor="middle" font-size="9" fill="#D5F5E3">IP Validation / Netplan / ARP</text>
      <rect x="455" y="262" width="160" height="38" rx="6" fill="url(#gGreen)" filter="url(#shadow)"/>
      <text x="535" y="278" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Backup &amp; DR</text>
      <text x="535" y="293" text-anchor="middle" font-size="9" fill="#D5F5E3">ZFS / Cron / Archive</text>
      <rect x="635" y="262" width="170" height="38" rx="6" fill="url(#gGreen)" filter="url(#shadow)"/>
      <text x="720" y="278" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Blue/Green Deploy</text>
      <text x="720" y="293" text-anchor="middle" font-size="9" fill="#D5F5E3">Jenkins / Health Check</text>
      <path d="M450,310 L450,340" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <text x="465" y="328" font-size="9" fill="#7F8C8D">VBoxManage / SSH</text>
      <rect x="180" y="345" width="540" height="50" rx="8" fill="url(#gOrange)" filter="url(#shadow)"/>
      <text x="450" y="367" text-anchor="middle" font-size="14" font-weight="600" fill="#fff">VM Host — Linux (VirtualBox)</text>
      <text x="450" y="383" text-anchor="middle" font-size="10" fill="#FEF9E7">VBoxManage CLI / VRDE / Guest Properties</text>
      <path d="M300,395 L300,420" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <path d="M450,395 L450,420" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <path d="M600,395 L600,420" stroke="#7F8C8D" stroke-width="2" marker-end="url(#arrowhead)"/>
      <rect x="120" y="425" width="200" height="70" rx="8" fill="url(#gGray)" filter="url(#shadow)"/>
      <text x="220" y="450" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">VM 1 (Dev Server)</text>
      <text x="220" y="467" text-anchor="middle" font-size="9" fill="#D5D8DC">Ubuntu 22.04</text>
      <text x="220" y="480" text-anchor="middle" font-size="9" fill="#D5D8DC">Docker / App / DB</text>
      <rect x="350" y="425" width="200" height="70" rx="8" fill="url(#gGray)" filter="url(#shadow)"/>
      <text x="450" y="450" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">VM 2 (Staging)</text>
      <text x="450" y="467" text-anchor="middle" font-size="9" fill="#D5D8DC">Ubuntu 22.04</text>
      <text x="450" y="480" text-anchor="middle" font-size="9" fill="#D5D8DC">Web / WAS / Test</text>
      <rect x="580" y="425" width="200" height="70" rx="8" fill="url(#gGray)" filter="url(#shadow)"/>
      <text x="680" y="450" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">VM N (Service)</text>
      <text x="680" y="467" text-anchor="middle" font-size="9" fill="#D5D8DC">CentOS / Ubuntu</text>
      <text x="680" y="480" text-anchor="middle" font-size="9" fill="#D5D8DC">Production Workload</text>
      <text x="40" y="515" font-size="9" fill="#95A5A6">Web Browser → Claude MCP → Control Layer → VBoxManage CLI → Virtual Machines</text>
    </svg>

    <h5>Background</h5>
    <p>개발팀의 VirtualBox VM 서버를 관리하면서, VM 생성·복제·백업을 매번 SSH 접속 후 CLI 명령어로 수행하는 비효율을 경험했습니다. 특히 VM 복제 시 호스트명 변경, 고정 IP 할당, SSH 키 재생성 등 7단계를 수작업으로 처리해야 했고, 백업 역시 cron과 쉘 스크립트에 의존하여 이력 추적과 실패 감지가 어려웠습니다. 이러한 반복 작업을 웹 인터페이스로 통합하여, 누구나 안전하게 인프라를 운영할 수 있는 관리 도구를 만들고자 했습니다.</p>

    <h5>What I Did</h5>
    <h6>Claude MCP 기반 개발 워크플로우</h6>
    <ul>
      <li>Claude Code CLI와 MCP(Model Context Protocol) 서버를 연동하여 Redmine 이슈 기반 개발 워크플로우 구축</li>
      <li>PRD → 기능정의 → 컨텍스트 → 태스크의 4단계 이슈 계층 자동 생성</li>
      <li>독립 평가자 에이전트(/evaluate)와 QA 자동 사이클(/qa-cycle)을 커스텀 스킬로 구현</li>
      <li>코드 검증과 버그 수정을 최대 3회까지 자동 반복 실행</li>
    </ul>
    <h6>VM 라이프사이클 관리</h6>
    <ul>
      <li>VBoxManage CLI를 파싱하여 VM 생성, 시작/중지, 리소스 변경(CPU·RAM·디스크), 삭제를 웹에서 수행</li>
      <li>VM 복제: 소스 검증 → 클론 → 부팅 감지 → 호스트명 → 고정 IP → SSH 키 재생성 → 네트워크 검증의 7단계 비동기 Job 설계</li>
      <li>프론트엔드에서 단계별 진행률 실시간 확인</li>
      <li>템플릿 VM 기반 프로비저닝, VRDE 원격 데스크톱 포트 자동 할당(4000~4100)</li>
    </ul>
    <h6>네트워크 관리</h6>
    <ul>
      <li>IP 할당 전 다단계 검증: IPv4 형식 → 서브넷·게이트웨이 계산 → 예약 IP 필터링 → ARP 테이블 조회 → Guest Property 교차 확인 → Ping 테스트</li>
      <li>Netplan YAML 자동 생성·배포로 고정 IP 설정</li>
      <li>사용 중인 IP 현황 대시보드 제공</li>
    </ul>
    <h6>스냅샷·백업·재해복구</h6>
    <ul>
      <li>전체/DB전용/일반전용/개별 VM의 4가지 백업 모드 지원</li>
      <li>백업 서버 2대 비동기 실행 및 실시간 로그 모니터링</li>
      <li>ZFS 스냅샷 기반 복원, 장기 아카이브, DR 서버 동기화</li>
      <li>Quartz 호환 Cron 스케줄링, 백업 이력 DB 영속화로 실패 자동 감지</li>
    </ul>

    <h5>Technical Highlights</h5>
    <ul>
      <li>Blue/Green 무중단 배포를 Jenkins 파이프라인으로 구현, Health Check 실패 시 자동 롤백, Spring Session JDBC로 세션 유지</li>
      <li>장시간 작업(VM 복제·삭제)을 비동기 Job 트래커로 관리하여 7단계 진행률을 API로 제공, 완료 Job은 1시간 후 자동 정리</li>
      <li>Docker 멀티스테이지 빌드(Node 22 → Gradle 8 → JRE 21 Alpine)로 단일 이미지 패키징, 비root 사용자 실행으로 컨테이너 보안 확보</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>VM 복제를 수작업 30분 이상에서 웹 클릭 한 번으로 단축, 7단계 자동 프로비저닝으로 휴먼 에러 제거</li>
      <li>백업 이력 DB 영속화와 상태 자동 감지로 실패한 백업 즉시 파악·대응 가능</li>
      <li>Blue/Green 배포로 서비스 중단 없이 업데이트, Health Check 실패 시 자동 롤백으로 운영 안정성 확보</li>
      <li>Claude MCP 기반 QA 자동화 사이클로 코드 검증·수정·재검증 자동 반복, 개발 생산성과 코드 품질 동시 향상</li>
    </ul>

    <h5>Tech Stack</h5>
    <p>
      <span class="tech-tag">React 19</span>
      <span class="tech-tag">TypeScript 5.9</span>
      <span class="tech-tag">Vite 8</span>
      <span class="tech-tag">Ant Design 6</span>
      <span class="tech-tag">Spring Boot 3.4</span>
      <span class="tech-tag">Java 21</span>
      <span class="tech-tag">Gradle 8</span>
      <span class="tech-tag">Spring Data JPA</span>
      <span class="tech-tag">Spring Security</span>
      <span class="tech-tag">MariaDB 10.6</span>
      <span class="tech-tag">Flyway</span>
      <span class="tech-tag">Docker</span>
      <span class="tech-tag">Jenkins CI/CD</span>
      <span class="tech-tag">Nginx</span>
      <span class="tech-tag">ZFS</span>
      <span class="tech-tag">VirtualBox</span>
      <span class="tech-tag">Claude MCP</span>
      <span class="tech-tag">Redmine API</span>
    </p>
  </div>

<!-- Project 2: Samsung SDR (2025.09 ~ 2026.03) -->
<div class="project-toggle" data-target="#proj-sdr" aria-expanded="false">
  <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
  <h4>Samsung SDR 방문자 관리 시스템</h4>
  <p class="proj-meta">2025.09 ~ 2026.03 · 풀스택 개발자 · 배포/운영 담당</p>
  <p class="proj-summary">
    카드 발급/회수 자동화와 데이터 정합성 개선을 통해 방문자 출입 관리 시스템을 구축하고,
    JSP + MyBatis 기반 레거시 환경에서 발생하는 실제 운영 이슈를 해결하며 시스템 안정성을 향상시킴
  </p>
  <div>
    <span class="tech-tag">Java</span>
    <span class="tech-tag">Spring MVC</span>
    <span class="tech-tag">JSP</span>
    <span class="tech-tag">JavaScript</span>
    <span class="tech-tag">MyBatis</span>
    <span class="tech-tag">JBoss</span>
    <span class="tech-tag">REST API</span>
    <span class="tech-tag">Oracle SQL</span>
  </div>
</div>

<div id="proj-sdr" class="project-detail">
  <h5>프로젝트 배경</h5>
  <p>
    삼성 SDR 사업장의 방문자 출입 관리를 수기/반자동 방식에서 웹 기반 시스템으로 전환하고,
    카드 발급·회수 및 출입 이력 관리까지 통합하여 운영 효율성과 데이터 신뢰성을 개선하는 것이 목적이었음
  </p>

<h5>주요 수행 내용</h5>

<h6>백엔드 개발</h6>
  <ul>
    <li>방문자 등록, 승인, 출입, 이력 관리 등 비즈니스 로직 설계 및 구현</li>
    <li>카드사 연동 API 개발을 통한 발급/회수 상태 실시간 동기화</li>
    <li>DB 구조 분석</li>
  </ul>

<h6>프론트엔드 개발</h6>
  <ul>
    <li>JSP + Grid 기반 화면 개발</li>
    <li>JavaScript를 활용한 동적 UI 처리 및 입력 검증 로직 구현</li>
  </ul>

<h6>배포 및 운영</h6>
  <ul>
    <li>JBoss 환경 설정 및 WAS 운영</li>
    <li>배포 전략 수립 및 운영 안정화</li>
    <li>운영/인수인계 문서 작성 및 해외 개발자 협업 지원</li>
  </ul>

<h5>성과</h5>
  <ul>
    <li>카드 발급/회수 자동화로 방문자 처리 업무 효율 개선</li>
    <li>UI–DB 간 데이터 흐름 정합성을 확보하여 유지보수성 향상</li>
    <li>레거시 환경(JSP + MyBatis)에서 안정적인 운영 구조 구축</li>
  </ul>
</div>

  <!-- 프로젝트 2: DDoS (2025.08) -->
  <div class="project-toggle" data-target="#proj-ddos" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>DDoS 대응체계 구축</h4>
    <p class="proj-meta">2025.08 · SRE · 기여도 100%</p>
    <p class="proj-summary">2일 1회 서버 중단(CPU 140%, 로그 일 100GB+) → 3계층 방어 체계 구축으로 장애 제로화, 일평균 1,000+ IP 자동 차단으로 AWS 비용 20%+ 절감</p>
    <div>
      <span class="tech-tag">AWS WAF</span>
      <span class="tech-tag">ALB</span>
      <span class="tech-tag">CloudWatch</span>
      <span class="tech-tag">Nginx</span>
      <span class="tech-tag">iptables</span>
      <span class="tech-tag">Shell Script</span>
    </div>
  </div>
  <div id="proj-ddos" class="project-detail">
    <img src="{{ '/assets/ddos_arc.drawio.png' | relative_url }}" alt="DDoS 3계층 방어 아키텍처">

    <h5>Background</h5>
    <p>분산된 L7 공격으로 봇/스캐너 트래픽이 폭증하여 <strong>WAS CPU 사용률이 140%까지 치솟고, catalina.out 로그가 하루 100GB 이상</strong> 쌓이며 <strong>2일에 1회꼴로 서버가 중단</strong>되는 상황이었습니다. 단일 지점 차단만으로는 대응이 어려워 Cloud-Web-WAS 다층 방어가 필요했습니다.</p>

    <h5>What I Did</h5>
    <h6>Cloud Layer</h6>
    <ul>
      <li>AWS WAF 구성 및 ALB 연동</li>
      <li>AWS Managed Rule 적용 + Rate-based Custom Rule 추가</li>
      <li>WAF 로그를 CloudWatch 연결하여 운영 가시성 확보</li>
    </ul>
    <h6>Web Layer</h6>
    <ul>
      <li>User-Agent 필터링 및 Rate Limiting 설정</li>
      <li>공격 대상 엔드포인트를 Nginx 레벨에서 직접 제어</li>
    </ul>
    <h6>WAS Layer</h6>
    <ul>
      <li>Tomcat Access Log 분석</li>
      <li>iptables 기반 자동 차단 스크립트 작성 및 운영</li>
      <li>단일 IP 차단 → 분산 공격 대응으로 확장</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>2일 1회 서버 중단 → 방어 체계 구축 후 <strong>장애 제로화</strong></li>
      <li>WAS CPU 140% → 정상 범위로 안정화, catalina.out 로그 폭증 문제 해소</li>
      <li>단일 IP 차단 → 다수 IP 로테이션 공격 대응으로 고도화, <strong>하루 평균 1,000개 이상 IP 자동 차단</strong></li>
      <li>봇/스캐너 요청을 Cloud 레벨에서 선제 차단하여 <strong>AWS 비용 20% 이상 절감</strong></li>
      <li>Cloud-Web-WAS를 아우르는 재사용 가능한 방어 패턴 확보</li>
    </ul>
  </div>

  <!-- 프로젝트 3: AI 실행 인프라 (2025.08) -->
  <div class="project-toggle" data-target="#proj-ai" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>AI 실행 인프라 구축</h4>
    <p class="proj-meta">2025.08 · DevOps · 기여도 100%</p>
    <p class="proj-summary">서버리스+상시운영 하이브리드 구조로 비용 효율적인 AI 질의응답 파이프라인 구축, 재현 가능한 실행 환경 확보</p>
    <div>
      <span class="tech-tag">Claude MCP</span>
      <span class="tech-tag">OpenSearch</span>
      <span class="tech-tag">AWS S3</span>
      <span class="tech-tag">AWS Lambda</span>
      <span class="tech-tag">EC2</span>
    </div>
  </div>
  <div id="proj-ai" class="project-detail">
    <img src="{{ '/assets/Chatbot-arc.drawio.png' | relative_url }}" alt="AI 실행 인프라 아키텍처">

    <h5>Background</h5>
    <p>AI 기반 질의응답 시스템을 안정적으로 실행하고 데이터를 체계적으로 저장·검색할 수 있는 인프라가 필요했습니다. 단순 API 호출이 아닌, 재현 가능하고 확장 가능한 실행 환경을 구축하는 것이 목표였습니다.</p>

    <h5>What I Did</h5>
    <h6>인프라 설계 및 구축</h6>
    <ul>
      <li>MCP(Model Context Protocol) 기반 AI 실행 환경 구성</li>
      <li>OpenSearch를 활용한 데이터 인덱싱 및 검색 체계 구축</li>
      <li>S3 기반 데이터 저장소 설계</li>
    </ul>
    <h6>서비스 연동</h6>
    <ul>
      <li>Lambda를 활용한 서버리스 실행 파이프라인 구성</li>
      <li>EC2 기반 상시 운영 환경과 Lambda 이벤트 처리 연결</li>
      <li>각 컴포넌트 간 데이터 흐름 및 연동 구조 설계</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>질의응답 실행과 데이터 저장이 통합된 재현형 AI 인프라 확보</li>
      <li>서버리스 + 상시운영 하이브리드 구조로 비용 효율 달성</li>
      <li>OpenSearch 기반 빠른 데이터 검색 환경 구축</li>
    </ul>
  </div>

  <!-- 프로젝트 4: 글로벌 개발 인프라 (2025.08) -->
  <div class="project-toggle" data-target="#proj-global" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>글로벌 개발 인프라 구축</h4>
    <p class="proj-meta">2025.07 · DevOps · 기여도 100%</p>
    <p class="proj-summary">AWS+온프레미스 하이브리드 인프라 설계·구축과 CI/CD 파이프라인 구축·배포 자동화로 해외 개발자 원격 협업 환경 확립</p>
    <div>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">Route 53</span>
      <span class="tech-tag">ALB</span>
      <span class="tech-tag">EC2</span>
      <span class="tech-tag">Docker</span>
      <span class="tech-tag">Jenkins</span>
      <span class="tech-tag">Slack</span>
      <span class="tech-tag">WireGuard</span>
    </div>
  </div>
  <div id="proj-global" class="project-detail">
    <img src="{{ '/assets/Global_arc.drawio.png' | relative_url }}" alt="글로벌 개발 인프라 아키텍처">

    <h5>Background</h5>
    <p>해외 개발자와의 협업을 위해 AWS와 온프레미스를 연결하는 하이브리드 인프라가 필요했습니다. 개발 환경, 배포 파이프라인, 커뮤니케이션 채널을 하나의 흐름으로 정비하여 원격 협업 효율을 높이는 것이 목표였습니다.</p>

    <h5>What I Did</h5>
    <h6>하이브리드 인프라</h6>
    <ul>
      <li>AWS(Route 53, ALB, EC2)와 온프레미스 서버 간 연동 구조 설계</li>
      <li>Docker 기반 Web / WAS / DB 운영 체계 구성</li>
      <li>WireGuard VPN을 활용한 보안 네트워크 연결</li>
    </ul>
    <h6>CI/CD 및 협업 환경</h6>
    <ul>
      <li>Jenkins 기반 공통 빌드·테스트·배포 파이프라인 구성</li>
      <li>Slack 연동 알림으로 배포 상태 실시간 공유</li>
      <li>해외 개발자 온보딩을 위한 서버 접근, 레포지토리, 배포 절차 문서화</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>하이브리드 인프라 운영 기준 정립</li>
      <li>재현 가능한 배포 및 운영 절차 문서화</li>
      <li>원격·해외 협업 환경의 온보딩 시간 단축</li>
    </ul>
  </div>

  <!-- 프로젝트 5: 모니터링·알림 체계 (2025.06) -->
  <div class="project-toggle" data-target="#proj-monitor" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>블록체인 노드 모니터링 · 알림 체계 구축</h4>
    <p class="proj-meta">2025.06 · SRE · 기여도 100%</p>
    <p class="proj-summary">모니터링·알림 체계 구축으로 관측성(Observability) 확보 — 장애 트러블슈팅 소요 시간 1주일 → 30분 이내 단축 + Slack 실시간 알림 운영</p>
    <div>
      <span class="tech-tag">Prometheus</span>
      <span class="tech-tag">Grafana</span>
      <span class="tech-tag">Alertmanager</span>
      <span class="tech-tag">Blackbox Exporter</span>
      <span class="tech-tag">Slack</span>
    </div>
  </div>
  <div id="proj-monitor" class="project-detail">
    <img src="{{ '/assets/alert_sysytem.drawio.png' | relative_url }}" alt="모니터링·알림 체계 아키텍처">

    <h5>Background</h5>
    <p>블록체인 노드 및 서비스의 가용성을 실시간으로 파악할 수 있는 체계가 부재했습니다. 장애 발생 시 인지까지 시간이 걸렸고, 외부 헬스체크와 내부 지표를 결합한 모니터링 및 즉각 알림이 필요했습니다.</p>

    <h5>What I Did</h5>
    <h6>모니터링 구축</h6>
    <ul>
      <li>Prometheus 기반 메트릭 수집 체계 설계</li>
      <li>Blackbox Exporter를 활용한 외부 헬스체크 구성</li>
      <li>Grafana 대시보드를 통한 운영 가시성 확보</li>
    </ul>
    <h6>알림 체계</h6>
    <ul>
      <li>Alertmanager 규칙 설정 및 알림 라우팅 구성</li>
      <li>Slack 웹훅 연동으로 실시간 장애 알림 구현</li>
      <li>의미 있는 경보만 남기도록 알림 임계값 튜닝</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>장애 트러블슈팅 소요 시간 <strong>1주일 → 30분 이내 단축</strong> (RCA 문서 축적과 병행)</li>
      <li>외부+내부 지표 결합으로 운영 가시성 확보</li>
      <li>필요한 경보만 남기는 효율적 알림 체계 확립</li>
    </ul>
  </div>

  <!-- 프로젝트 6: VM 백업 시스템 (2025.03 ~ 2025.04) -->
  <div class="project-toggle" data-target="#proj-vm-backup" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>VM 서버 백업 시스템 구축</h4>
    <p class="proj-meta">2025.03 ~ 2025.04 · SRE · 기여도 100%</p>
    <p class="proj-summary">ZFS 증분 백업 + UPS 연동 자동 종료로 개발 자산 무손실 보호 체계 확립, 정전 시에도 데이터 안전 보장</p>
    <div>
      <span class="tech-tag">Linux</span>
      <span class="tech-tag">ZFS</span>
      <span class="tech-tag">KVM / Proxmox</span>
      <span class="tech-tag">Shell Script</span>
      <span class="tech-tag">UPS</span>
      <span class="tech-tag">Cron</span>
    </div>
  </div>
  <div id="proj-vm-backup" class="project-detail">
    <img src="{{ '/assets/VM_SERVER.drawio.png' | relative_url }}" alt="VM 백업 시스템 아키텍처">

    <h5>Background</h5>
    <p>온프레미스 서버실의 VM 개발 자산을 보호할 체계가 부재했습니다. 정전, 하드웨어 장애 등에 대비한 자동 백업과 안전한 종료 메커니즘이 필요했습니다.</p>

    <h5>What I Did</h5>
    <h6>백업 체계 구축</h6>
    <ul>
      <li>ZFS 스냅샷 기반 VM 백업 시스템 설계 및 구현</li>
      <li>증분 백업으로 스토리지 효율 최적화</li>
      <li>백업 스케줄링(Cron) 및 이력 관리 자동화</li>
    </ul>
    <h6>재해 방지</h6>
    <ul>
      <li>UPS 연동 자동 종료 체계 구현 (정전 감지 → 안전 셧다운)</li>
      <li>장애 시 스냅샷 기반 복원 절차 수립 및 문서화</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>개발 자산 보호 체계 확립 (자동 백업 + 자동 종료)</li>
      <li>증분 백업으로 스토리지 비용 절감</li>
      <li>장애 발생 시 빠른 복원 가능한 운영 기반 확보</li>
    </ul>
  </div>

  <!-- 프로젝트 8: 블록체인 의약품 관리 시스템 (2024.09 ~ 2025.01) -->
  <div class="project-toggle" data-target="#proj-blockchain" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>블록체인 의약품 관리 시스템 개발</h4>
    <p class="proj-meta">2024.09 ~ 2025.01 · Backend Developer · API 서버 및 관리자 페이지 담당</p>
    <p class="proj-summary">공공API 기반 의약품 데이터 검증 + 블록체인 BaaS 연동 중간 API 서버 구축으로 의약품 이력의 무결성 보장</p>
    <div>
      <span class="tech-tag">Java</span>
      <span class="tech-tag">Spring Boot</span>
      <span class="tech-tag">REST API</span>
      <span class="tech-tag">Blockchain BaaS</span>
      <span class="tech-tag">공공API</span>
      <span class="tech-tag">Batch</span>
      <span class="tech-tag">MariaDB</span>
    </div>
  </div>
  <div id="proj-blockchain" class="project-detail">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 480" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:12px 0;">
      <defs>
        <filter id="bs" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="ah2" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <linearGradient id="bBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="bGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="bOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
        <linearGradient id="bPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
        <linearGradient id="bTeal" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#26A69A"/><stop offset="100%" stop-color="#00897B"/></linearGradient>
      </defs>
      <rect width="920" height="480" fill="#FAFBFC" rx="12"/>
      <text x="460" y="35" text-anchor="middle" font-size="22" font-weight="700" fill="#2C3E50">Blockchain Drug Management System</text>
      <!-- Frontend App -->
      <rect x="40" y="65" width="200" height="65" rx="8" fill="url(#bBlue)" filter="url(#bs)"/>
      <text x="140" y="93" text-anchor="middle" font-size="17" font-weight="600" fill="#fff">Frontend App</text>
      <text x="140" y="114" text-anchor="middle" font-size="13" fill="#D6EAF8">Drug Registration Request</text>
      <!-- Admin Page -->
      <rect x="40" y="160" width="200" height="65" rx="8" fill="url(#bBlue)" filter="url(#bs)"/>
      <text x="140" y="188" text-anchor="middle" font-size="17" font-weight="600" fill="#fff">Admin Dashboard</text>
      <text x="140" y="210" text-anchor="middle" font-size="13" fill="#D6EAF8">Master Data · Batch Monitor</text>
      <!-- Arrow: Frontend → API Server -->
      <path d="M240,97 L340,97" stroke="#7F8C8D" stroke-width="2" marker-end="url(#ah2)"/>
      <text x="290" y="89" text-anchor="middle" font-size="13" fill="#7F8C8D">REST API</text>
      <!-- Arrow: Admin → API Server -->
      <path d="M240,192 L340,155" stroke="#7F8C8D" stroke-width="2" marker-end="url(#ah2)"/>
      <!-- Blockchain API Server -->
      <rect x="345" y="58" width="240" height="150" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
      <text x="465" y="85" text-anchor="middle" font-size="18" font-weight="700" fill="#2C3E50">Blockchain API Server</text>
      <text x="465" y="105" text-anchor="middle" font-size="13" fill="#555">Validation &amp; Relay Gateway</text>
      <rect x="360" y="118" width="105" height="40" rx="6" fill="url(#bGreen)" filter="url(#bs)"/>
      <text x="412" y="137" text-anchor="middle" font-size="14" font-weight="600" fill="#fff">Data Validation</text>
      <text x="412" y="153" text-anchor="middle" font-size="11" fill="#D5F5E3">Public API Verify</text>
      <rect x="475" y="118" width="105" height="40" rx="6" fill="url(#bOrange)" filter="url(#bs)"/>
      <text x="527" y="137" text-anchor="middle" font-size="14" font-weight="600" fill="#fff">Batch Sync</text>
      <text x="527" y="153" text-anchor="middle" font-size="11" fill="#FEF9E7">Scheduled Update</text>
      <!-- Arrow: API Server → 공공API -->
      <path d="M465,208 L465,260" stroke="#7F8C8D" stroke-width="2" marker-end="url(#ah2)"/>
      <text x="490" y="240" font-size="13" fill="#7F8C8D">Query &amp; Verify</text>
      <!-- 공공API -->
      <rect x="355" y="265" width="220" height="60" rx="8" fill="url(#bPurple)" filter="url(#bs)"/>
      <text x="465" y="292" text-anchor="middle" font-size="17" font-weight="600" fill="#fff">Public Drug API</text>
      <text x="465" y="312" text-anchor="middle" font-size="13" fill="#E8DAEF">MFDS Registered Drug Database</text>
      <!-- Arrow: API Server → BaaS -->
      <path d="M585,145 L675,145" stroke="#7F8C8D" stroke-width="2" marker-end="url(#ah2)"/>
      <text x="630" y="135" text-anchor="middle" font-size="13" fill="#7F8C8D">Verified Data</text>
      <!-- Blockchain BaaS -->
      <rect x="680" y="80" width="200" height="120" rx="10" fill="url(#bTeal)" filter="url(#bs)"/>
      <text x="780" y="115" text-anchor="middle" font-size="18" font-weight="700" fill="#fff">Blockchain BaaS</text>
      <text x="780" y="138" text-anchor="middle" font-size="14" fill="#E0F2F1">Distributed Ledger</text>
      <text x="780" y="158" text-anchor="middle" font-size="13" fill="#B2DFDB">Drug Traceability Record</text>
      <!-- DB -->
      <rect x="680" y="255" width="200" height="60" rx="8" fill="#6C757D" filter="url(#bs)"/>
      <text x="780" y="282" text-anchor="middle" font-size="17" font-weight="600" fill="#fff">MariaDB</text>
      <text x="780" y="303" text-anchor="middle" font-size="13" fill="#D5D8DC">Drug Master · Batch History</text>
      <!-- Arrow: API Server → DB -->
      <path d="M540,208 L720,265" stroke="#7F8C8D" stroke-width="1.5" stroke-dasharray="5,3" marker-end="url(#ah2)"/>
      <text x="645" y="232" font-size="12" fill="#7F8C8D">Persist</text>
      <!-- Data Flow Legend -->
      <rect x="40" y="365" width="840" height="100" rx="8" fill="#F8F9FA" stroke="#E9ECEF" stroke-width="1"/>
      <text x="60" y="390" font-size="15" font-weight="700" fill="#2C3E50">Data Flow</text>
      <text x="60" y="413" font-size="14" fill="#555">1. Client → API Server : Drug registration data submitted via REST API</text>
      <text x="60" y="433" font-size="14" fill="#555">2. API Server → Public API : Validate against MFDS registered drug database</text>
      <text x="60" y="453" font-size="14" fill="#555">3. API Server → BaaS : Verified data recorded on blockchain ledger | Batch : Periodic sync from public API</text>
    </svg>

    <h5>Background</h5>
    <p>의약품 유통 이력의 무결성과 투명성을 블록체인으로 보장하는 시스템이 필요했습니다. 프론트엔드 앱에서 등록하는 의약품 데이터가 실제 존재하는 의약품인지 검증하고, 검증된 데이터만 블록체인에 기록하는 중간 API 서버가 핵심이었습니다.</p>

    <h5>What I Did</h5>
    <h6>블록체인 API 서버 (중간 서버)</h6>
    <ul>
      <li>프론트엔드에서 전송된 의약품 데이터를 공공API(식약처)와 대조하여 실제 등록 의약품인지 검증</li>
      <li>검증 통과된 데이터를 블록체인 BaaS 서버로 전송하여 원장에 기록</li>
      <li>Batch 프로세스로 공공API에서 최신 의약품 정보를 주기적으로 동기화·업데이트</li>
      <li>검증 실패 시 에러 핸들링 및 재처리 로직 구현</li>
    </ul>
    <h6>관리자 페이지</h6>
    <ul>
      <li>의약품 마스터 데이터 관리 대시보드 개발</li>
      <li>Batch 실행 이력 조회 및 상태 모니터링</li>
      <li>블록체인 기록 현황 조회 기능</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>공공API 기반 자동 검증으로 허위·미등록 의약품 데이터 블록체인 유입 차단</li>
      <li>Batch 자동 동기화로 의약품 마스터 데이터 최신 상태 유지</li>
      <li>검증→기록의 자동화된 파이프라인으로 수작업 검증 제거</li>
    </ul>
  </div>

</div>

<!-- ====== 업무 스타일 & 방향 ====== -->
<div class="section-title">Work Style</div>

- 문제를 서비스 흐름 전체를 따라가며 원인을 단계적으로 도출
- 임시 복구보다 재발 방지에 중점을 둠
- 반복 작업은 자동화, 운영 절차는 문서화하여 재현 가능한 운영 환경 구축
- 개발·운영·네트워크를 분리하지 않고 하나의 시스템으로 이해

---

<div class="section-title">Contact</div>

<div class="contact-bar">
  <a href="#" class="btn-primary-contact" id="copyEmail" onclick="copyEmail(event)">
    <i class="fa fa-envelope"></i> <span id="emailText">lsfguni@gmail.com</span>
  </a>
  <a href="https://github.com/lsfGuni" target="_blank">
    <i class="fab fa-github"></i> GitHub
  </a>
  <a href="#" onclick="window.print(); return false;">
    <i class="fa fa-print"></i> Print
  </a>
</div>


<script>
  // 펼치기/접기: vanilla JS (이벤트 위임, jQuery 미의존)
  document.addEventListener('click', function(e) {
    var toggle = e.target.closest('.project-toggle');
    if (!toggle) return;

    var targetId = toggle.getAttribute('data-target');
    var target = document.querySelector(targetId);
    if (!target) return;

    var isOpen = toggle.getAttribute('aria-expanded') === 'true';

    if (isOpen) {
      // 닫기
      target.style.display = 'none';
      toggle.setAttribute('aria-expanded', 'false');
    } else {
      // 다른 열린 패널 먼저 닫기 (아코디언)
      document.querySelectorAll('.project-toggle[aria-expanded="true"]').forEach(function(other) {
        var otherId = other.getAttribute('data-target');
        var otherTarget = document.querySelector(otherId);
        if (otherTarget) otherTarget.style.display = 'none';
        other.setAttribute('aria-expanded', 'false');
      });
      // 열기
      target.style.display = 'block';
      toggle.setAttribute('aria-expanded', 'true');
    }
  });

  // 이메일 클립보드 복사
  function copyEmail(e) {
    e.preventDefault();
    var email = 'lsfguni@gmail.com';
    navigator.clipboard.writeText(email).then(function() {
      var el = document.getElementById('emailText');
      el.textContent = '이메일 주소가 복사되었습니다';
      setTimeout(function() { el.textContent = email; }, 2000);
    });
  }
</script>
