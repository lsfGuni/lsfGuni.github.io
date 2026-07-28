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
  /* 인터랙티브 도면 임베드 */
  .demo-embed {
    margin: 12px 0 8px 0;
    border: 1px solid #dee2e6;
    border-radius: 10px;
    overflow: hidden;
    background: #040d1e;
  }
  .demo-embed iframe { display: block; width: 100%; height: 620px; border: 0; }
  .demo-note { font-size: 0.82rem; color: #666; margin: 0 0 14px 2px; line-height: 2.1; }
  .demo-btn {
    display: inline-block;
    padding: 7px 15px;
    margin-left: 4px;
    border-radius: 8px;
    font-size: 0.85rem;
    font-weight: 600;
    text-decoration: none;
    background: #0b1b3a;
    color: #7dd3fc !important;
    border: 1px solid #1e3a6a;
  }
  .demo-btn:hover { background: #12264f; color: #bae6fd !important; text-decoration: none; }
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
  /* 상단 우측 고정 Contact — navbar(fixed-top) 아래로 오프셋 */
  .floating-contact {
    position: fixed;
    top: 68px;
    right: 16px;
    z-index: 1020;
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 6px 8px;
    background: rgba(255, 255, 255, 0.96);
    border: 1px solid #dee2e6;
    border-radius: 24px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
    backdrop-filter: blur(4px);
  }
  .floating-contact a {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 5px 11px;
    border-radius: 18px;
    font-size: 0.8rem;
    font-weight: 500;
    line-height: 1.2;
    white-space: nowrap;
    text-decoration: none;
    color: #333;
    transition: all 0.15s;
  }
  .floating-contact a:hover { background: #f1f5fb; color: #008AFF; text-decoration: none; }
  .floating-contact .fc-primary { background: #008AFF; color: #fff; }
  .floating-contact .fc-primary:hover { background: #0069d9; color: #fff; }
  /* PDF 인쇄용 */
  @media print {
    .intro-header, nav, footer, .contact-bar, .toggle-wrap, .floating-contact { display: none !important; }
    .project-toggle { border: 1px solid #ccc !important; break-inside: avoid; }
    .project-detail { display: block !important; height: auto !important; }
    .project-detail { border: 1px solid #ccc !important; break-inside: avoid; }
    .project-detail svg { max-height: 300px; }
    .demo-embed { display: none !important; }
    .badge-skill, .tech-tag { border: 1px solid #999 !important; }
    body { font-size: 11pt; }
    a { color: #333 !important; text-decoration: none !important; }
    .open-to-work { print-color-adjust: exact; -webkit-print-color-adjust: exact; }
  }
  /* 작은 화면에서는 임베드 대신 새 창 링크만 노출 */
  @media (max-width: 820px) {
    .demo-embed { display: none; }
  }
  /* 좁은 화면에서는 고정 Contact를 숨김 — 하단 Contact 섹션으로 대체 */
  @media (max-width: 767px) {
    .floating-contact { display: none; }
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

<!-- ====== 상단 우측 고정 Contact ====== -->
<div class="floating-contact">
  <a href="#" class="fc-primary" onclick="copyEmail(event)" title="클릭하면 이메일 주소가 복사됩니다">
    <i class="fa fa-envelope"></i> <span class="email-text">lsfguni@gmail.com</span>
  </a>
  <a href="https://github.com/lsfGuni" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> GitHub
  </a>
  <a href="#" onclick="window.print(); return false;" title="이 페이지를 PDF로 저장">
    <i class="fa fa-print"></i> PDF
  </a>
</div>

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
폐쇄망 AI 플랫폼 배포부터 DDoS 3계층 방어, Blue/Green 무중단 배포까지 단독 수행해 온 DevOps 엔지니어
</p>

Spring 백엔드 개발로 시작하여 Linux 서버 구축·운영, 하이브리드 인프라, CI/CD 파이프라인 구축·개선, 모니터링·알림 체계(관측성), 보안 대응까지 확장했습니다. 장애 발생 시 근본 원인 분석(RCA) → 해결 → 고도화 → 문서화까지 이어가며, 재현 가능한 운영 체계를 만듭니다. 사내 AI 에이전트 실행 플랫폼에서는 k3s 클러스터와 ArgoCD GitOps 배포 체계를 직접 구축하며, 실행 1건 = Job 1개로 신뢰할 수 없는 워크로드를 격리하는 인프라를 만들고 있습니다(서비스 오픈 전 단계).

</div>

<!-- ====== 핵심 기술 ====== -->
<div class="section-title">Core Skills</div>

<span class="badge-skill infra">AWS</span>
<span class="badge-skill infra">Route 53 · DNS</span>
<span class="badge-skill infra">CloudFront</span>
<span class="badge-skill infra">ACM</span>
<span class="badge-skill infra">ALB</span>
<span class="badge-skill infra">EC2</span>
<span class="badge-skill infra">ECS (Fargate)</span>
<span class="badge-skill infra">Docker</span>
<span class="badge-skill infra">Kubernetes (k8s)</span>
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
  <strong>Air-gapped / AI Platform</strong> — 폐쇄망(망분리) 환경 AI 서비스 스택 오프라인 배포·기동. deb/wheel/Docker/Yarn Berry 번들링, CPU 아키텍처(ARM↔x86_64) 불일치 해결, 제한된 GPU에서 로컬 서빙과 원격 API 위임을 나누는 워크로드 배치, litellm·watsonx 연동
</div>
<div class="strength-item">
  <strong>CI/CD & Automation</strong> — Jenkins, GitLab CI, Bitbucket Pipelines 기반 CI/CD 파이프라인 구축·개선, CodeDeploy Blue/Green 무중단 배포, 반복 작업 자동화 및 절차 표준화
</div>
<div class="strength-item">
  <strong>Kubernetes &amp; GitOps</strong> — k3s 클러스터 직접 구축(컨트롤플레인·워커 분리), ArgoCD app-of-apps로 루트 1개 + 자식 18개 앱을 Git에서 선언적 관리, 실행 1건 = Job 1개 + 전용 네임스페이스·ServiceAccount·RBAC 격리. 관리형(EKS·GKE)이 아닌 self-managed 기준이며, 서비스 오픈 전 구축 단계
</div>
<div class="strength-item">
  <strong>IaC (전환 진행 중)</strong> — Proxmox 3대 홈랩을 Terraform(VM 프로비저닝) + Ansible(k8s 설치·설정)로 코드화, 명령 두 번으로 클러스터 전체 재현
</div>
<div class="strength-item">
  <strong>Hybrid Infrastructure &amp; FinOps</strong> — AWS + On-Premise 연동 인프라 설계·구축·운영. Route 53, ALB, EC2, ECS, Docker, Nginx 기반 서비스 아키텍처. 클라우드 비용 구조를 근거로 온프레미스 이관을 설계·실행 — 이관 순번을 리스크 기준으로 정하고 롤백 경로를 먼저 확보
</div>
<div class="strength-item">
  <strong>Observability & Reliability</strong> — Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반 모니터링·로깅·알림 체계 구축으로 관측성 확보
</div>
<div class="strength-item">
  <strong>Security & Troubleshooting</strong> — AWS WAF, CloudFront Functions 기반 IP 접근제어, Nginx, iptables 다층 방어. 로그 기반 근본 원인 분석(RCA)과 재발 방지, 금융권 망분리 환경 장애 진단
</div>

<!-- ====== 경력 ====== -->
<div class="section-title">Experience</div>

<div class="exp-card">
  <h4>(주)베리드코리아 <small style="color:#008AFF;">Developer · DevOps · SRE</small></h4>
  <div class="exp-meta">개발팀 / 주임 · 2024.08 ~ Present</div>
  <ul>
    <li>자사 블록체인 서비스(BaaS·Wallet·Scan) AWS·온프레미스 하이브리드 인프라 상시 운영 — 장애 트러블슈팅 1주일 → 30분 단축, 봇 트래픽 하루 평균 1,000+ IP 차단으로 AWS 비용 20%+ 절감</li>
    <li>AWS 비용 절감을 위한 온프레미스 이관(FinOps, 2026.04~): 이관 순번을 리스크 기준으로 설계하고 롤백 경로를 먼저 확보한 뒤 전환 — BaaS API 2노드 이중화 후 실트래픽 전환 완료, 실적 약 20% 절감(1단계 목표 56~70%)</li>
      <li>사내 AI 에이전트 실행 플랫폼 인프라 구축(2026.05~): AI가 스스로 작성한 코드를 안전하게 실행하기 위한 격리 환경 구축 — 실행 1건마다 일회용 컨테이너로 분리하고 외부로 나가는 통신을 차단해 API 키 유출 경로 제거, 쿠버네티스 클러스터 직접 구축 + ArgoCD GitOps 배포 자동화</li>
    <li>하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터(2026.05~07, 완료): 금융권 망분리 환경 SSO·DRM 어댑터 구축, 다단계 연동 구간의 통신 장애 진단 및 다자간 업무 조율</li>
    <li>삼성디스플레이 폐쇄망 AI 플랫폼 구축(2026.05~06): USB 단방향 반입 환경에 AI 서비스 5종 배포, "내부에서는 빌드하지 않는다"로 전략 전환해 반입-배포 1사이클 5시간+ → 30분 단축, 9월 후속 단계 확정</li>
    <li>KBS 재난방송 STG 인프라(2026.04~06): 검증 환경이 없던 대국민 서비스에 AWS CLI로 운영 구성을 확인해 동등한 스테이징 신규 구축 — ECS Fargate·CodeDeploy Blue/Green, CloudFront 7경로 분기, IAM 최소권한, PRD-STG 대조 검증 불일치 0건</li>
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
    <p class="proj-summary">자사 서비스(BaaS·Wallet·Scan)를 AWS + 온프레미스 이중화로 상시 운영 — 트러블슈팅 1주일 → 30분, 봇 트래픽 일평균 1,000+ IP 자동 차단. 현재는 <strong>AWS 월 고정비 절감을 위한 온프레미스 이관(FinOps)</strong>을 단계적으로 진행 중 — 실적 약 20% 절감, 1단계 목표 56~70%</p>
    <div>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">EC2</span>
      <span class="tech-tag">RDS</span>
      <span class="tech-tag">OpenSearch</span>
      <span class="tech-tag">Route 53</span>
      <span class="tech-tag">Nginx</span>
      <span class="tech-tag">On-Premise</span>
      <span class="tech-tag">Blockchain Node</span>
      <span class="tech-tag">FinOps</span>
      <span class="tech-tag">WireGuard VPN</span>
      <span class="tech-tag">systemd</span>
    </div>
  </div>
  <div id="proj-berith-ops" class="project-detail">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 762" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
      <defs>
        <filter id="brShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="brArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <marker id="brArrowR" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#C0392B"/></marker>
        <linearGradient id="brBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="brGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="brOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
        <linearGradient id="brRed" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#D9534F"/><stop offset="100%" stop-color="#C0392B"/></linearGradient>
        <linearGradient id="brGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
        <linearGradient id="brPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
      </defs>
      <rect width="920" height="762" fill="#FAFBFC" rx="12"/>
      <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Berith 하이브리드 인프라 — AWS + 온프레미스 상시 운영</text>

      <rect x="48" y="50" width="200" height="50" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="148" y="72" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">BaaS 기업 고객 (B2B)</text>
      <text x="148" y="88" text-anchor="middle" font-size="9" fill="#DDE1E3">보안서약서 · 물품관리 이력 기록</text>

      <rect x="262" y="50" width="200" height="50" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="362" y="72" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Wallet · Scan 사용자 (B2C)</text>
      <text x="362" y="88" text-anchor="middle" font-size="9" fill="#DDE1E3">코인 지갑 · 블록체인 익스플로러</text>

      <rect x="476" y="50" width="230" height="50" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
      <text x="591" y="72" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">무차별 대입 · 봇 트래픽</text>
      <text x="591" y="88" text-anchor="middle" font-size="9" fill="#FADBD8">지갑 특성상 계정 탈취 시도 상시 유입</text>

      <rect x="720" y="50" width="152" height="50" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="796" y="70" text-anchor="middle" font-size="11" font-weight="700" fill="#fff">트러블슈팅 소요</text>
      <text x="796" y="88" text-anchor="middle" font-size="11" font-weight="700" fill="#fff">1주일 → 30분 이내</text>

      <path d="M148,100 L148,124" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
      <path d="M362,100 L362,124" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
      <path d="M591,100 L591,124" stroke="#C0392B" stroke-width="2" marker-end="url(#brArrowR)"/>

      <rect x="30" y="130" width="860" height="96" rx="10" fill="#FDEDEC" stroke="#E6B0AA" stroke-width="1.5"/>
      <text x="46" y="150" font-size="11" font-weight="700" fill="#943126">3계층 방어 — 단일 IP 차단으로 시작해 다수 IP 로테이션 공격에 맞춰 단계적으로 고도화</text>

      <rect x="48" y="160" width="200" height="52" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
      <text x="148" y="183" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">AWS WAF</text>
      <text x="148" y="200" text-anchor="middle" font-size="9" fill="#FADBD8">엣지 단 규칙 차단</text>
      <path d="M248,186 L266,186" stroke="#C0392B" stroke-width="2" marker-end="url(#brArrowR)"/>

      <rect x="271" y="160" width="200" height="52" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
      <text x="371" y="183" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Nginx</text>
      <text x="371" y="200" text-anchor="middle" font-size="9" fill="#FADBD8">요청 패턴 · 경로 기반 차단</text>
      <path d="M471,186 L489,186" stroke="#C0392B" stroke-width="2" marker-end="url(#brArrowR)"/>

      <rect x="494" y="160" width="212" height="52" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
      <text x="600" y="183" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">iptables</text>
      <text x="600" y="200" text-anchor="middle" font-size="9" fill="#FADBD8">하루 평균 1,000개+ IP 자동 차단</text>

      <rect x="726" y="160" width="146" height="52" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="799" y="181" text-anchor="middle" font-size="11.5" font-weight="700" fill="#fff">AWS 비용 20%↓</text>
      <text x="799" y="199" text-anchor="middle" font-size="9" fill="#DFF0D8">일 50GB 공격 로그 대응</text>

      <path d="M460,226 L460,248" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
      <rect x="360" y="252" width="200" height="46" rx="8" fill="url(#brPurple)" filter="url(#brShadow)"/>
      <text x="460" y="273" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Route 53</text>
      <text x="460" y="290" text-anchor="middle" font-size="9" fill="#E8DAEF">AWS ↔ 온프레미스 요청 라우팅</text>

      <path d="M400,298 L280,322" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
      <path d="M520,298 L680,322" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>

      <rect x="40" y="330" width="470" height="152" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
      <text x="56" y="350" font-size="11" font-weight="700" fill="#1B4F72">AWS — EC2 7대 · RDS · OpenSearch</text>

      <rect x="56" y="360" width="140" height="44" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
      <text x="126" y="380" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">부트노드 2대</text>
      <text x="126" y="395" text-anchor="middle" font-size="9" fill="#D6EAF8">피어 탐색</text>

      <rect x="206" y="360" width="140" height="44" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
      <text x="276" y="380" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">메인넷 노드</text>
      <text x="276" y="395" text-anchor="middle" font-size="9" fill="#D6EAF8">자체 이더리움 계열 체인</text>

      <rect x="356" y="360" width="140" height="44" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
      <text x="426" y="380" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Web / WAS</text>
      <text x="426" y="395" text-anchor="middle" font-size="9" fill="#D6EAF8">Docker 컨테이너 운영</text>

      <rect x="56" y="414" width="215" height="44" rx="7" fill="url(#brOrange)" filter="url(#brShadow)"/>
      <text x="163" y="434" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">RDS</text>
      <text x="163" y="449" text-anchor="middle" font-size="9" fill="#FDF2E0">서비스 데이터</text>

      <rect x="281" y="414" width="215" height="44" rx="7" fill="url(#brOrange)" filter="url(#brShadow)"/>
      <text x="388" y="434" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">OpenSearch</text>
      <text x="388" y="449" text-anchor="middle" font-size="9" fill="#FDF2E0">체인 데이터 인덱싱 · Scan 연동</text>

      <rect x="530" y="330" width="350" height="152" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
      <text x="546" y="350" font-size="11" font-weight="700" fill="#186A3B">온프레미스 — 이중화 구간</text>

      <rect x="546" y="360" width="160" height="44" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="626" y="380" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">이중화 서버</text>
      <text x="626" y="395" text-anchor="middle" font-size="9" fill="#DFF0D8">AWS 비용 절감 목적 이관</text>

      <rect x="716" y="360" width="148" height="44" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="790" y="380" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">메인넷 노드</text>
      <text x="790" y="395" text-anchor="middle" font-size="9" fill="#DFF0D8">BaaS 요청 전담</text>

      <rect x="546" y="414" width="318" height="44" rx="7" fill="#FFFFFF" stroke="#A9DFBF" stroke-width="1.2"/>
      <text x="558" y="431" font-size="9.5" fill="#186A3B">대규모 트랜잭션 유입 시 반복되던 노드 다운 — 디스크 I/O 병목 +</text>
      <text x="558" y="447" font-size="9.5" fill="#186A3B">체인 데이터 용량 부족으로 특정 → BaaS 요청 분산 (Wallet은 AWS 유지)</text>

      <rect x="30" y="498" width="860" height="86" rx="10" fill="#FEF9E7" stroke="#F7DC6F" stroke-width="1.5"/>
      <text x="46" y="518" font-size="11" font-weight="700" fill="#9A7D0A">관측성 — 외부 헬스체크와 내부 지표를 결합</text>

      <rect x="48" y="528" width="185" height="40" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="140" y="553" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Blackbox Exporter</text>
      <path d="M233,548 L251,548" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>

      <rect x="256" y="528" width="200" height="40" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="356" y="553" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Prometheus · Grafana</text>
      <path d="M456,548 L474,548" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>

      <rect x="479" y="528" width="185" height="40" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="571" y="553" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Alertmanager</text>
      <path d="M664,548 L682,548" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>

      <rect x="687" y="528" width="185" height="40" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="779" y="547" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">Slack 실시간 알림</text>
      <text x="779" y="561" text-anchor="middle" font-size="8.5" fill="#DFF0D8">대응 가능한 경보만 남김</text>

      <rect x="30" y="598" width="860" height="146" rx="10" fill="#EAF2F8" stroke="#85C1E9" stroke-width="1.5"/>
      <text x="46" y="618" font-size="11" font-weight="700" fill="#1A5276">진행 중 — AWS 월 고정비 절감을 위한 온프레미스 이관 (FinOps) · 실적 약 20% 절감 / 1단계 목표 56~70%</text>

      <rect x="48" y="628" width="256" height="36" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="176" y="651" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">BaaS API — 실트래픽 전환 완료</text>

      <rect x="316" y="628" width="268" height="36" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
      <text x="450" y="651" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">캐시 · 스캔 · 검색엔진 · 스토리지 이관</text>

      <rect x="596" y="628" width="274" height="36" rx="7" fill="url(#brOrange)" filter="url(#brShadow)"/>
      <text x="733" y="651" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">지갑 — 이관·검증 완료, 전환 대기</text>

      <rect x="48" y="672" width="400" height="36" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
      <text x="248" y="695" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">WAS 계열 17개 · RDB 3종 · 블록체인 노드 — 미착수</text>

      <rect x="460" y="672" width="410" height="36" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
      <text x="665" y="695" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">정리한 AWS 리소스 — EC2 3대 정지 · 탄력 IP 3개 반납</text>

      <text x="46" y="722" font-size="9.5" fill="#1A5276">웹 계층은 의도적으로 AWS 유지 — DNS·로드밸런서를 그대로 두고 업스트림 한 줄만 바꾸므로 전환과 롤백이 설정 수준으로 축소되고, 서비스별 점진 전환이 가능</text>
      <text x="46" y="738" font-size="9.5" fill="#943126">순절감(TCO)은 전력·하드웨어 감가 미반영으로 아직 미산정 — 남은 과제로 관리 중</text>
    </svg>
    <h5>Background</h5>
    <p>기업용 블록체인 기록 서비스 <strong>BaaS</strong>(삼성디스플레이 보안서약서, 롯데이노베이츠 물품관리 이력)와 B2C 서비스(<strong>Berith Wallet·Berith Scan</strong>)를 AWS와 온프레미스를 연동한 하이브리드 구성으로 상시 운영합니다. 부트노드 2대·메인넷 노드(이더리움 계열 자체 메인넷) 포함 EC2 7대, RDS, OpenSearch(체인 데이터 인덱싱), 온프레미스 이중화 서버로 구성되며, 지갑 서비스 특성상 <strong>계정 탈취를 노리는 무차별 대입·봇 공격이 상시 유입</strong>되는 환경입니다.</p>

    <h5>What I Did</h5>
    <ul>
      <li>메인넷·부트노드 노드 운영, Nginx 웹 계층(Route 53 기반 AWS·온프레미스 요청 라우팅) 운영</li>
      <li>모니터링·알림 체계 구축과 장애별 RCA 문서화 — "뭔가 안 된다" 수준의 신고에서 시작하던 트러블슈팅을 체계화</li>
      <li>단일 봇 차단 후 다수 IP가 로테이션하며 공격하는 패턴으로 진화하자 WAF·Nginx·iptables 3계층 차단 룰을 단계적으로 고도화</li>
      <li>메인넷 노드 다운의 근본 원인을 디스크 I/O 병목 + 체인 데이터 용량 부족으로 특정 — EBS 증설과 함께, 장비 증설 없이 BaaS 요청을 온프레미스 메인넷으로 분산(Wallet은 AWS 유지)하는 구조 변경으로 해소</li>
    </ul>

    <h5>현재 진행 과제 — AWS 비용 절감을 위한 온프레미스 이관 (FinOps)</h5>
    <p>매월 고정 지출되는 AWS 비용을 줄이기 위해 사내 유휴 물리 서버(20코어 2대)로 워크로드를 단계적으로 이관하고 있습니다. <strong>현재 실적은 약 20% 절감, 1단계 완료 시 목표는 56~70%</strong>이며 실적과 목표를 분리해 관리합니다.</p>
    <h6>설계 판단</h6>
    <ul>
      <li><strong>쿠버네티스 계획을 중단하고 VM + systemd를 채택</strong> — 대상 서비스가 실시간 고객 트래픽을 받고 있었고, 한 호스트는 가용 RAM 6GB 수준이라 컨트롤플레인 오버헤드(약 4GB)를 흡수할 여력이 없었음. <strong>더 나은 방식이 아니라 지금 자원과 리스크 조건에서 실행 가능한 방식</strong>을 택하되, Dockerfile·매니페스트는 미리 준비해 이후 systemd를 Pod로 교체만 하면 되는 상태로 유지</li>
      <li><strong>이관 순번을 세 기준으로 결정</strong> — ① 상태 의존도가 낮은 것부터 ② <strong>의존성 역방향</strong>(의존하는 쪽을 먼저 옮겨 클라우드에 남은 자원을 참조하게 함 — 반대는 불가) ③ 원본 호스트 부하가 위험 수준인 서비스는 순번을 앞당김</li>
      <li><strong>웹 계층은 의도적으로 AWS에 유지</strong> — DNS·로드밸런서를 그대로 두고 업스트림만 바꾸므로 전환·롤백이 설정 한 줄 수준으로 축소되고 서비스별 점진 전환이 가능. 최종 진입점이 사내 회선이 되면 회선 장애가 곧 서비스 장애가 된다는 점도 고려</li>
      <li><strong>되돌릴 경로를 남긴 채 전환</strong> — 원본 인스턴스를 삭제하지 않고 정지 상태로 보존해 업스트림 원복만으로 30초 내 복귀 가능</li>
    </ul>
    <h6>검증 기준을 "떴다"가 아니라 "이전과 같다"로 설정</h6>
    <ul>
      <li>재빌드하지 않고 바이너리 복사 후 <strong>sha256 전량 대조</strong> — 재빌드하면 브랜치 변동으로 두 노드가 다른 코드를 돌 수 있기 때문. JDK 빌드 문자열·systemd 유닛 해시·기동 시간(143초 vs 144초)까지 대조</li>
      <li><strong>분산 락 소유자 식별자를 0.3초 간격으로 추적</strong>해 두 노드가 실제로 작업 파티션을 나눠 갖는지 실측(60초간 36:36 균등). 한쪽만 재기동시켜 식별자 하나만 바뀌는 것으로 노드를 확정하는 교차검증 사용</li>
      <li><strong>장애를 실제로 유발해 확인</strong> — 2노드 중 1대 정지 후 30건 요청 전부 정상(5건은 웹 계층이 실패를 감지해 다른 노드로 자동 재시도), 프로세스 강제 종료 후 <strong>2분 34초 만에 자동 복구</strong></li>
    </ul>
    <h6>트러블슈팅 — 캐시의 성격을 다시 규정해 이중화를 하지 않기로 판단</h6>
    <p>소스 코드를 읽어 보니 이 캐시는 데이터 저장소가 아니라 <strong>분산 락 코디네이터</strong>였습니다. 락 백엔드를 standalone·Redis·ZooKeeper 중에서 고를 수 있게 설계돼 있었고, ZooKeeper와 교체 가능한 자리는 데이터 저장소가 아닙니다. 실측에서도 저장된 키는 0개, 락 키만 수백 ms 단위로 생겼다 사라졌습니다.</p>
    <ul>
      <li>영속 데이터가 없으므로 <strong>데이터를 옮기지 않고</strong> IP를 승계시켜 애플리케이션 설정 변경·재시작 없이 전환</li>
      <li>온라인 스냅샷 → 가동 중 대용량 복사 → 정지 후 변경분만 전송의 2단계 설계로 <strong>실제 중단 약 2분</strong></li>
      <li>중단 시 애플리케이션이 fail-safe로 동작함을 <strong>코드로 먼저 확인</strong> — 락을 얻지 못하면 아무것도 처리하지 않음. 블록체인 전송에서 "멈춤"은 복구 가능하지만 "중복 전송"은 되돌릴 수 없으므로 올바른 방향</li>
      <li><strong>이중화는 의도적으로 하지 않음</strong> — 비동기 복제 HA를 락에 붙이면 마스터 장애 시 복제 전 락 정보가 유실돼 두 노드가 같은 파티션을 동시 처리할 수 있음. 가용성을 올리려다 정합성을 깨는 교환이라 판단하고, <strong>"안 죽게"가 아니라 "빨리 살아나게"</strong>(호스트 분리 + 자동 기동 + 프로세스 자동 재시작)에 투자</li>
    </ul>
    <h6>트러블슈팅 — 이중화가 드러낸 설정 불일치</h6>
    <p>BaaS API를 2노드로 이중화한 직후 신규 노드에서 트랜잭션 처리가 8분간 멈췄습니다. 스레드 덤프에서 스케줄러가 카운트다운 래치에 대기 중이었고, 소켓은 특정 블록체인 노드로 SYN-SENT 3건이 응답 없이 매달려 있었습니다. 원인은 <strong>기존 노드에만 존재하던 DNAT 규칙</strong>이었습니다.</p>
    <ul>
      <li>같은 조사에서 <strong>신규 노드에 기존 노드의 방화벽 정책이 적용되지 않아 서비스 포트가 외부에 노출될 수 있는 상태</strong>임을 발견. 원격 작업이라 <strong>240초 자동 롤백 타이머를 먼저 걸고</strong> 허용 목록 적용 → 외부 도달성 검증 → 타이머 취소 순서로 잠금 사고를 예방</li>
      <li><strong>연결 타임아웃과 래치 타임아웃이 모두 없어</strong> 블록체인 노드 하나가 응답을 멈추면 인스턴스의 트랜잭션 처리기 전체가 정지하고, 그 사이 락 자동 갱신이 끊겨 다른 노드가 같은 파티션을 가져가는 동시 처리 창이 열린다는 구조적 결함을 확인 — 코드 수정 과제로 등록하고 기존 문서의 "해당 노드 ping 실패는 서비스 영향 없음" 판단을 정정</li>
      <li><strong>복제했다고 믿은 노드가 실제로는 동일하지 않았습니다.</strong> 애플리케이션 아티팩트는 해시까지 대조했지만 OS 계층 설정은 비교 대상에서 빠져 있었습니다 — 이중화하지 않았다면 두 문제 모두 드러나지 않았을 것</li>
    </ul>
    <h6>호스트 자원 병목 — 증설을 기다리지 않고 재배치로 해소</h6>
    <p>한 물리 호스트가 RAM 62GB 중 55GB 사용에 스왑까지 진입해 가용 5.9GB였습니다. 문서상 선결 조건은 "메모리 증설"이었지만 두 호스트의 가용 RAM이 5.9GB와 90GB로 심하게 불균형했기 때문에, <strong>증설을 기다리는 대신 재배치를 먼저 택했습니다.</strong> 캐시·VPN·홈페이지 3대를 여유 호스트로 옮겨 <strong>가용 RAM 5.9GB → 22GB(약 3.7배) 회복</strong>, 캐시가 앱 노드와 같은 호스트에 있어 동시 장애 지점이 되던 문제도 함께 해소했습니다.</p>
    <h6>현재 상태</h6>
    <ul>
      <li><strong>실트래픽 전환 완료 — BaaS API</strong>: 웹 계층 2대의 업스트림이 온프레미스 2노드로 균등 분산되는 것을 실측 확인</li>
      <li><strong>이관·가동 완료</strong>: 캐시, 스캔(API·Web·Batch), 검색엔진, 오브젝트 스토리지</li>
      <li><strong>전환 대기</strong>: 지갑 — 이관·검증 완료, QA 통과 후 트래픽 전환 예정</li>
      <li><strong>미착수</strong>: WAS 계열 약 17개, RDB 3종, 블록체인 노드</li>
      <li><strong>정리한 AWS 리소스</strong>: EC2 3대 정지, 탄력 IP 3개 반납(삭제는 후속 단계로 보류)</li>
      <li><strong>남은 과제</strong>: 순절감(TCO)에 전력·하드웨어 감가가 미반영 상태 — 절감률만 보면 과대평가될 수 있어 산정 보완을 과제로 관리 중. 온프레미스 노드의 모니터링 편입, 전사 runbook 정비도 미완</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>장애 트러블슈팅 소요 시간 <strong>1주일 → 30분 이내 단축</strong></li>
      <li>봇 트래픽 <strong>하루 평균 1,000개 이상 IP 자동 차단</strong>, <strong>AWS 비용 20% 이상 절감</strong></li>
      <li>장비 증설 없이 구조 변경만으로 I/O 병목 해소</li>
    </ul>
  </div>

  <!-- 프로젝트 0-0b: AI 에이전트 실행 플랫폼 (진행 중) -->
  <div class="project-toggle" data-target="#proj-ai-agent" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>🤖 AI 에이전트 실행 플랫폼 — Kubernetes 격리 실행 인프라 (구축 중)</h4>
    <p class="proj-meta">2026.05 ~ 진행 중 · 사내 프로젝트 · 클러스터 구축·GitOps 배포 파이프라인 담당 · 서비스 오픈 전 단계</p>
    <p class="proj-summary">삼성 폐쇄망 POC에서 드러난 "에이전트가 자기 실행 환경을 수정하는" 문제를 풀기 위해, 실행 1건 = Job 1개로 격리하는 k3s 인프라를 구축 중. ArgoCD app-of-apps로 루트 1 + 자식 18개 앱 선언적 배포</p>
    <div>
      <span class="tech-tag">Kubernetes (k3s)</span>
      <span class="tech-tag">ArgoCD (app-of-apps)</span>
      <span class="tech-tag">Helm</span>
      <span class="tech-tag">NetworkPolicy</span>
      <span class="tech-tag">RBAC</span>
      <span class="tech-tag">Linkerd (mTLS)</span>
      <span class="tech-tag">Harbor</span>
      <span class="tech-tag">OpenTelemetry</span>
    </div>
  </div>
  <div id="proj-ai-agent" class="project-detail">
    <h5>Background</h5>
    <p><strong>삼성디스플레이 폐쇄망 POC에서 이어진 과제입니다.</strong> 그때 DevAX는 격리 인프라 없이 systemd로 구동했는데, 에이전트가 호스트 파일을 건드려 자기 실행 환경을 망가뜨리는 일이 발생했습니다. 에이전트에는 모델 API 키와 사내 서비스 토큰이 주입되기 때문에, <strong>실행 단위를 격리하는 sandbox 인프라가 필요했습니다.</strong></p>

    <h5>What I Did</h5>
    <ul>
      <li><strong>k3s 클러스터 직접 구축</strong> — 사내 VM에 컨트롤플레인·워커를 분리 구성, 기본 traefik을 ingress-nginx로 교체하고 Linkerd 서비스 메시로 서비스 간 mTLS 적용</li>
      <li><strong>에이전트 실행 1건 = Job 1개</strong>로 격리 — 전용 네임스페이스(<code>agent-jobs</code>)와 전용 ServiceAccount를 부여하고, Job 생성 시 <code>backoffLimit=0</code>(실패 재시도 없음) · <code>activeDeadlineSeconds</code>(무한 대기 차단) · <code>ttlSecondsAfterFinished</code>(완료 Job 자동 정리)를 지정</li>
      <li><strong>egress NetworkPolicy 적용 후 트러블슈팅</strong> — 화이트리스트에 Linkerd 컨트롤 플레인 포트(destination 8086 / policy 8090 / identity 8080)를 넣지 않아 사이드카가 막히며 컨트롤러가 hang → liveness 실패 → <code>Exit 137</code>(SIGKILL). 원인을 추적해 <strong>재활성 조건(Linkerd 3포트 + OTel 4317 + JWKS)을 문서화</strong>하고, 현재는 비활성 상태로 관리 중</li>
      <li><strong>ArgoCD app-of-apps GitOps</strong> — 루트 Application 1개가 자식 18개를 관리하고, Helm 차트 14종을 Git 단일 소스에서 선언적 배포. Bitbucket Pipelines + self-hosted runner 연동</li>
      <li>레지스트리 3종(Harbor·Kellnr·Verdaccio)을 전량 self-host하고, OpenTelemetry·Tempo로 분산 트레이싱 구성. 설계 판단은 ADR 28건으로 문서화</li>
    </ul>

    <h5>인터랙티브 아키텍처 도면 (직접 제작)</h5>
    <p>클러스터 구조를 설명하고 진행 상황을 공유하기 위해 직접 만든 아이소메트릭 도면입니다. 상단 6개 모드(<strong>일반 K8s · DevAX 구조 · 자연어 실행 · Sandbox · GitOps · 관측성</strong>)로 관점을 바꿔 볼 수 있고, 컴포넌트를 클릭하면 역할 설명이 나옵니다. <strong>구현 완료 / 스캐폴드 / 목표</strong>를 색으로 구분해 진행 상황을 있는 그대로 표시합니다.</p>
    <div class="demo-embed">
      <iframe src="{{ '/assets/diagrams/k8s-iso-city.html' | relative_url }}" title="DevAX Kubernetes 인프라 아이소메트릭 도면" loading="lazy"></iframe>
    </div>
    <p class="demo-note">드래그로 시점 이동 · 컴포넌트 클릭 시 상세 설명 · 1~6 키로 모드 전환(전체 화면 권장)
      <a class="demo-btn" href="{{ '/assets/diagrams/k8s-iso-city.html' | relative_url }}" target="_blank" rel="noopener">🖥️ 전체 화면으로 열기</a>
    </p>

    <h5>현재 상태 — 서비스 오픈 전 단계입니다</h5>
    <ul>
      <li><strong>에이전트 실행 1차 관통 완료</strong> (2026-05-29) — 자동 검증 23종 전체 통과</li>
      <li><strong>egress NetworkPolicy는 위 사유로 현재 비활성</strong> — 재활성 조건을 정의해 두고 관리 중</li>
      <li><strong>실격리(microVM)와 사용자 화면은 미착수</strong> — 현재는 네임스페이스·RBAC 수준의 논리 격리까지이며, 컨테이너 탈출까지 막는 실격리는 다음 과제로 리스크에 명시 관리 중</li>
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
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 500" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
      <defs>
        <filter id="hnShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="hnArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <marker id="hnArrowP" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7B5BA6"/></marker>
        <linearGradient id="hnBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="hnGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="hnGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
        <linearGradient id="hnPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
      </defs>
      <rect width="920" height="500" fill="#FAFBFC" rx="12"/>
      <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">금융권 망분리 다단계 연동 — 구간별 검증으로 원인 구간 특정</text>

      <rect x="30" y="48" width="860" height="150" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
      <text x="46" y="68" font-size="11" font-weight="700" fill="#1B4F72">연동 경로 — 구간마다 담당 업체가 모두 다르고, 어느 한 곳도 전체 흐름을 알지 못하는 상태</text>

      <rect x="44" y="80" width="152" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
      <text x="120" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Dooray</text>
      <text x="120" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">외부망 그룹웨어 SaaS</text>
      <text x="120" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">그룹웨어사</text>
      <path d="M198,108 L218,108" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="222" y="80" width="122" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
      <text x="283" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">VPN</text>
      <text x="283" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">망 간 통신 구간</text>
      <text x="283" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">VPN 업체</text>
      <path d="M346,108 L366,108" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="370" y="80" width="152" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
      <text x="446" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">하나증권 인프라</text>
      <text x="446" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">DNS · 방화벽 · HA 구성</text>
      <text x="446" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">인프라팀 · HA 업체</text>
      <path d="M524,108 L544,108" stroke="#7B5BA6" stroke-width="2" marker-end="url(#hnArrowP)"/>

      <rect x="548" y="76" width="176" height="64" rx="8" fill="url(#hnPurple)" stroke="#5B3E85" stroke-width="2.5" filter="url(#hnShadow)"/>
      <text x="636" y="100" text-anchor="middle" font-size="12.5" font-weight="700" fill="#fff">SSO · DRM 어댑터</text>
      <text x="636" y="117" text-anchor="middle" font-size="9" fill="#E8DAEF">설치 · 구동 스크립트 구축</text>
      <text x="636" y="131" text-anchor="middle" font-size="9" fill="#E8DAEF">Spring Boot</text>
      <text x="636" y="152" text-anchor="middle" font-size="9.5" font-weight="700" fill="#6C3483">본인 담당 구간</text>
      <path d="M726,108 L746,108" stroke="#7B5BA6" stroke-width="2" marker-end="url(#hnArrowP)"/>

      <rect x="750" y="80" width="126" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
      <text x="813" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">내부 SSO·DRM</text>
      <text x="813" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">사내 애플리케이션</text>
      <text x="813" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">솔루션사</text>

      <text x="46" y="184" font-size="9.5" fill="#1B4F72">전체 흐름을 아는 주체가 없으니 장애가 나면 "우리 쪽은 문제 없다"에서 멈춘다 — 그래서 구간을 잘라 증거를 만드는 방식을 택했습니다</text>

      <rect x="30" y="214" width="860" height="132" rx="10" fill="#F4ECF7" stroke="#BB8FCE" stroke-width="1.5"/>
      <text x="46" y="234" font-size="11" font-weight="700" fill="#6C3483">구간별 검증 사이클 — 원인이 좁혀질 때까지 반복</text>

      <rect x="48" y="246" width="160" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
      <text x="128" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">① 설정 파일 확인</text>
      <text x="128" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">각 주체별 구성 대조</text>
      <path d="M208,270 L226,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="230" y="246" width="140" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
      <text x="300" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">② 테스트 요청</text>
      <text x="300" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">구간 단위로 발신</text>
      <path d="M370,270 L388,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="392" y="246" width="140" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
      <text x="462" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">③ 로그 분석</text>
      <text x="462" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">도달 여부 확인</text>
      <path d="M532,270 L550,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="554" y="246" width="150" height="48" rx="7" fill="url(#hnPurple)" filter="url(#hnShadow)"/>
      <text x="629" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">④ 원인 구간 특정</text>
      <text x="629" y="282" text-anchor="middle" font-size="9" fill="#E8DAEF">증거 확보</text>
      <path d="M704,270 L722,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

      <rect x="726" y="246" width="146" height="48" rx="7" fill="url(#hnGreen)" filter="url(#hnShadow)"/>
      <text x="799" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">⑤ 조치 요청</text>
      <text x="799" y="282" text-anchor="middle" font-size="9" fill="#DFF0D8">해당 업체에 근거 제시</text>

      <path d="M799,294 L799,314 L128,314 L128,296" stroke="#7B5BA6" stroke-width="1.8" stroke-dasharray="5 4" fill="none" marker-end="url(#hnArrowP)"/>
      <text x="460" y="330" text-anchor="middle" font-size="9.5" fill="#6C3483">미해결이면 다음 구간으로 이동해 다시 반복 — 주간 정례 미팅으로 다자간 일정·이슈 조율</text>

      <rect x="30" y="362" width="860" height="118" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
      <text x="46" y="382" font-size="11" font-weight="700" fill="#186A3B">적용 사례 — 서버 권한이 제한된 환경에서 비침습적 진단으로 근거 확보</text>
      <text x="46" y="404" font-size="9.5" fill="#145A32">운영 서버 SSO 초기화 실패 → 어댑터 로그에서 연결 실패 지점 확인 → 이름 해석과 포트 도달을 각각 분리해 검증 →</text>
      <text x="46" y="421" font-size="9.5" fill="#145A32">DNS 미해석 + 방화벽 미개방 두 가지로 원인을 나누어 특정 → 각 담당팀에 필요한 조치를 근거와 함께 요청</text>
      <text x="46" y="448" font-size="11" font-weight="700" fill="#1E8449">결과 — 전 테스트 통과, 잔여 이슈 없이 2026.07.15 정상 오픈 (일정 지연 없음)</text>
      <text x="46" y="468" font-size="9.5" fill="#145A32">애플리케이션 · OS · 네트워크를 관통하는 통신 구조 분석과, 여러 업체가 얽힌 장애의 진단·조율 프로세스를 경험</text>
    </svg>
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
    <h4>🔒 삼성디스플레이 폐쇄망 AI 플랫폼 구축 (AI POC)</h4>
    <p class="proj-meta">2026.05 ~ 2026.06 · 폐쇄망 인프라 단독 담당 (인프라 1인 / 총 5인)</p>
    <p class="proj-summary">인터넷 차단 + USB 단방향 반입(반출 불가) 환경에 AI 서비스 5종 배포. "내부에서는 빌드하지 않는다"로 전략을 바꿔 반입-배포 1사이클 5시간+ → 30분 단축, 9월 후속 단계 확정</p>
    <div>
      <span class="tech-tag">Air-gapped</span>
      <span class="tech-tag">litellm</span>
      <span class="tech-tag">IBM watsonx</span>
      <span class="tech-tag">WrenAI</span>
      <span class="tech-tag">STT 로컬 서빙</span>
      <span class="tech-tag">Docker (multi-arch)</span>
      <span class="tech-tag">systemd</span>
      <span class="tech-tag">GPU / CUDA</span>
      <span class="tech-tag">Yarn Berry</span>
      <span class="tech-tag">Linux</span>
    </div>
  </div>
  <div id="proj-sdc-poc" class="project-detail">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 600" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
      <defs>
        <filter id="agShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="agArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <marker id="agArrowR" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#C0392B"/></marker>
        <linearGradient id="agBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="agGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="agOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
        <linearGradient id="agPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
        <linearGradient id="agGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
        <linearGradient id="agTeal" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3AAFA9"/><stop offset="100%" stop-color="#2B8A85"/></linearGradient>
      </defs>
      <rect width="920" height="600" fill="#FAFBFC" rx="12"/>
      <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">폐쇄망 AI 플랫폼 — 반입 파이프라인 · 서비스 구성</text>

      <rect x="30" y="48" width="860" height="112" rx="10" fill="#FFF7E6" stroke="#F0AD4E" stroke-width="1.5" stroke-dasharray="6 4"/>
      <text x="46" y="68" font-size="11" font-weight="700" fill="#B9770E">외부 인터넷 구간 (사외)</text>
      <rect x="55" y="80" width="205" height="62" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
      <text x="157" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">개인 로컬 PC</text>
      <text x="157" y="124" text-anchor="middle" font-size="10" fill="#DDE1E3">사외 반출 후 LTE 테더링으로 빌드</text>
      <path d="M262,111 L306,111" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <rect x="315" y="80" width="255" height="62" rx="8" fill="url(#agOrange)" filter="url(#agShadow)"/>
      <text x="442" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">즉시 구동 이미지 · 오프라인 번들 빌드</text>
      <text x="442" y="124" text-anchor="middle" font-size="10" fill="#FDF2E0">타깃 아키텍처 linux/amd64 명시</text>
      <path d="M572,111 L616,111" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <rect x="625" y="80" width="230" height="62" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
      <text x="740" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">USB 적재 · 물리 반입</text>
      <text x="740" y="124" text-anchor="middle" font-size="10" fill="#DDE1E3">단방향 — 한 번 들어가면 반출 불가</text>

      <path d="M20,182 L900,182" stroke="#C0392B" stroke-width="2" stroke-dasharray="8 5"/>
      <text x="30" y="176" font-size="11" font-weight="700" fill="#C0392B">에어갭 경계</text>
      <text x="898" y="176" text-anchor="end" font-size="10.5" fill="#C0392B">번들 누락 1건 = 사이클 전체 재실행 → “내부에서는 빌드하지 않는다”</text>
      <path d="M740,144 L740,202" stroke="#C0392B" stroke-width="2" marker-end="url(#agArrowR)"/>

      <rect x="30" y="208" width="700" height="360" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
      <text x="46" y="228" font-size="11" font-weight="700" fill="#1B4F72">폐쇄망 워크스테이션 1대 · GPU 16GB VRAM</text>

      <rect x="48" y="246" width="118" height="44" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
      <text x="107" y="273" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">사용자</text>
      <path d="M107,292 L107,324" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

      <rect x="48" y="330" width="118" height="58" rx="8" fill="url(#agPurple)" filter="url(#agShadow)"/>
      <text x="107" y="354" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">DevAX</text>
      <text x="107" y="371" text-anchor="middle" font-size="9.5" fill="#E8DAEF">프런트엔드 · 진입점</text>

      <path d="M168,359 L184,359" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M184,266 L184,422" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M184,266 L196,266" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <path d="M184,318 L196,318" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <path d="M184,370 L196,370" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <path d="M184,422 L196,422" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

      <rect x="200" y="244" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
      <text x="315" y="263" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">WrenAI</text>
      <text x="315" y="279" text-anchor="middle" font-size="9.5" fill="#D6EAF8">SQL 분석·질의 자동생성 · systemd</text>
      <rect x="200" y="296" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
      <text x="315" y="315" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">보안성검토 에이전트</text>
      <text x="315" y="331" text-anchor="middle" font-size="9.5" fill="#D6EAF8">애플리케이션 보안성 검토 · systemd</text>
      <rect x="200" y="348" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
      <text x="315" y="367" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">ai-gateway</text>
      <text x="315" y="383" text-anchor="middle" font-size="9.5" fill="#D6EAF8">문서 업로드 기반 보안성 검토 · systemd</text>
      <rect x="200" y="400" width="230" height="44" rx="7" fill="url(#agGray)" filter="url(#agShadow)"/>
      <text x="315" y="419" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">chat-bot</text>
      <text x="315" y="435" text-anchor="middle" font-size="9.5" fill="#DDE1E3">현장 개발 서비스 — watsonx 연동·배포 담당 · Docker</text>

      <path d="M432,266 L448,266" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M432,318 L448,318" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M432,370 L448,370" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M432,422 L448,422" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M448,266 L448,432" stroke="#7F8C8D" stroke-width="2"/>
      <path d="M448,306 L466,306" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <path d="M448,432 L466,432" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

      <rect x="468" y="276" width="162" height="60" rx="8" fill="url(#agOrange)" filter="url(#agShadow)"/>
      <text x="549" y="301" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">litellm 게이트웨이</text>
      <text x="549" y="319" text-anchor="middle" font-size="9.5" fill="#FDF2E0">모델 호출 단일 창구</text>

      <rect x="468" y="402" width="162" height="60" rx="8" fill="url(#agGreen)" filter="url(#agShadow)"/>
      <text x="549" y="427" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">STT 서빙 (로컬 GPU)</text>
      <text x="549" y="445" text-anchor="middle" font-size="9.5" fill="#DFF0D8">유일한 자체 서빙 모델</text>

      <text x="46" y="497" font-size="10" fill="#1B4F72">DevAX·WrenAI·보안성검토·ai-gateway = systemd 서비스 · chat-bot = Docker 컨테이너 (모든 의존성 포함 이미지)</text>
      <text x="46" y="524" font-size="10" fill="#7B5BA6">※ POC 시점 DevAX는 격리 인프라 없이 systemd 구동 — 여기서 드러난 “에이전트가 자기 실행 환경을 수정” 문제가</text>
      <text x="46" y="540" font-size="10" fill="#7B5BA6">   이후 사내 Kubernetes 샌드박스(실행 1건 = Job 1개) 구축의 출발점이 됨</text>

      <rect x="752" y="208" width="148" height="360" rx="10" fill="#F4F6F7" stroke="#B2BABB" stroke-width="1.5" stroke-dasharray="6 4"/>
      <text x="768" y="228" font-size="11" font-weight="700" fill="#566573">협력사망</text>
      <text x="768" y="244" font-size="9.5" fill="#7F8C8D">스위치 허브 연동</text>
      <path d="M632,306 L764,306" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
      <rect x="768" y="266" width="116" height="80" rx="8" fill="url(#agTeal)" filter="url(#agShadow)"/>
      <text x="826" y="300" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">IBM watsonx</text>
      <text x="826" y="318" text-anchor="middle" font-size="9.5" fill="#D6F0EE">LLM 추론 API</text>

      <text x="460" y="588" text-anchor="middle" font-size="10.5" fill="#566573">GPU 16GB 제약 → LLM 추론은 전량 watsonx API로 위임하고, GPU는 STT 전용으로 배분</text>
    </svg>

    <h5>Background</h5>
    <p>인터넷·패키지 저장소·CI/CD가 모두 없는 삼성디스플레이 폐쇄망에 AI 서비스 5종(DevAX 멀티 에이전트 플랫폼, WrenAI, 보안성검토 에이전트, ai-gateway, chat-bot)과 litellm 게이트웨이를 구동해야 했습니다. 1사이클은 빌드 → USB 적재 → 물리 반입 → 기동인데, USB는 한 번 반입하면 반출할 수 없습니다. 기동 단계에서 번들 누락이 발견되면 사외로 나가 처음부터 다시 돌려야 했고, 초기에는 한 사이클에 5시간 이상이 걸렸습니다. 사전 조사도 제한돼 워크스테이션 사양을 미리 확인할 수 없었고, 결정적으로 개발 환경(ARM)과 실제 배정된 워크스테이션(x86_64)의 CPU 아키텍처가 달랐다는 사실이 반입 후에야 드러났습니다.</p>

    <h5>What I Did</h5>
    <ul>
      <li><strong>"내부에서 빌드하지 않는다"로 전략 전환</strong> — 실패 비용이 비대칭인 환경에서는 내부 빌드가 최대 리스크였습니다. 외부에서 <strong>모든 의존성이 포함된 즉시 구동 가능한 이미지</strong>를 완성해 반입하고, 내부 작업은 적재·기동만 남기는 방식으로 바꿔 1사이클을 <strong>최소 30분</strong>까지 단축</li>
      <li><strong>CPU 아키텍처 불일치 규명·해결</strong> — ARM에서 빌드한 컨테이너 이미지와 wheel은 x86_64에서 실행 자체가 불가능(<code>exec format error</code>)합니다. 이를 원인으로 특정하고 <strong>타깃 아키텍처(linux/amd64)를 명시해 전 산출물을 재빌드</strong></li>
      <li><strong>16GB VRAM 한 장에 맞춘 워크로드 배치</strong> — 5개 서비스의 모델을 모두 로컬에 올릴 수 없어, <strong>LLM 추론은 전량 watsonx API로 위임하고 GPU는 STT 전용으로 배분</strong>. litellm을 모델 호출 단일 창구로 두어 서비스별 연동 코드를 분리</li>
      <li><strong>서비스 성격에 맞춘 배포 방식 선택</strong> — 상시 기동이 필요한 4종(DevAX·WrenAI·보안성검토·ai-gateway)은 systemd 서비스로, 현장 개발자가 만들던 chat-bot은 컨테이너로 배포하고 <strong>watsonx 연동을 담당</strong></li>
      <li>외부 빌드 환경조차 제공되지 않아 <strong>개인 장비를 사외로 반출해 LTE 테더링으로 빌드</strong>하는 방식으로 반입 파이프라인을 유지. Yarn Berry 기반 프런트엔드 오프라인 빌드, deb/wheel 오프라인 번들링으로 의존성을 사전 확보</li>
      <li>도입에 회의적이던 현장 이해관계자와 <strong>신뢰 관계를 먼저 구축</strong>하고, 고객사 PM·기존 개발진 사이의 커뮤니케이션을 조율하여 프로젝트를 정상 궤도로 복원</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li><strong>POC 완료</strong> — 전 서비스 정상 동작 시연, 고객사 임원 보고 긍정 평가로 <strong>2026년 9월 후속 단계 진행 확정</strong></li>
      <li>반입-배포 1사이클 <strong>5시간+ → 30분 (약 90% 단축)</strong></li>
      <li>폐쇄망 AI 서비스 5종 + 게이트웨이 전체를 <strong>단독으로 배포·기동</strong></li>
      <li><strong>다음 프로젝트의 출발점을 만듦</strong> — 이 POC에서 DevAX는 격리 인프라 없이 systemd로 구동했는데, 여기서 <strong>에이전트가 자기 실행 환경을 수정하는 문제</strong>가 드러났고, 이 경험이 사내 Kubernetes 샌드박스 구축으로 이어졌습니다</li>
    </ul>
  </div>

  <!-- 프로젝트 0-3: KBS 재난방송 STG 인프라 (2026.04 ~ 2026.06) -->
  <div class="project-toggle" data-target="#proj-kbs-stg" aria-expanded="false">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span></span>
    <h4>📡 KBS 통합재난방송시스템 STG 인프라 구축</h4>
    <p class="proj-meta">2026.04 ~ 2026.06 · 인프라 설계·구축 단독 (1인)</p>
    <p class="proj-summary">운영만 있고 검증 환경이 없던 대국민 서비스에, AWS CLI로 운영 구성을 확인해 가며 동등한 스테이징을 신규 구축. ECS Fargate·CodeDeploy Blue/Green, CloudFront 7경로 분기, IAM 최소권한. PRD-STG 전 항목을 CLI로 대조 검증해 불일치 0건으로 인계</p>
    <div>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">ECS Fargate</span>
      <span class="tech-tag">ECR</span>
      <span class="tech-tag">ALB</span>
      <span class="tech-tag">CodeDeploy</span>
      <span class="tech-tag">Blue/Green</span>
      <span class="tech-tag">CloudFront</span>
      <span class="tech-tag">CloudFront Functions</span>
      <span class="tech-tag">WAF</span>
      <span class="tech-tag">Route 53</span>
      <span class="tech-tag">ACM</span>
      <span class="tech-tag">S3</span>
      <span class="tech-tag">DynamoDB</span>
      <span class="tech-tag">IAM</span>
      <span class="tech-tag">AWS CLI</span>
      <span class="tech-tag">Jenkins</span>
    </div>
  </div>
  <div id="proj-kbs-stg" class="project-detail">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 700" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
      <defs>
        <filter id="kbShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
        <marker id="kbArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
        <marker id="kbArrowG" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#449D44"/></marker>
        <linearGradient id="kbBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
        <linearGradient id="kbGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
        <linearGradient id="kbOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
        <linearGradient id="kbPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
        <linearGradient id="kbGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
        <linearGradient id="kbTeal" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3AAFA9"/><stop offset="100%" stop-color="#2B8A85"/></linearGradient>
      </defs>
      <rect width="920" height="700" fill="#FAFBFC" rx="12"/>
      <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">KBS 재난방송 STG — 운영 환경과 동등하게 구축한 스테이징</text>

      <rect x="30" y="48" width="860" height="122" rx="10" fill="#F4ECF7" stroke="#BB8FCE" stroke-width="1.5"/>
      <text x="46" y="68" font-size="11" font-weight="700" fill="#6C3483">진입 계층 — 단일 도메인</text>

      <rect x="48" y="80" width="140" height="58" rx="8" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="118" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">사용자 · 개발팀</text>
      <text x="118" y="124" text-anchor="middle" font-size="9.5" fill="#DDE1E3">대국민 재난 페이지</text>
      <path d="M188,109 L206,109" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

      <rect x="211" y="80" width="180" height="58" rx="8" fill="url(#kbPurple)" filter="url(#kbShadow)"/>
      <text x="301" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">Route 53</text>
      <text x="301" y="124" text-anchor="middle" font-size="9.5" fill="#E8DAEF">STG 도메인 Alias 레코드</text>
      <path d="M391,109 L409,109" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

      <rect x="414" y="80" width="205" height="58" rx="8" fill="url(#kbPurple)" filter="url(#kbShadow)"/>
      <text x="516" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">CloudFront</text>
      <text x="516" y="124" text-anchor="middle" font-size="9.5" fill="#E8DAEF">동작(behavior) 7개 경로 분기</text>

      <path d="M619,98 L640,92" stroke="#7F8C8D" stroke-width="1.5" stroke-dasharray="4 3" marker-end="url(#kbArrow)"/>
      <path d="M619,120 L640,137" stroke="#7F8C8D" stroke-width="1.5" stroke-dasharray="4 3" marker-end="url(#kbArrow)"/>

      <rect x="644" y="72" width="228" height="40" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
      <text x="758" y="90" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">CloudFront Functions</text>
      <text x="758" y="105" text-anchor="middle" font-size="9" fill="#D4EFEC">IP 허용목록 — WAF 제약의 대체 구현</text>

      <rect x="644" y="118" width="228" height="40" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
      <text x="758" y="136" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">ACM 인증서</text>
      <text x="758" y="151" text-anchor="middle" font-size="9" fill="#D4EFEC">와일드카드 1레벨 매칭 실증 검증</text>

      <rect x="30" y="186" width="860" height="176" rx="10" fill="#E8F6F3" stroke="#A2D9CE" stroke-width="1.5"/>
      <text x="46" y="206" font-size="11" font-weight="700" fill="#117A65">콘텐츠 분기 — 한 도메인에서 3개 서비스가 병행 (총 7개 경로)</text>

      <rect x="48" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="143" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">v1 기본 경로</text>
      <text x="143" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">정적 페이지</text>
      <path d="M143,264 L143,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
      <rect x="48" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
      <text x="143" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 버킷</text>
      <text x="143" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">정적 오리진</text>

      <rect x="252" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="347" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">v2 (Next.js)</text>
      <text x="347" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">신규 프런트</text>
      <path d="M347,264 L347,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
      <rect x="252" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
      <text x="347" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 버킷</text>
      <text x="347" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">빌드 산출물</text>

      <rect x="456" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="551" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">별도 포털</text>
      <text x="551" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">독립 콘텐츠 영역</text>
      <path d="M551,264 L551,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
      <rect x="456" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
      <text x="551" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 버킷</text>
      <text x="551" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">포털 오리진</text>

      <rect x="660" y="220" width="210" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="765" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">API · 동적 요청</text>
      <text x="765" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">애플리케이션 처리</text>
      <path d="M765,264 L765,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
      <rect x="660" y="294" width="210" height="46" rx="7" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
      <text x="765" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">ALB로 전달</text>
      <text x="765" y="331" text-anchor="middle" font-size="9" fill="#D6EAF8">아래 실행 계층으로</text>

      <text x="46" y="354" font-size="9.5" fill="#117A65">S3 4버킷 — 경로별 오리진을 CloudFront 동작 규칙으로 분기해 운영과 동일한 구조로 재현</text>

      <rect x="30" y="378" width="860" height="190" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
      <text x="46" y="398" font-size="11" font-weight="700" fill="#1B4F72">실행 · 무중단 배포</text>

      <rect x="48" y="412" width="200" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
      <text x="148" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">ALB</text>
      <text x="148" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">이중 리스너 443 / 444</text>
      <path d="M248,440 L266,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

      <rect x="271" y="412" width="155" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
      <text x="348" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">타겟그룹 2조</text>
      <text x="348" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Blue / Green</text>
      <path d="M426,440 L444,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

      <rect x="449" y="412" width="198" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
      <text x="548" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">ECS Fargate</text>
      <text x="548" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">운영 태스크 정의와 동일 구성</text>
      <path d="M647,440 L663,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

      <rect x="665" y="412" width="205" height="56" rx="8" fill="url(#kbOrange)" filter="url(#kbShadow)"/>
      <text x="767" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">DynamoDB 3테이블</text>
      <text x="767" y="455" text-anchor="middle" font-size="9.5" fill="#FDF2E0">GSI 포함 · 키 스키마 복원</text>

      <rect x="48" y="496" width="150" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
      <text x="123" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Jenkins</text>
      <text x="123" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">배포 파이프라인</text>
      <path d="M198,520 L216,520" stroke="#449D44" stroke-width="2" marker-end="url(#kbArrowG)"/>

      <rect x="221" y="496" width="140" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
      <text x="291" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">ECR</text>
      <text x="291" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">이미지 저장소</text>
      <path d="M361,520 L379,520" stroke="#449D44" stroke-width="2" marker-end="url(#kbArrowG)"/>

      <rect x="384" y="496" width="205" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
      <text x="486" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">CodeDeploy</text>
      <text x="486" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">Blue/Green — 리스너 전환으로 무중단</text>
      <path d="M486,496 L486,480 L348,480 L348,470" stroke="#449D44" stroke-width="1.8" stroke-dasharray="5 4" fill="none" marker-end="url(#kbArrowG)"/>

      <rect x="665" y="496" width="205" height="48" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
      <text x="767" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">IAM 최소권한</text>
      <text x="767" y="532" text-anchor="middle" font-size="9" fill="#DDE1E3">STG 전용 역할 · 운영은 조회만</text>

      <rect x="30" y="584" width="860" height="102" rx="10" fill="#FEF9E7" stroke="#F7DC6F" stroke-width="1.5"/>
      <text x="46" y="604" font-size="11" font-weight="700" fill="#9A7D0A">제약 조건 아래에서 내린 판단 3건</text>
      <text x="46" y="625" font-size="9.5" fill="#5D4E07">① ACM 와일드카드가 한 레벨만 매칭한다는 점(RFC 6125)을 실제 인증서로 검증해 인증서 추가 발급 비용을 사전 차단</text>
      <text x="46" y="643" font-size="9.5" fill="#5D4E07">② 계정 분리 대신 단일 계정 + 네이밍·태그 분리로 cross-account 관리 부담 제거</text>
      <text x="46" y="661" font-size="9.5" fill="#5D4E07">③ WAF를 붙일 수 없는 요금제 제약은 CloudFront Functions로 IP 접근제어를 대체 구현</text>
      <text x="46" y="681" font-size="9.5" font-weight="600" fill="#1E8449">PRD–STG 전 항목 CLI 대조 검증 — 불일치 0건</text>
    </svg>
    <h5>Background</h5>
    <p>재난 유형별 페이지를 제공하는 대국민 서비스인데 검증 환경 없이 운영만 존재해, 프론트 변경도 백엔드 배포도 운영에서 직접 확인해야 했습니다. 운영 담당자로부터 "운영 환경은 구축되어 있으나 스테이징이 없어 지금 구축하려 한다"는 현황을 전달받아 착수했고, 상세 구성 문서는 없는 상태여서 AWS CLI로 실제 리소스를 확인해 가며 동등한 환경을 재현하는 것이 과제였습니다.</p>

    <h5>What I Did</h5>
    <ul>
      <li><strong>운영 환경 구성 파악</strong> — AWS CLI로 리소스를 전수 조회해 ECS 태스크 정의·ALB 리스너·CloudFront 동작·DynamoDB 키 스키마·VPC 서브넷 구성을 복원하고, 이를 기준으로 구축 순서를 설계</li>
      <li><strong>ECS Fargate + CodeDeploy Blue/Green 무중단 배포 구축</strong> — ALB 이중 리스너·타겟그룹 2조·ECR 연동, Jenkins 배포 파이프라인 동작까지 검증</li>
      <li><strong>CloudFront 7개 경로 분기 구성</strong> — v1·v2(Next.js)·별도 포털이 한 도메인에서 병행되는 구조를 그대로 재현(S3 4버킷 + ALB 라우팅), DynamoDB 3테이블(GSI 포함)·IP 화이트리스트 접근제어 구성</li>
      <li><strong>비용과 제약이 걸린 판단 3건을 근거로 결정</strong> — ACM 와일드카드가 한 레벨만 매칭한다는 점(RFC 6125)을 실제 인증서로 검증해 <strong>인증서 추가 발급 비용을 사전 차단</strong>, 계정 분리 대신 <strong>단일 계정 + 네이밍·태그 분리</strong>로 cross-account 관리 부담 제거, WAF를 붙일 수 없는 요금제 제약은 <strong>CloudFront Functions로 IP 접근제어를 대체 구현</strong></li>
      <li><strong>IAM 최소권한 설계</strong> — STG 전용 역할을 분리해, 개발자가 <strong>운영 리소스는 조회만 가능</strong>하도록 통제</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li><strong>STG 전 리소스 구축 완료</strong> — PRD-STG 전 항목을 CLI로 대조 검증, <strong>불일치 0건</strong></li>
      <li><strong>운영에서 직접 배포를 검증하던 구조를 제거</strong> — 개발팀이 안전하게 테스트할 환경 확보</li>
      <li>구축 가이드·체크리스트·인계 문서로 <strong>담당자가 바뀌어도 이어갈 수 있는 상태</strong> 유지</li>
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
    <i class="fa fa-envelope"></i> <span class="email-text">lsfguni@gmail.com</span>
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

  // 이메일 클립보드 복사 — 상단 고정 Contact와 하단 Contact 양쪽에서 호출
  function copyEmail(e) {
    e.preventDefault();
    var email = 'lsfguni@gmail.com';
    var link = e.target.closest('a');
    var el = link ? link.querySelector('.email-text') : null;

    function done() {
      if (!el) return;
      var prev = el.textContent;
      el.textContent = '복사되었습니다';
      setTimeout(function() { el.textContent = prev; }, 2000);
    }

    if (navigator.clipboard && window.isSecureContext) {
      navigator.clipboard.writeText(email).then(done);
    } else {
      // 클립보드 API를 쓸 수 없는 환경 대비 (구형 브라우저 등)
      var ta = document.createElement('textarea');
      ta.value = email;
      ta.style.position = 'fixed';
      ta.style.opacity = '0';
      document.body.appendChild(ta);
      ta.select();
      try { document.execCommand('copy'); done(); } catch (err) { /* 복사 실패 시 무시 */ }
      document.body.removeChild(ta);
    }
  }
</script>
