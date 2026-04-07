---
layout: page
title: 한권희 | System Engineer · DevOps
subtitle: 자동화와 근본 원인 해결로 안정적인 인프라를 만드는 엔지니어
---

<style>
  /* 헤더 타이틀 크기 축소 */
  .intro-header .page-heading h1 { font-size: 1.6rem; }
  .intro-header .page-heading .page-subheading { font-size: 1rem; }

  .profile-summary { margin-bottom: 2rem; }
  .badge-skill {
    display: inline-block;
    padding: 4px 12px;
    margin: 3px 4px;
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
    padding: 12px 20px;
    margin: 6px 8px;
    border: 1px solid #dee2e6;
    border-radius: 10px;
    min-width: 130px;
  }
  .stat-box .stat-num { font-size: 1.4rem; font-weight: 700; color: #008AFF; }
  .stat-box .stat-label { font-size: 0.8rem; color: #666; margin-top: 2px; }
  .exp-card {
    border-left: 3px solid #008AFF;
    padding: 12px 16px;
    margin-bottom: 16px;
    background: #fafbfc;
    border-radius: 0 8px 8px 0;
  }
  .exp-card h4 { margin: 0 0 4px 0; font-size: 1.05rem; }
  .exp-card .exp-meta { font-size: 0.85rem; color: #666; margin-bottom: 6px; }
  .exp-card ul { margin: 4px 0 0 0; padding-left: 18px; font-size: 0.9rem; }
  .project-toggle {
    cursor: pointer;
    padding: 16px 20px;
    margin-bottom: 8px;
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
    margin: 2rem 0 1rem 0;
  }
  .strength-item { margin-bottom: 10px; }
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
  <span class="open-to-work">DevOps / SRE 포지션에 관심이 있습니다</span>
</div>

<div style="text-align:center; margin-bottom: 1.2rem;">
  <div class="stat-box">
    <div class="stat-num">2년 5개월+</div>
    <div class="stat-label">총 경력</div>
  </div>
  <div class="stat-box">
    <div class="stat-num">7개</div>
    <div class="stat-label">프로젝트</div>
  </div>
  <div class="stat-box">
    <div class="stat-num">DevOps · SRE</div>
    <div class="stat-label">현재 역할</div>
  </div>
</div>

<p class="hook-text" style="text-align:center;">
하이브리드 인프라 설계부터 DDoS 3계층 방어, Blue/Green 무중단 배포까지<br>
2년차에 독립 설계·구축·운영한 엔지니어
</p>

백엔드 개발로 시작하여 **Linux 서버 운영, 하이브리드 인프라, CI/CD, 모니터링, 보안 대응**까지 확장했습니다.  
문제 발생 시 **원인 분석 → 해결 → 고도화 → 문서화**까지 이어가며, 재현 가능한 운영 체계를 만듭니다.

</div>

<!-- ====== 핵심 기술 ====== -->
<div class="section-title">Core Skills</div>

<span class="badge-skill infra">AWS</span>
<span class="badge-skill infra">Route 53</span>
<span class="badge-skill infra">ALB</span>
<span class="badge-skill infra">EC2</span>
<span class="badge-skill infra">Docker</span>
<span class="badge-skill infra">Linux</span>
<span class="badge-skill infra">Nginx</span>
<span class="badge-skill">Jenkins</span>
<span class="badge-skill">GitLab CI</span>
<span class="badge-skill">Bitbucket Pipelines</span>
<span class="badge-skill monitor">Prometheus</span>
<span class="badge-skill monitor">Grafana</span>
<span class="badge-skill monitor">Alertmanager</span>
<span class="badge-skill monitor">CloudWatch</span>
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
  <strong>Hybrid Infrastructure</strong> — AWS + On-Premise 연동 인프라 설계·운영. Route 53, ALB, EC2, Docker, Nginx 기반 서비스 구조
</div>
<div class="strength-item">
  <strong>Automation & CI/CD</strong> — Jenkins, GitLab CI, Bitbucket Pipelines 기반 배포 자동화. 반복 작업 스크립트화 및 절차 표준화
</div>
<div class="strength-item">
  <strong>Monitoring & Reliability</strong> — Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반 모니터링·알림 체계 구축
</div>
<div class="strength-item">
  <strong>Security & Troubleshooting</strong> — AWS WAF, Nginx, iptables 다층 방어. 로그 분석으로 장애 원인 추적 및 재발 방지
</div>

<!-- ====== 경력 ====== -->
<div class="section-title">Experience</div>

<div class="exp-card">
  <h4>베리드코리아 <small style="color:#008AFF;">Developer · DevOps · SRE</small></h4>
  <div class="exp-meta">개발팀 / 주임 · 2024.08 ~ Present</div>
  <ul>
    <li>AWS + 온프레미스 하이브리드 인프라 운영 표준화 → 팀 누구나 동일한 절차로 배포·운영 가능</li>
    <li>AWS WAF + Nginx + iptables 3계층 방어 체계 구축 → 비정상 트래픽 선제 차단, API 장애 제로화</li>
    <li>Prometheus/Grafana 모니터링 + Slack 알림 → 장애 인지 시간 대폭 단축</li>
    <li>Jenkins 기반 CI/CD + Blue/Green 무중단 배포 → 서비스 중단 없는 배포 체계 확립</li>
    <li>온프레미스 서버실 구축, VM 백업·복원 자동화 → 개발 자산 보호 체계 확립</li>
    <li>MCP + OpenSearch + Lambda 기반 AI 실행 인프라 → 재현 가능한 질의응답 파이프라인 구축</li>
    <li>삼성SDR 파견(2025.09~2026.03): 내방객 관리시스템 풀스택 개발 + 카드사 연동 API 자동화</li>
  </ul>
</div>

<div class="exp-card">
  <h4>아이뱅크컨설턴츠 <small style="color:#008AFF;">Developer</small></h4>
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

  <!-- 프로젝트 1: VM 관리 웹페이지 (2026.04 ~ 진행중) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-vm-web" aria-expanded="false" aria-controls="proj-vm-web">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
    <h4>온프레미스 VM 관리 웹페이지</h4>
    <p class="proj-meta">2026.04 ~ 진행중 · 설계 및 개발 전체 · 기여도 100%</p>
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
  <div id="proj-vm-web" class="collapse project-detail" data-parent="#projectAccordion">
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

  <!-- 프로젝트 2: 삼성SDR (2025.09 ~ 2026.03) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-sdr" aria-expanded="false" aria-controls="proj-sdr">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
    <h4>삼성SDR 내방객 관리시스템</h4>
    <p class="proj-meta">2025.09 ~ 2026.03 · Full-Stack Developer · 배포 담당</p>
    <p class="proj-summary">수기 출입 관리를 웹 시스템으로 전환. 카드사 연동 API로 발급·회수 자동화, JBoss 배포 전략으로 운영 안정화 달성</p>
    <div>
      <span class="tech-tag">Java</span>
      <span class="tech-tag">Spring MVC</span>
      <span class="tech-tag">JSP</span>
      <span class="tech-tag">JavaScript</span>
      <span class="tech-tag">JBoss</span>
      <span class="tech-tag">REST API</span>
    </div>
  </div>
  <div id="proj-sdr" class="collapse project-detail" data-parent="#projectAccordion">
    <h5>Background</h5>
    <p>삼성SDR 사업장에서 내방객 출입을 수기/반자동 관리하던 방식을 개선하기 위해, 등록부터 카드 발급, 출입 이력까지 통합된 웹 관리시스템이 필요했습니다.</p>

    <h5>What I Did</h5>
    <h6>Backend 개발</h6>
    <ul>
      <li>Spring MVC 패턴 기반 서버 아키텍처 설계 및 구현</li>
      <li>카드연동 API 설계·개발 (카드 발급/회수 상태 동기화)</li>
      <li>내방객 등록, 조회, 승인, 이력 관리 핵심 비즈니스 로직</li>
    </ul>
    <h6>Frontend 개발</h6>
    <ul>
      <li>JSP 기반 사용자 화면 개발</li>
      <li>JavaScript 동적 UI 처리 및 유효성 검증</li>
    </ul>
    <h6>배포 및 서버 운영</h6>
    <ul>
      <li>JBoss 웹서버 설정 및 환경 구성</li>
      <li>배포 전략 수립, 절차 문서화, 안정화</li>
    </ul>

    <h5>Outcome</h5>
    <ul>
      <li>카드사 연동 API로 내방객 출입 관리 자동화</li>
      <li>안정적 배포 전략으로 서비스 운영 안정화</li>
      <li>수기 관리 대비 내방객 처리 효율 대폭 향상</li>
    </ul>
  </div>

  <!-- 프로젝트 2: DDoS (2025.08) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-ddos" aria-expanded="false" aria-controls="proj-ddos">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
    <h4>DDoS 대응체계 구축</h4>
    <p class="proj-meta">2025.08 · SRE · 기여도 100%</p>
    <p class="proj-summary">Cloud-Web-WAS 3계층 방어 체계 구축으로 비정상 트래픽 선제 차단, 핵심 API 장애율 제로화 및 클라우드 비용 절감 달성</p>
    <div>
      <span class="tech-tag">AWS WAF</span>
      <span class="tech-tag">ALB</span>
      <span class="tech-tag">CloudWatch</span>
      <span class="tech-tag">Nginx</span>
      <span class="tech-tag">iptables</span>
      <span class="tech-tag">Shell Script</span>
    </div>
  </div>
  <div id="proj-ddos" class="collapse project-detail" data-parent="#projectAccordion">
    <img src="{{ '/assets/ddos_arc.drawio.png' | relative_url }}" alt="DDoS 3계층 방어 아키텍처">

    <h5>Background</h5>
    <p>분산된 L7 공격으로 비정상 요청이 급증하여 WAS CPU 상승, 로그인 지연, 트래픽 비용 증가 문제가 발생했습니다. 단일 지점 차단만으로는 대응이 어려워 Cloud-Web-WAS 다층 방어가 필요했습니다.</p>

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
      <li>비정상 트래픽을 WAS 도달 전 선제 차단</li>
      <li>핵심 API 무장애 안정화</li>
      <li>봇/스캐너 요청으로 인한 클라우드 비용 감소</li>
      <li>재사용 가능한 방어 패턴 확보</li>
    </ul>
  </div>

  <!-- 프로젝트 3: AI 실행 인프라 (2025.08) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-ai" aria-expanded="false" aria-controls="proj-ai">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
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
  <div id="proj-ai" class="collapse project-detail" data-parent="#projectAccordion">
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

  <!-- 프로젝트 4: 모니터링·알림 체계 (2025.06) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-monitor" aria-expanded="false" aria-controls="proj-monitor">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
    <h4>블록체인 노드 모니터링 · 알림 체계 구축</h4>
    <p class="proj-meta">2025.06 · SRE · 기여도 100%</p>
    <p class="proj-summary">장애 인지·대응 시간을 대폭 단축한 경량 모니터링 + Slack 실시간 알림 체계 구축</p>
    <div>
      <span class="tech-tag">Prometheus</span>
      <span class="tech-tag">Grafana</span>
      <span class="tech-tag">Alertmanager</span>
      <span class="tech-tag">Blackbox Exporter</span>
      <span class="tech-tag">Slack</span>
    </div>
  </div>
  <div id="proj-monitor" class="collapse project-detail" data-parent="#projectAccordion">
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
      <li>장애 탐지 및 대응 시간 대폭 단축</li>
      <li>외부+내부 지표 결합으로 운영 가시성 확보</li>
      <li>필요한 경보만 남기는 효율적 알림 체계 확립</li>
    </ul>
  </div>

  <!-- 프로젝트 6: VM 백업 시스템 (2025.03 ~ 2025.04) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-vm-backup" aria-expanded="false" aria-controls="proj-vm-backup">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
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
  <div id="proj-vm-backup" class="collapse project-detail" data-parent="#projectAccordion">
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

  <!-- 프로젝트 7: 글로벌 개발 인프라 (2024.07) -->
  <div class="project-toggle" data-toggle="collapse" data-target="#proj-global" aria-expanded="false" aria-controls="proj-global">
    <span class="toggle-wrap"><span class="toggle-arrow">▼</span> <span class="toggle-text">펼치기</span></span>
    <h4>글로벌 개발 인프라 구축</h4>
    <p class="proj-meta">2024.07 · DevOps · 기여도 100%</p>
    <p class="proj-summary">AWS+온프레미스 하이브리드 인프라와 CI/CD 파이프라인을 구축하여 해외 개발자 원격 협업 환경 확립</p>
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
  <div id="proj-global" class="collapse project-detail" data-parent="#projectAccordion">
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

</div>

<!-- ====== 업무 스타일 & 방향 ====== -->
<div class="section-title">Work Style</div>

- 문제를 **서비스 흐름 전체**를 따라가며 원인을 좁혀감
- 임시 복구보다 **재발 방지**를 더 중요하게 생각
- 반복 작업은 자동화, 운영 절차는 문서화하여 **재현 가능한 운영 환경** 구축
- 개발·운영·네트워크를 분리하지 않고 **하나의 시스템**으로 이해

---

<div class="section-title">Contact</div>

<div class="contact-bar">
  <a href="mailto:lsfguni@gmail.com" class="btn-primary-contact">
    <i class="fa fa-envelope"></i> lsfguni@gmail.com
  </a>
  <a href="https://github.com/lsfGuni" target="_blank">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

<div style="text-align:center; margin-top: 1rem;">
  <p style="font-size: 0.85rem; color: #888;">
    <a href="/career">상세 경력</a> ·
    <a href="/project">프로젝트 개별 페이지</a> ·
    <a href="/blog">업무 방식</a>
  </p>
</div>

<script>
  // 펼치기/접기 텍스트 토글 (화살표는 CSS transform으로 회전)
  $('#projectAccordion .project-toggle').on('click', function() {
    var textEl = $(this).find('.toggle-text');
    var target = $(this).data('target');
    setTimeout(function() {
      if ($(target).hasClass('show')) {
        textEl.text('접기');
      } else {
        textEl.text('펼치기');
      }
    }, 350);
  });
</script>
