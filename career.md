---
layout: page
title: Career
subtitle: 근본 원인까지 해결하는 DevOps 엔지니어
---

<p style="text-align:right; font-size:0.9rem;"><a href="{{ '/resume/' | relative_url }}">이력서(요약본) →</a> · <a href="{{ '/career-en/' | relative_url }}">English →</a></p>

<style>
  /* PDF 인쇄용 — 지원서 첨부 시 사용 */
  @media print {
    .intro-header, nav, footer, .navbar, .iso-embed, .iso-note, .iso-btn { display: none !important; }
    body { font-size: 10.5pt; }
    a { color: #333 !important; text-decoration: none !important; }
    h2 { break-before: page; }
    h2:first-of-type { break-before: auto; }
    h3, h4, table, svg { break-inside: avoid; }
    svg { max-height: 320px; }
    /* Bootstrap 그리드 리셋 — .row 음수 마진이 인쇄 시 좌측을 잘라내므로 함께 0으로 */
    .container-md, .container, .row, .col-xl-10, .col-lg-10, [class*="col-"] {
      max-width: 100% !important; width: 100% !important; flex: 0 0 100% !important;
      margin-left: 0 !important; margin-right: 0 !important;
      padding-left: 0 !important; padding-right: 0 !important;
    }
    html, body { width: auto !important; overflow: visible !important; }
  }
</style>

# Career

안녕하세요.  
저는 **배포 자동화와 근본 원인 분석(RCA)으로 안정적인 인프라를 만드는 DevOps 엔지니어** 한권희입니다.

현재는 **자사 블록체인 BaaS 서비스의 AWS·온프레미스 하이브리드 인프라를 상시 운영**하며,  
CI/CD 파이프라인, 모니터링·알림 체계, 그리고 상시 유입되는 봇·무차별 대입 공격 방어를 담당하고 있습니다.

Spring 기반 백엔드 개발자로 커리어를 시작해,  
실무에서는 **Linux 서버 구축·운영, AWS·온프레미스 하이브리드 인프라, CI/CD 파이프라인 구축·개선, 모니터링·알림 체계 구축을 통한 관측성(Observability) 확보, 보안 대응, 장애 대응 및 재발 방지, 운영 절차 문서화·표준화**까지 역할을 확장해 왔습니다.

최근에는 **폐쇄망(air-gapped) 환경의 AI 플랫폼 배포**, 금융권 망분리 환경 연동 트러블슈팅 등  
**제약이 큰 환경에서 서비스를 안정적으로 동작시키는 문제**를 주로 다루고 있습니다.

또한 사내 AI 에이전트 실행 플랫폼에서 **쿠버네티스 클러스터(k8s)와 ArgoCD GitOps 기반 배포 체계를 구축**하여,  
**실행 1건 = Job 1개**로 신뢰할 수 없는 워크로드를 격리하는 실행 인프라를 구축했습니다.

문제가 발생했을 때는 단순 복구에 그치지 않고,  
**근본 원인 분석 → 해결 → 고도화 → 문서화**로 이어지는 방식으로  
재발을 방지하고 재현 가능한 운영 체계를 만드는 것을 중요하게 생각합니다.

---

## Current Operations — 자사 서비스 상시 운영

### ⛓️ Berith 블록체인 서비스 — AWS 종속 해소 · 무인 운영 체계 구축 *(완료)*

**2024.08 ~ 2026.08 (2년 1개월) · DevOps / SRE · 인프라 운영 전담**
*(2024.08~2025.01 관계사 아이비즈소프트웨어 프로젝트 계약, 2025.02 베리드코리아 정규 입사)*

> 블록체인 서비스(BaaS·Wallet·Explorer) 인프라를 **2년간 운영**하며,
> AWS에 있던 서비스를 **사내 물리서버로 전량 이관**하고 진입 계층을 **Cloudflare Tunnel**로 교체했습니다.
> **월 고정비 78% 절감**.
> 상시 담당자 없이도 돌아가야 했기에 **사람 없이 스스로 복구하는 무인 운영 체계**를 만들고,
> **AI 세션이 장애 대응을 수행할 수 있도록** 진단 스크립트와 런북까지 구성했습니다.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 790" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
  <defs>
    <filter id="brShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
    <marker id="brArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
    <marker id="brArrowO" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#E8890C"/></marker>
    <marker id="brArrowR" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#C0392B"/></marker>
    <linearGradient id="brBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
    <linearGradient id="brGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
    <linearGradient id="brOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
    <linearGradient id="brRed" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#D9534F"/><stop offset="100%" stop-color="#C0392B"/></linearGradient>
    <linearGradient id="brGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
    <linearGradient id="brPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
  </defs>
  <rect width="920" height="790" fill="#FAFBFC" rx="12"/>
  <text x="460" y="28" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Berith 인프라 &#8212; AWS 진입 계층 전면 이전 (2026.08 완료)</text>
  <text x="460" y="46" text-anchor="middle" font-size="10.5" fill="#7F8C8D">Route 53 + ALB 8개 + WAF + 리버스프록시 EC2 &#8594; Cloudflare + 사내 커넥터 2대</text>

  <rect x="40" y="60" width="250" height="44" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="165" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">일반 이용자 &#183; BaaS 기업고객</text>
  <text x="165" y="96" text-anchor="middle" font-size="9" fill="#DDE1E3">Wallet &#183; Scan &#183; 삼성디스플레이 &#183; 롯데이노베이트</text>

  <rect x="302" y="60" width="196" height="44" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="400" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">PC 지갑 사용자</text>
  <text x="400" y="96" text-anchor="middle" font-size="9" fill="#DDE1E3">풀노드로 체인에 직접 참여</text>

  <rect x="510" y="60" width="200" height="44" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
  <text x="610" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">봇 &#183; 무차별 대입</text>
  <text x="610" y="96" text-anchor="middle" font-size="9" fill="#FADBD8">월 1.4~2억 요청 (WAF 청구로 역산)</text>

  <rect x="722" y="60" width="158" height="44" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="801" y="79" text-anchor="middle" font-size="11" font-weight="700" fill="#fff">AWS 월 청구</text>
  <text x="801" y="96" text-anchor="middle" font-size="11.5" font-weight="700" fill="#fff">78% 절감</text>

  <path d="M165,104 L165,126" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <path d="M400,104 L400,126" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <path d="M610,104 L610,126" stroke="#C0392B" stroke-width="2" marker-end="url(#brArrowR)"/>

  <rect x="30" y="132" width="860" height="96" rx="10" fill="#FEF5E7" stroke="#F5CBA7" stroke-width="1.5"/>
  <text x="46" y="152" font-size="11" font-weight="700" fill="#9C640C">Cloudflare &#8212; 진입 계층 (AWS Route 53 + ALB 8개 + WAF 대체)</text>

  <rect x="48" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="146" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">DNS &#183; TLS 종단</text>
  <text x="146" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">존 5개 &#183; 인증서 자동 갱신</text>

  <rect x="254" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="352" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">WAF &#183; 봇 &#183; DDoS</text>
  <text x="352" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">요청당 과금 &#8594; 정액 (공격량 무관)</text>

  <rect x="460" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="558" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Pages + R2</text>
  <text x="558" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">정적 홈페이지 &#183; 지갑 설치본 119MB</text>

  <rect x="666" y="162" width="206" height="52" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="769" y="184" text-anchor="middle" font-size="11.5" font-weight="700" fill="#fff">Tunnel</text>
  <text x="769" y="201" text-anchor="middle" font-size="9" fill="#DFF0D8">아웃바운드 전용 &#8594; 인바운드 개방 0</text>

  <path d="M769,214 L769,238 L460,238 L460,258" stroke="#E8890C" stroke-width="2" fill="none" marker-end="url(#brArrowO)"/>

  <rect x="230" y="262" width="460" height="66" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
  <text x="246" y="281" font-size="11" font-weight="700" fill="#186A3B">커넥터 2대 &#8212; 서로 다른 물리 호스트 (1대 장애는 견딤)</text>
  <rect x="246" y="288" width="200" height="32" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="346" y="308" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">cf-connector-01 (R740-2)</text>
  <rect x="458" y="288" width="216" height="32" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="566" y="308" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">cf-connector-02 (R740-1)</text>

  <path d="M460,328 L460,348" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <text x="472" y="343" font-size="9" fill="#5A6268">nginx :8080 &#8212; 도메인별 분기 &#183; upstream 헬스체크</text>

  <rect x="30" y="352" width="600" height="150" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="371" font-size="11" font-weight="700" fill="#1B4F72">사내 물리서버 2대 &#8212; berith VM 11대 (VirtualBox + systemd)</text>

  <rect x="46" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="114" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Wallet</text>
  <text x="114" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">무중단 전환 완료</text>

  <rect x="190" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="258" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Scan</text>
  <text x="258" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">익스플로러 + 색인</text>

  <rect x="334" y="380" width="136" height="42" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="402" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">BaaS API &#215;2</text>
  <text x="402" y="414" text-anchor="middle" font-size="8.5" fill="#DFF0D8">2노드 HA</text>

  <rect x="478" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="546" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Admin</text>
  <text x="546" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">소스 재빌드로 복구</text>

  <rect x="46" y="430" width="180" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="136" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Redis (ElastiCache 대체)</text>
  <text x="136" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">12노드 &#8594; 1대</text>

  <rect x="234" y="430" width="180" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="324" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">MinIO &#215;2 (S3 대체)</text>
  <text x="324" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">백업 이중화</text>

  <rect x="422" y="430" width="192" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="518" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Elasticsearch (OpenSearch 대체)</text>
  <text x="518" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">54GB &#183; 검색 인프라 내재화</text>

  <text x="46" y="490" font-size="9.5" fill="#1B4F72">별도 물리 5대 &#8212; 블록체인 노드 4대(RPC 1 &#183; 검증자 2 &#183; ETH 1) + Elasticsearch 1</text>

  <rect x="644" y="352" width="246" height="150" rx="10" fill="#FDEDEC" stroke="#E6B0AA" stroke-width="1.5"/>
  <text x="660" y="371" font-size="11" font-weight="700" fill="#943126">AWS &#8212; 남긴 것 (의도적)</text>

  <rect x="660" y="380" width="214" height="40" rx="7" fill="url(#brRed)" filter="url(#brShadow)"/>
  <text x="767" y="397" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">RDS (운영 DB)</text>
  <text x="767" y="411" text-anchor="middle" font-size="8.5" fill="#FADBD8">데이터 티어는 최후 &#183; 이관 설계 중</text>

  <rect x="660" y="426" width="214" height="40" rx="7" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="767" y="443" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">부트노드 1대</text>
  <text x="767" y="457" text-anchor="middle" font-size="8.5" fill="#FDF2E0">지갑 바이너리에 IP 하드코딩</text>

  <text x="660" y="482" font-size="9" fill="#943126">끄면 신규 사용자가 체인에 접속 불가</text>
  <text x="660" y="495" font-size="9" fill="#943126">&#8594; 지갑 재배포 없이는 폐기 불가로 판정</text>

  <rect x="30" y="512" width="430" height="118" rx="10" fill="#FEF9E7" stroke="#F7DC6F" stroke-width="1.5"/>
  <text x="46" y="531" font-size="11" font-weight="700" fill="#9A7D0A">무인 운영 &#8212; 담당자 부재를 전제로 설계</text>
  <rect x="46" y="540" width="184" height="36" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="138" y="556" text-anchor="middle" font-size="10" font-weight="600" fill="#fff">L1 로컬 워치독 &#215;11</text>
  <text x="138" y="569" text-anchor="middle" font-size="8.5" fill="#DDE1E3">2분 주기 &#183; 자가 복구</text>
  <rect x="240" y="540" width="204" height="36" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="342" y="556" text-anchor="middle" font-size="10" font-weight="600" fill="#fff">L2 호스트 감시자 &#215;2</text>
  <text x="342" y="569" text-anchor="middle" font-size="8.5" fill="#DDE1E3">VM 전원 계층 + L1 생존</text>
  <text x="46" y="594" font-size="9.5" font-weight="600" fill="#9A7D0A">판정 기준 &#8212; &#8220;프로세스가 떠 있는가&#8221; 가 아니라 &#8220;데이터가 진행하는가&#8221;</text>
  <text x="46" y="609" font-size="9" fill="#7D6608">서비스가 active 인 채 5일간 색인이 멈춘 사고를 겪고 판정 방식을 바꿈</text>
  <text x="46" y="623" font-size="9" fill="#7D6608">연속 3회 확인 &#183; 30분 쿨다운 &#183; 일일 상한 &#183; 과반 이상 시 전체 조치 중단</text>

  <rect x="474" y="512" width="416" height="118" rx="10" fill="#EAF2F8" stroke="#85C1E9" stroke-width="1.5"/>
  <text x="490" y="531" font-size="11" font-weight="700" fill="#1A5276">백업 3계층 &#8212; AWS OpenSearch 자동 S3 백업 대체</text>
  <rect x="490" y="540" width="126" height="36" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="553" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">스냅샷 6시간</text>
  <text x="553" y="569" text-anchor="middle" font-size="8" fill="#D6EAF8">&#8594; MinIO #1</text>
  <path d="M616,558 L628,558" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <rect x="632" y="540" width="126" height="36" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="695" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">미러 6시간</text>
  <text x="695" y="569" text-anchor="middle" font-size="8" fill="#D6EAF8">&#8594; MinIO #2 (pull)</text>
  <rect x="766" y="540" width="110" height="36" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="821" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">논리백업 매시간</text>
  <text x="821" y="569" text-anchor="middle" font-size="8" fill="#DFF0D8">양 호스트 독립</text>
  <text x="490" y="594" font-size="9.5" font-weight="600" fill="#1A5276">사본 측이 원본 자격증명을 갖지 않도록 pull 방향으로 설계</text>
  <text x="490" y="609" font-size="9" fill="#21618C">&#8594; 원본 측 사고(오삭제 &#183; 침해)가 사본까지 번지지 않음</text>
  <text x="490" y="623" font-size="9" fill="#21618C">미러가 9일간 &#8220;완료&#8221; 로그를 찍으며 실패한 사고 후, 판정을 로그에서 객체 수 실대조로 교체</text>

  <rect x="30" y="640" width="860" height="128" rx="10" fill="#F4F6F7" stroke="#D5DBDB" stroke-width="1.5"/>
  <text x="46" y="659" font-size="11" font-weight="700" fill="#2C3E50">비용 &#8212; 실청구 기준 (정가 추정이 아니라 청구서 확보 후 재산정)</text>

  <rect x="46" y="668" width="700" height="26" rx="5" fill="#E74C3C"/>
  <text x="56" y="686" font-size="11" font-weight="700" fill="#fff">이전 &#8212; 월 고정비 100%</text>
  <text x="700" y="686" font-size="9.5" fill="#FADBD8">2026-08 실청구</text>

  <rect x="46" y="700" width="154" height="26" rx="5" fill="#27AE60"/>
  <text x="56" y="718" font-size="11" font-weight="700" fill="#fff">현재 &#8212; 약 22%</text>
  <text x="212" y="718" font-size="9.5" fill="#196F3D">약 78% 감소</text>

  <text x="46" y="742" font-size="9.5" fill="#566573">폐기 &#8212; OpenSearch 2도메인 &#183; WAF &#183; ALB 7개 &#183; ElastiCache 전체 &#183; RDS 2개 &#183; EC2 9대 &#183; 탄력IP 23&#8594;4개</text>
  <text x="46" y="757" font-size="9.5" fill="#943126">단, 폐기분 스냅샷 2,874GB를 복구 보험으로 보존 중 &#8212; 만료(2027-02)까지는 그만큼이 상쇄됨. 전력 &#183; 하드웨어 감가를 넣은 순절감(TCO)은 여전히 미산정</text>
</svg>

#### 어떤 일이었나

기업용 블록체인 기록 서비스 **BaaS**(삼성디스플레이 보안서약서, 롯데이노베이트 물품관리 이력)와
B2C 서비스(**지갑 · 블록체인 익스플로러**)의 인프라 운영을 맡았습니다.
자체 이더리움 계열 메인넷을 포함해 AWS EC2 다수 · RDS · OpenSearch로 돌아가고 있었고,
지갑 특성상 계정 탈취를 노리는 봇 트래픽이 상시 유입되는 환경이었습니다.

풀어야 할 문제는 두 가지였습니다.

- **① AWS 월 고정비** — 실청구서를 확보해 보니 **회사가 알고 있던 금액의 3.7배**였습니다. 비용으로 한 번도 계산된 적 없던 항목(웹 방화벽 등)이 원인이었습니다
- **② 상시 담당자 부재** — 사람이 붙어 있지 않아도 서비스가 유지되어야 했습니다

#### 한 일

**진입 계층을 통째로 Cloudflare로 이전**

AWS Route 53 + ALB 8개 + WAF + 리버스프록시 EC2가 전 서비스의 단일 진입점이었고,
그 EC2는 **Ubuntu 16.04 EOL · 5.5년 무재기동 · 백업 0건**이었습니다.
Cloudflare Tunnel로 바꿔 **방화벽 인바운드 개방을 0으로** 만들고, 커넥터 2대를 서로 다른 물리 호스트에 두어 이중화했습니다.
도메인 단위로 8건을 전환했고 회귀는 없었습니다.
과금 모델이 **요청당 → 정액**으로 바뀌어, 봇 트래픽이 늘어도 청구가 오르지 않는 구조가 됐습니다.

**서비스 전량을 사내 물리서버로 이관**

- 지갑 — Redis 복제로 세션을 넘겨 **재로그인 없이 무중단 전환**. 구조가 AJP → HTTP + Nginx로 바뀌며 **AJP 노출(Ghostcat)도 함께 해소**
- BaaS — 2노드 HA로 구성, Nginx upstream 헬스체크로 장애 노드 자동 제외
- 관리자 콘솔·API 문서 — **라우팅만 바뀌어 있고 백엔드가 3년간 없던** 상태를 발견해 소스에서 재빌드 복구. 같은 패턴이 2건이라 "완료" 기록을 실제 응답으로 검증하는 절차를 추가
- ElastiCache 12노드 → Redis 1대 · OpenSearch 2도메인 → Elasticsearch 1대 · S3 → MinIO 2대

**폐기 판단은 실측으로**

"안 쓰는 것 같다"가 아니라 근거를 만들고 지웠습니다.

- ElastiCache — 14일간 명령 처리량 **양쪽 모두 0** 확인 + 설정·코드 참조 전수 조회
- OpenSearch — 인덱스를 전수 대조해 **온프레미스가 모든 인덱스에서 동등 이상**임을 확인, AWS 전용 인덱스도 표본으로 부분집합임을 실증
- 탄력 IP 반납은 되돌릴 수 없어 DNS 존·온프레 설정·블록체인 노드까지 참조를 전부 훑은 뒤 실행
- 반대로 **끌 수 없는 것**도 명확히 남겼습니다 — 부트노드는 **IP가 지갑 바이너리에 컴파일**돼 있어, 끄면 신규 사용자가 체인에 접속하지 못합니다

**무인 운영 체계 구축**

로컬 워치독 11대(2분 주기)와 호스트 감시자 2대(5분 주기)로 **사람 없이 스스로 복구**하게 만들었습니다.
관측 도구가 그래프를 산출한다면, 이 시스템의 산출물은 **재시작된 서비스**입니다.

- 🔑 판정 기준을 **"프로세스가 떠 있는가"에서 "데이터가 진행하는가"로** 바꾼 것이 핵심입니다 — 서비스가 `active (running)`으로 보고하는 채 **색인이 5일간 멈춘** 사고를 겪었기 때문입니다
- 안전장치 — 연속 3회 확인 후 조치 · 30분 쿨다운 · 일일 상한 · **의존 대상을 못 읽으면 조치 생략**(남의 장애를 우리 장애로 오인 방지) · **과반 동시 이상 시 전체 중단**(공통 원인일 때 대량 오조치 방지). 이 게이트가 실제로 발동해 **VM 6대 강제 재기동을 막았습니다**

**백업 3계층 구축 + 복원 실증**

AWS가 자동으로 해 주던 백업이 이관과 함께 사라져 직접 만들었습니다.

- 6시간 스냅샷 → MinIO #1, 6시간 미러 → MinIO #2(다른 물리 호스트), 재수집 불가 인덱스는 **매시간 논리백업**을 양 호스트가 독립적으로
- **사본이 원본을 당겨오는(pull) 방향**으로 설계 — 원본 쪽 사고(오삭제·침해)가 사본까지 번지지 않습니다
- 🔴 **미러가 9일간 36회 연속 실패하면서도 로그에는 "완료"를 찍고 있었습니다.** 이후 판정을 로그 시각에서 **객체 수 실대조**로 교체했습니다
- **실제 복원 리허설**로 동작을 확인했습니다 — "백업이 있다"와 "복원된다"는 다른 명제입니다

**판단이 틀렸을 때 되돌린 사례**

WAF 규칙을 Log에서 Block으로 올렸다가 **3분 만에 되돌렸습니다.**
24시간 실측에서 임계치 초과가 0건이라 안전하다고 봤는데, 관리형 룰셋에 액션을 덮어쓰면
**점수 합산을 거치지 않고 개별 규칙이 각자 차단**한다는 것을 전환 직후에야 확인했습니다.
안전이 검증된 부분(오탐 규칙 6종 비활성, 하루 로그의 81%)만 남겼습니다.

#### 결과

- **AWS 월 고정비 78% 절감** — OpenSearch 2도메인 · WAF · ALB 7개 · ElastiCache 전체 · RDS 2개 · EC2 9대 · 탄력 IP 23→4개 정리
- **진입 계층 단일 장애점 제거** — EOL·무재기동·백업 0건이던 EC2 의존을 걷어내고 물리 호스트가 다른 커넥터 2대로 이중화
- **장애 트러블슈팅 1주일 → 30분 이내** — 지표도 장애 이력도 없던 상태에서 모니터링·알림과 RCA 문서를 쌓아 만든 결과
- **봇 트래픽 하루 평균 1,000개 이상 IP 자동 차단** — 단일 봇에서 다수 IP 로테이션으로 진화한 공격에 맞춰 3계층 방어를 단계적으로 고도화
- **대부분의 장애가 사람이 인지하기 전에 자동 복구**되는 상태로 전환

#### 운영 지속성 — 담당자가 바뀌어도 돌아가게

담당자가 상주하지 않아도 운영이 이어지도록, **문서보다 "동작하는 것"을 남기는 데 무게를 뒀습니다.**

- **운영 문서 5권** — 아키텍처 · 백업체계 · 계정정보 · 폐기절차 · 운영 세션
- **사내 18대 통합 SSH 키** — 키 2종·계정 2개로 흩어져 있던 접속을 파일 하나로 통합(기존 인증은 유지). 배포·확인·폐기 스크립트 포함
- **AI 기반 장애 대응 세트** — 시스템 상태 9개 축을 한 번에 찍는 진단 스크립트 + 증상별 런북 9종을, **Claude Code 세션이 읽고 그대로 수행하도록** 진입 규칙과 함께 묶었습니다. 담당자가 "스캔이 안 된다" 수준으로 말해도 **사실 확보 → 원인 특정 → 조치** 순서를 밟습니다 — 추측으로 재시작부터 하지 못하게 규칙에 박아 뒀습니다
- **변경 이력과 결정 근거 기록** — 지금 구성이 왜 이 형태가 됐는지, 무엇을 확인하고 바꿨는지를 변경할 때마다 남겼습니다. **배경을 모르는 사람이 예전 방식으로 되돌리는 일**을 막기 위한 것입니다

---

## Featured Projects

### 🔒 삼성디스플레이 폐쇄망 AI 플랫폼 구축 (AI POC)

**2026.05 ~ 2026.06 · 폐쇄망 인프라 담당 (총 5인)**

> 인터넷이 차단되고 **USB 반입이 단방향(반출 불가)** 인 환경에 AI 서비스 5종과 게이트웨이를 배포했습니다.  
> 번들 누락 하나가 사이클 전체를 되돌리는 조건에서 **"내부에서는 빌드하지 않는다"** 로 전략을 바꿔,  
> 반입-배포 1사이클을 **5시간+ → 30분**으로 줄였습니다.

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

#### 문제 상황
- 인터넷·패키지 저장소·CI/CD가 모두 없는 환경 — `pip install` 한 줄도 동작하지 않는 곳에서 AI 서비스 5종을 구동해야 했습니다.
- 1사이클은 **빌드 → USB 적재 → 물리 반입 → 기동**인데, **USB는 한 번 반입하면 반출할 수 없습니다.** 기동 단계에서 번들 누락이 발견되면 사외로 나가 처음부터 다시 돌려야 했고, 초기에는 한 사이클에 5시간 이상이 걸렸습니다.
- 사전 조사도 제한돼 워크스테이션 사양을 미리 확인할 수 없었고, 결정적으로 **개발 환경(ARM)과 실제 배정된 워크스테이션(x86_64)의 CPU 아키텍처가 달랐다는 사실이 반입 후에야 드러났습니다.**

#### 해결 과정
- **"내부에서 빌드하지 않는다"로 전략 전환** — 실패 비용이 비대칭인 환경에서는 내부 빌드가 최대 리스크였습니다. 외부에서 **모든 의존성이 포함된 즉시 구동 가능한 이미지**를 완성해 반입하고 내부 작업은 적재·기동만 남기는 방식으로 바꿔, 1사이클을 **최소 30분**까지 단축
- **CPU 아키텍처 불일치 규명·해결** — ARM에서 빌드한 이미지와 wheel은 x86_64에서 실행 자체가 불가능(`exec format error`)합니다. 이를 원인으로 특정하고 **타깃 아키텍처(linux/amd64)를 명시해 전 산출물을 재빌드**
- **16GB VRAM 한 장에 맞춘 워크로드 배치** — 5개 서비스의 모델을 모두 로컬에 올릴 수 없어, **LLM 추론은 전량 watsonx API로 위임하고 GPU는 STT 전용으로 배분**. litellm을 모델 호출 단일 창구로 두어 서비스별 연동 코드를 분리
- **서비스 성격에 맞춘 배포 방식 선택** — 상시 기동이 필요한 4종(DevAX·WrenAI·보안성검토·ai-gateway)은 systemd 서비스로, 현장 개발자가 만들던 chat-bot은 컨테이너로 배포하고 **watsonx 연동을 담당**
- 외부 빌드 환경조차 제공되지 않아 **개인 장비를 사외로 반출해 LTE 테더링으로 빌드**하는 방식으로 반입 파이프라인을 유지
- 도입에 회의적이던 현장 이해관계자와 **신뢰 관계를 먼저 구축**하고, 고객사 PM과 기존 개발진 사이의 커뮤니케이션을 조율하여 프로젝트를 정상 궤도로 복원

#### 성과
- **POC 완료** — 전 서비스 정상 동작 시연, 고객사 임원 보고 긍정 평가로 **2026년 9월 후속 단계 진행 확정**
- 반입-배포 1사이클 **5시간+ → 30분 (약 90% 단축)**
- 폐쇄망 AI 서비스 5종 + 게이트웨이 전체를 **직접 배포·기동**
- **다음 프로젝트의 출발점을 만듦** — 이 POC에서 DevAX는 격리 인프라 없이 systemd로 구동했는데, 여기서 **에이전트가 자기 실행 환경을 수정하는 문제**가 드러났습니다. 이 경험이 아래 **Kubernetes 샌드박스 구축**으로 이어졌습니다.

**Tech:** litellm(LLM Gateway), IBM watsonx API, WrenAI, STT 모델 로컬 서빙, Docker(멀티 아키텍처 빌드), systemd, Linux(x86_64), GPU/CUDA, deb·wheel 오프라인 번들링, Yarn Berry 오프라인 빌드

---

### 🏦 하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터 엔지니어링

**2026.05 ~ 2026.07 (완료) · 어댑터 엔지니어 (총 6인) · 2026.07.15 정상 오픈**

> 외부망 SaaS부터 내부 SSO·DRM 애플리케이션까지, **업체가 모두 다른 시스템이 다단계로 이어지는 금융권 망분리 환경**에서  
> **구간별 통신 검증으로 연동 장애의 원인을 특정**하고 다자간 업무 조율로 해결했습니다.

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

#### 문제 상황
- 하나증권 **AI 협업솔루션 POC** 프로젝트의 세부 과제로 그룹웨어 SaaS 연동용 SSO·DRM 어댑터를 구축했으나, **Dooray(외부망) → VPN → 하나증권 인프라 → SSO·DRM 어댑터 → 내부 SSO·DRM 애플리케이션**으로 이어지는 다단계 연동 구간에서 통신 장애가 발생
- 구간마다 담당 업체가 모두 달라(그룹웨어사, VPN 업체, 하나증권 인프라팀, HA 업체, 내부 SSO·DRM 솔루션사) **어느 한 곳도 전체 흐름을 알지 못하는 상태**로 원인 규명이 정체

#### 해결 과정
- SSO·DRM 어댑터 설치 및 구동 스크립트 구축
- 장애 발생 시 전체 통신 경로를 구간별로 나누어 검증 — **각 주체의 설정 파일 확인 → 테스트 요청 → 로그 분석 → 원인 구간 특정 → 해당 업체 조치 요청**의 사이클을 반복하며 원인을 좁혀가는 방식으로 해결
- 운영 서버 SSO 초기화 실패를 DNS 미해석 + 방화벽 미개방으로 특정한 사례 등, 서버 권한 제약 환경에서 **비침습적 진단으로 근거를 확보**해 인프라팀 조치를 이끌어냄
- HA 업체, VPN 업체, 하나증권 인프라팀·현업, Dooray 등 **다자간 업무 조율**과 주간 정례 미팅으로 이슈·일정 협의

#### 성과
- 전 테스트 통과, **잔여 이슈 없이 7/15 정상 오픈 — 담당 업무 완료**
- 여러 업체에 걸쳐 있던 연동 장애를 구간별 검증으로 해소하여 **일정 지연 없이 진행**
- 애플리케이션·OS·네트워크를 관통하는 통신 구조 분석과 장애 진단·조율 프로세스 경험 확보

---

### 🗂️ 사내 문서관리 시스템 — 스테이징·운영 분리 및 CI/CD 배포 체계 구축

**2026.07 (완료) · 사내 프로젝트 · 서버 구축·CI/CD·문서화 담당**

> 검증 환경 없이 운영 서버 한 대에 수작업으로 배포되던 사내 문서관리 시스템(Google Drive 대체)에  
> **스테이징·운영 2서버 체계와 자동 배포 파이프라인을 신규 구축**하고, 인수인계 문서 2종과 함께 이관했습니다.

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 596" font-family="'Segoe UI', Arial, sans-serif" style="max-width:100%; border-radius:8px; margin:16px 0;">
  <defs>
    <filter id="dvShadow" x="-4%" y="-4%" width="108%" height="108%"><feDropShadow dx="1" dy="2" stdDeviation="2" flood-opacity="0.12"/></filter>
    <marker id="dvArrow" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7F8C8D"/></marker>
    <marker id="dvArrowP" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto"><polygon points="0 0, 8 3, 0 6" fill="#7B5BA6"/></marker>
    <linearGradient id="dvBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#4A90D9"/><stop offset="100%" stop-color="#357ABD"/></linearGradient>
    <linearGradient id="dvGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#5CB85C"/><stop offset="100%" stop-color="#449D44"/></linearGradient>
    <linearGradient id="dvGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#6C757D"/><stop offset="100%" stop-color="#5A6268"/></linearGradient>
    <linearGradient id="dvPurple" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#8E6FBF"/><stop offset="100%" stop-color="#7B5BA6"/></linearGradient>
    <linearGradient id="dvOrange" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#F0AD4E"/><stop offset="100%" stop-color="#EC971F"/></linearGradient>
  </defs>
  <rect width="920" height="596" fill="#FAFBFC" rx="12"/>
  <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">devax-drive 배포 체계 — 스테이징 자동 · 운영은 검증 이미지 승격</text>

  <rect x="30" y="48" width="860" height="160" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="68" font-size="11" font-weight="700" fill="#1B4F72">스테이징 (전 구간 자동) — main push 후 사람이 할 일 없음</text>

  <rect x="46" y="80" width="118" height="52" rx="8" fill="url(#dvGray)" filter="url(#dvShadow)"/>
  <text x="105" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">개발 PC</text>
  <text x="105" y="120" text-anchor="middle" font-size="9" fill="#DDE1E3">git push origin main</text>
  <path d="M164,106 L182,106" stroke="#7F8C8D" stroke-width="2" marker-end="url(#dvArrow)"/>

  <rect x="186" y="80" width="118" height="52" rx="8" fill="url(#dvGray)" filter="url(#dvShadow)"/>
  <text x="245" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Bitbucket</text>
  <text x="245" y="120" text-anchor="middle" font-size="9" fill="#DDE1E3">Jenkins 2분 폴링</text>
  <path d="M304,106 L322,106" stroke="#7F8C8D" stroke-width="2" marker-end="url(#dvArrow)"/>

  <rect x="326" y="80" width="130" height="52" rx="8" fill="url(#dvBlue)" filter="url(#dvShadow)"/>
  <text x="391" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Test (병렬)</text>
  <text x="391" y="120" text-anchor="middle" font-size="9" fill="#D6EAF8">실패 시 여기서 멈춤</text>
  <path d="M456,106 L474,106" stroke="#7F8C8D" stroke-width="2" marker-end="url(#dvArrow)"/>

  <rect x="478" y="80" width="130" height="52" rx="8" fill="url(#dvBlue)" filter="url(#dvShadow)"/>
  <text x="543" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Build → Push</text>
  <text x="543" y="120" text-anchor="middle" font-size="9" fill="#D6EAF8">사설 레지스트리 보관</text>
  <path d="M608,106 L626,106" stroke="#7F8C8D" stroke-width="2" marker-end="url(#dvArrow)"/>

  <rect x="630" y="80" width="130" height="52" rx="8" fill="url(#dvBlue)" filter="url(#dvShadow)"/>
  <text x="695" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">STG 배포</text>
  <text x="695" y="120" text-anchor="middle" font-size="9" fill="#D6EAF8">compose 자동 반영</text>
  <path d="M760,106 L778,106" stroke="#7F8C8D" stroke-width="2" marker-end="url(#dvArrow)"/>

  <rect x="782" y="80" width="94" height="52" rx="8" fill="url(#dvGreen)" filter="url(#dvShadow)"/>
  <text x="829" y="103" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Smoke</text>
  <text x="829" y="120" text-anchor="middle" font-size="9" fill="#DFF0D8">동작 확인</text>

  <text x="46" y="158" font-size="9.5" fill="#1B4F72">태그 = 빌드번호-커밋SHA · 테스트(프론트 typecheck·lint·test / 백엔드 gradle test) 실패 시 배포되지 않음</text>
  <text x="46" y="176" font-size="9.5" fill="#1B4F72">Jenkins 설정 전체를 JCasC(코드)로 관리 — UI 변경 금지, 컨테이너를 다시 만들어도 상태가 재현됨</text>
  <text x="46" y="194" font-size="9.5" fill="#1B4F72">스테이징·운영은 완전 동일 구성 — 환경 차이는 .env 파일 하나뿐</text>

  <rect x="30" y="224" width="860" height="150" rx="10" fill="#F4ECF7" stroke="#BB8FCE" stroke-width="1.5"/>
  <text x="46" y="244" font-size="11" font-weight="700" fill="#6C3483">운영 (수동 승격 게이트) — "운영서버 배포해 줘" 한 마디, 약 40초</text>

  <rect x="46" y="258" width="160" height="52" rx="8" fill="url(#dvPurple)" filter="url(#dvShadow)"/>
  <text x="126" y="281" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">배포 지시</text>
  <text x="126" y="298" text-anchor="middle" font-size="9" fill="#E8DAEF">사람 또는 AI 에이전트</text>
  <path d="M206,284 L224,284" stroke="#7B5BA6" stroke-width="2" marker-end="url(#dvArrowP)"/>

  <rect x="228" y="258" width="160" height="52" rx="8" fill="url(#dvPurple)" filter="url(#dvShadow)"/>
  <text x="308" y="281" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">태그 결정 · 이미지 검증</text>
  <text x="308" y="298" text-anchor="middle" font-size="9" fill="#E8DAEF">스테이징 검증 태그 승격</text>
  <path d="M388,284 L406,284" stroke="#7B5BA6" stroke-width="2" marker-end="url(#dvArrowP)"/>

  <rect x="410" y="258" width="160" height="52" rx="8" fill="url(#dvOrange)" filter="url(#dvShadow)"/>
  <text x="490" y="281" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">DB 자동 백업</text>
  <text x="490" y="298" text-anchor="middle" font-size="9" fill="#FDEBD0">pg_dump · 최근 20개 보관</text>
  <path d="M570,284 L588,284" stroke="#7B5BA6" stroke-width="2" marker-end="url(#dvArrowP)"/>

  <rect x="592" y="258" width="140" height="52" rx="8" fill="url(#dvPurple)" filter="url(#dvShadow)"/>
  <text x="662" y="281" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">운영 배포</text>
  <text x="662" y="298" text-anchor="middle" font-size="9" fill="#E8DAEF">재빌드 없음</text>
  <path d="M732,284 L750,284" stroke="#7B5BA6" stroke-width="2" marker-end="url(#dvArrowP)"/>

  <rect x="754" y="258" width="122" height="52" rx="8" fill="url(#dvGreen)" filter="url(#dvShadow)"/>
  <text x="815" y="281" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Smoke</text>
  <text x="815" y="298" text-anchor="middle" font-size="9" fill="#DFF0D8">응답 200 확인</text>

  <text x="46" y="336" font-size="9.5" fill="#6C3483">운영만 수동인 이유 — 백엔드 기동 시 Flyway DB 마이그레이션이 자동 적용되므로, 사람의 실행이 스키마 변경의 확인 지점</text>
  <text x="46" y="354" font-size="9.5" fill="#6C3483">Build Once, Promote — 운영에서 다시 빌드하지 않아 "스테이징에선 됐는데 운영에선 안 되네"가 원리적으로 발생하지 않음</text>

  <rect x="30" y="390" width="860" height="186" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
  <text x="46" y="410" font-size="11" font-weight="700" fill="#186A3B">구축 중 사고를 자산으로 — 재발 방지 문서화와 3중 롤백 경로</text>
  <text x="46" y="432" font-size="9.5" fill="#145A32">· 레지스트리 매니페스트 수동 삭제로 저장소가 통째로 비워진 사고 2회 → 여러 태그가 같은 매니페스트를 공유하는 원리를 규명하고,</text>
  <text x="56" y="449" font-size="9.5" fill="#145A32">  자동 정리 스크립트로만 정리하도록 금지사항 문서화 (환경변수 충돌·공유폴더 소유권 등 사고 전부 원인과 함께 기록)</text>
  <text x="46" y="470" font-size="9.5" fill="#145A32">· 롤백 경로 3중 확보 — ① 레지스트리 태그 승격 롤백 ② 전환 전 운영 VM 무손상 보존 ③ 전환 전 전체 백업(DB·설정·계정)</text>
  <text x="46" y="491" font-size="9.5" fill="#145A32">· 인수인계 문서 이원화 — 사람용 가이드(그림·이유 중심) + AI 에이전트용 참조 문서(명령 매핑·사실 정보) 분리 작성,</text>
  <text x="56" y="508" font-size="9.5" fill="#145A32">  미검증 항목(대용량 업로드 등)도 정직하게 기록해 인수자가 우선 확인할 지점을 명시</text>
  <text x="46" y="535" font-size="11" font-weight="700" fill="#1E8449">결과 — 수작업 배포가 "push 후 2분 대기 + 말 한마디"로 표준화, 배포마다 DB 백업 자동 확보</text>
  <text x="46" y="555" font-size="9.5" fill="#145A32">테스트를 통과하지 못한 코드는 배포될 수 없고, 운영 반영 직전 상태로 언제든 복원 가능한 체계</text>
</svg>

#### 문제 상황
- Google Drive를 대체하는 사내 문서관리 시스템이 **검증 환경 없이 운영 서버 한 대에서 수작업으로 배포**되는 상태
- 서버 전환 시점에 맞춰 스테이징·운영 2서버 체계와 CI/CD 파이프라인을 신규 구축하고, 이어받을 개발자를 위한 문서화까지 마쳐야 하는 과제

#### 해결 과정
- 스테이징(+CI+사설 레지스트리)과 운영 VM을 **완전 동일 구성**으로 구축 — 환경 차이를 `.env` 파일 하나로 수렴시켜 "환경이 달라서 생기는 장애"를 구조적으로 차단
- Jenkins 파이프라인 구축: main push → 2분 폴링 → 테스트(프론트 typecheck·lint·test / 백엔드 gradle test 병렬) → 이미지 빌드 → 레지스트리 푸시 → 스테이징 배포 → smoke — **테스트 실패 시 배포되지 않으며, push 이후 사람 개입 없음**
- 운영 배포는 **재빌드 없이 스테이징 검증 이미지를 태그로 승격**(약 40초), 배포 직전 `pg_dump` 자동 백업(최근 20개 보관)
- Jenkins 설정 전체를 JCasC로 코드화하고 파이프라인·compose·nginx 설정을 전부 저장소에서 관리 — 서버를 다시 만들어도 상태가 재현됨
- "운영서버 배포해 줘" / "〈태그〉로 롤백해 줘" 발화를 배포 스크립트로 매핑해 **코딩 에이전트(Claude Code)가 운영 배포·롤백·상태 확인을 수행**하도록 설계 — 자격증명은 저장소 밖에 분리
- 구축 중 발생한 사고 전부를 원인과 함께 금지사항으로 문서화 — 레지스트리 매니페스트 수동 삭제로 저장소가 비워진 사고 2회(여러 태그가 같은 매니페스트를 공유하는 원리 규명), compose 환경변수가 Jenkins 환경에 덮여 기동 실패한 사례, 공유폴더(vboxsf) 소유권 제약으로 DB 배치 위치를 결정한 근거 등

#### 설계 판단
- **운영 배포만 수동으로 남긴 이유** — 백엔드 기동 시 Flyway DB 마이그레이션이 자동 적용되므로, 스키마 변경이 확인 없이 운영 DB에 반영되는 것을 막는 확인 지점으로 사람의 실행을 배치
- **Build Once, Promote** — 운영에서 다시 빌드하지 않고 스테이징이 검증한 이미지를 그대로 옮겨 "스테이징에선 됐는데 운영에선 안 되네"를 원리적으로 제거
- **롤백 경로 3중 확보 후 전환** — 레지스트리 태그 승격 롤백 + 전환 전 운영 VM 무손상 보존 + 전체 백업(DB·설정·계정)을 먼저 갖춘 뒤 신규 체계로 전환

#### 성과
- 수작업 배포가 **"push 후 2분 대기 + 말 한마디"로 표준화** — 테스트를 통과하지 못한 코드는 배포될 수 없는 구조
- 배포마다 운영 DB 백업이 자동 확보되고, 운영 반영 직전 상태로 언제든 복원 가능
- 파이프라인 전 구간 검증 완료 후 **인수인계 문서 2종(사람용 가이드 + 에이전트용 참조)과 함께 이관** — 미검증 항목도 정직하게 기록해 다음 담당자가 첫날부터 배포 가능한 상태로 전달

**Tech:** Jenkins(JCasC), 사설 Docker Registry, Docker Compose, Nginx, PostgreSQL(Flyway), Bitbucket, KVM(libvirt)·VirtualBox, Shell, Claude Code 연동

---

### 📡 KBS 통합재난방송시스템 STG(스테이징) 인프라 구축

**2026.04 ~ 2026.06 · 인프라 설계·구축 담당**

> 검증 환경 없이 운영만 존재하던 시스템에 **운영과 동등한 스테이징을 신규 구축**했습니다.  
> PRD-STG 전 항목을 CLI로 대조 검증해 **불일치 0건**으로 마무리했습니다.

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

#### 문제 상황
재난 유형별 페이지를 제공하는 대국민 서비스인데 검증 환경 없이 운영만 존재해, 프론트 변경도 백엔드 배포도 운영에서 직접 확인해야 했습니다.
운영 담당자로부터 "운영 환경은 구축되어 있으나 스테이징이 없어 지금 구축하려 한다"는 현황을 전달받아 착수했고,
상세 구성 문서는 없는 상태여서 AWS CLI로 실제 리소스를 확인해 가며 동등한 환경을 재현하는 것이 과제였습니다.

#### 해결 과정
- **운영 환경 구성 파악** — AWS CLI로 리소스를 전수 조회해 ECS 태스크 정의·ALB 리스너·CloudFront 동작·DynamoDB 키 스키마·VPC 서브넷 구성을 복원하고, 이를 기준으로 구축 순서를 설계
- **ECS Fargate + CodeDeploy Blue/Green 무중단 배포 구축** — ALB 이중 리스너·타겟그룹 2조·ECR 연동, Jenkins 배포 파이프라인 동작까지 검증
- **CloudFront 7개 경로 분기 구성** — v1·v2(Next.js)·별도 포털이 한 도메인에서 병행되는 구조를 그대로 재현(S3 4버킷 + ALB 라우팅), DynamoDB 3테이블(GSI 포함)·IP 화이트리스트 접근제어 구성
- **비용과 제약이 걸린 판단 3건을 근거로 결정** — ACM 와일드카드가 한 레벨만 매칭한다는 점(RFC 6125)을 실제 인증서로 검증해 **인증서 추가 발급 비용을 사전 차단**, 계정 분리 대신 **단일 계정 + 네이밍·태그 분리**로 cross-account 관리 부담 제거, WAF를 붙일 수 없는 요금제 제약은 **CloudFront Functions로 IP 접근제어를 대체 구현**
- **IAM 최소권한 설계** — STG 전용 역할을 분리해, 개발자가 **운영 리소스는 조회만 가능**하도록 통제

#### 성과
- **STG 전 리소스 구축 완료** — PRD-STG 전 항목을 CLI로 대조 검증, **불일치 0건**
- **운영에서 직접 배포를 검증하던 구조를 제거** — 개발팀이 안전하게 테스트할 환경 확보
- 구축 가이드·체크리스트·참조 문서로 **담당자가 바뀌어도 이어갈 수 있는 상태** 유지

**Tech:** AWS ECS(Fargate), ECR, CodeDeploy(Blue/Green), ALB, CloudFront, CloudFront Functions, WAF, Route 53(Alias Record), ACM, S3, DynamoDB(GSI), IAM, AWS CLI

---

### 🤖 AI 에이전트 실행 플랫폼 — Kubernetes 격리 실행 인프라 *(사내 프로젝트, 구축 완료)*

**2026.05 ~ 2026.08 · 클러스터 구축·GitOps 배포 파이프라인 담당**

> 위 삼성디스플레이 POC에서 드러난 **"에이전트가 자기 실행 환경을 수정하는"** 문제를 풀기 위해,  
> **실행 1건을 Job 1개로 격리**하는 쿠버네티스 인프라를 구축했습니다.

#### 문제 상황
**위 삼성디스플레이 POC에서 이어진 과제입니다.** 그때 DevAX는 격리 인프라 없이 systemd로 구동했는데,  
에이전트가 호스트 파일을 건드려 자기 실행 환경을 망가뜨리는 일이 발생했습니다.  
에이전트에는 모델 API 키와 사내 서비스 토큰이 주입되기 때문에, 실행 단위를 격리하는 sandbox 인프라가 필요했습니다.

#### 구축 내용
- **k3s 클러스터 직접 구축** — 사내 VM에 컨트롤플레인·워커를 분리 구성, 기본 traefik을 ingress-nginx로 교체하고 Linkerd 서비스 메시로 서비스 간 mTLS 적용
- **에이전트 실행 1건 = Job 1개**로 격리 — 전용 네임스페이스(`agent-jobs`)와 전용 ServiceAccount를 부여하고, Job 생성 시 `backoffLimit=0`(실패 재시도 없음) · `activeDeadlineSeconds`(무한 대기 차단) · `ttlSecondsAfterFinished`(완료 Job 자동 정리)를 지정
- **ArgoCD app-of-apps GitOps** — 루트 Application 1개가 자식 18개를 관리하고, Helm 차트 14종을 Git 단일 소스에서 선언적으로 배포. Bitbucket Pipelines + self-hosted runner 연동
- **레지스트리 3종 self-host** — Harbor(컨테이너 이미지)·Kellnr(Rust crate)·Verdaccio(npm)를 사내에 직접 운영
- **설계 판단을 ADR 28건으로 문서화** — Linkerd 도입, app-of-apps finalizer 표준화, Sealed Secrets 도입, 멀티테넌시 스키마 분리 등

#### 인터랙티브 아키텍처 도면 (직접 제작)

클러스터 구조를 설명하고 진행 상황을 공유하기 위해 직접 만든 아이소메트릭 도면입니다.
**일반 K8s · DevAX 구조 · 자연어 실행 · Sandbox · GitOps · 관측성** 6개 모드로 관점을 바꿔 볼 수 있고,
컴포넌트를 클릭하면 역할 설명이 나옵니다. **구현 완료 / 스캐폴드 / 목표**를 색으로 구분해 진행 상황을 있는 그대로 표시합니다.

<style>
  .iso-embed { margin: 12px 0 6px 0; border: 1px solid #dee2e6; border-radius: 10px; overflow: hidden; background: #040d1e; }
  .iso-embed iframe { display: block; width: 100%; height: 600px; border: 0; }
  .iso-note { font-size: 0.85rem; color: #666; line-height: 2.1; }
  .iso-btn { display: inline-block; margin-left: 4px; padding: 7px 15px; border-radius: 8px; font-size: 0.85rem; font-weight: 600; text-decoration: none; background: #0b1b3a; color: #7dd3fc !important; border: 1px solid #1e3a6a; }
  .iso-btn:hover { background: #12264f; color: #bae6fd !important; text-decoration: none; }
  @media (max-width: 820px) { .iso-embed { display: none; } }
  @media print { .iso-embed { display: none !important; } }
</style>

<div class="iso-embed">
  <iframe src="{{ '/assets/diagrams/k8s-iso-city.html' | relative_url }}" title="DevAX Kubernetes 인프라 아이소메트릭 도면" loading="lazy"></iframe>
</div>

<p class="iso-note">드래그로 시점 이동 · 컴포넌트 클릭 시 상세 설명 · 1~6 키로 모드 전환(전체 화면 권장)
  <a class="iso-btn" href="{{ '/assets/diagrams/k8s-iso-city.html' | relative_url }}" target="_blank" rel="noopener">🖥️ 전체 화면으로 열기</a>
</p>

#### 구축 범위

**인프라 구축과 에이전트 실행 관통 검증까지 완료했습니다.** 서비스 오픈은 이후 일정이라, 상용 트래픽을 받은 운영 경험은 아닙니다.
- **에이전트 실행 1차 관통 완료** (2026-05-29) — 자동 검증 23종 전체 통과
- **egress NetworkPolicy는 적용 후 의도적으로 비활성** — 화이트리스트에 **Linkerd 컨트롤 플레인 포트**(destination 8086 / policy 8090 / identity 8080)를 넣지 않아 사이드카가 막히면서, 컨트롤러가 JWKS를 가져오지 못해 hang → 포트 바인딩 실패 → liveness 실패 → **`Exit 137`(SIGKILL)**. 원인을 여기까지 추적한 뒤 **재활성 조건(Linkerd 3포트 + OTel 4317 + JWKS)을 문서화**하고 현재는 끈 상태로 관리하고 있습니다
- **실격리(microVM)와 사용자 화면은 미착수** — 현재는 네임스페이스·RBAC 수준의 논리 격리까지이며, 컨테이너 탈출까지 막는 실격리는 다음 과제로 남겨두고 리스크로 명시 관리 중입니다

---

## Career Summary

- **총 경력:** 2년 11개월+
- **핵심 분야:** DevOps, AI Platform Infrastructure(LLM Serving), Backend Development
- **중심 역량:** CI/CD 파이프라인 구축·개선, Air-gapped(폐쇄망) 배포, Hybrid Infrastructure, **비용 최적화(FinOps) 기반 클라우드 → 온프레미스 이관**, 관측성(Observability), 장애 대응·RCA, 운영 절차 문서화·표준화
- **Kubernetes:** 사내 AI 에이전트 실행 플랫폼에서 **k3s 클러스터 직접 구축 + ArgoCD app-of-apps GitOps 배포 체계 구성** — 실행 1건 = Job 1개 격리, 전용 네임스페이스·ServiceAccount·RBAC (관리형 서비스(EKS·GKE) 경험은 없으며 self-managed 클러스터 구축 기준. 상용 트래픽 운영 경험은 아닙니다)
- **전환 진행 중:** Terraform·Ansible 기반 IaC — 홈랩(Proxmox 3대) 실습 병행
- **관심 방향:** AI 플랫폼 인프라(LLM 서빙, GPU), 배포 자동화, 신뢰성 엔지니어링(SRE), 플랫폼 엔지니어링

---

## Professional Experience

### 베리드코리아
**개발팀 / 주임**  
**2025.02 ~ Present**  
**Role:** Developer · DevOps · SRE

#### 주요 업무
- 자사 블록체인 서비스(BaaS·Berith Wallet·Berith Scan) 인프라 **운영 전담** — 자체 메인넷 노드, 사내 물리서버 2대 위 VM 11대 + 별도 물리 5대
- **진입 계층을 AWS(Route 53 + ALB 8개 + WAF + 리버스프록시 EC2)에서 Cloudflare Tunnel로 전면 이전** — 인바운드 포트 개방 0, 커넥터 2대를 서로 다른 물리 호스트에 배치해 이중화
- **AWS 월 고정비 78% 절감 (FinOps)** — 리스크 기준으로 이관 순번을 설계하고 롤백 경로를 먼저 확보한 뒤 전환. 폐기 판단은 추정이 아니라 14일 실측·인덱스 전수 대조 같은 근거로 수행
- **담당자 부재를 전제로 한 무인 운영 체계 구축** — L1 워치독 11대 + L2 호스트 감시자 2대의 2계층 자가복구, 백업 3계층(복원 리허설 실증), 운영 문서 5권과 AI 장애 대응 세트 구축
- Docker 기반 Web / WAS / DB 컨테이너 운영 체계 구축·운영
- AWS WAF, Nginx, iptables를 활용한 다층 보안 아키텍처 구축 및 무차별 대입·봇 트래픽 상시 대응
- 외부 헬스체크와 내부 지표를 결합한 모니터링·알림 체계 구축으로 관측성(Observability) 확보, Slack 실시간 알림 운영
- 사내 AI 에이전트 실행 플랫폼 인프라 구축 (2026.05~) — **AI가 스스로 작성한 코드를 안전하게 실행**하기 위한 격리 환경 구축. 실행 1건마다 일회용 Job으로 분리하고 전용 네임스페이스·ServiceAccount·RBAC를 부여, 쿠버네티스 클러스터 직접 구축 + ArgoCD GitOps 배포 자동화
- Jenkins 및 스크립트 기반 CI/CD 파이프라인 구축과 빌드·테스트·배포 자동화
- 장애 대응 시 로그 기반 근본 원인 분석(RCA) 및 재발 방지 대책 수립
- 해외 개발자 온보딩을 위한 서버 접근, 레포지토리, 배포 절차 문서화
- MCP, OpenSearch, S3, Lambda, EC2를 연동한 AI 실행 인프라 구축·운영
- 온프레미스 서버실 구축 및 VM 백업·재해복구(DR) 체계 운영
- **삼성SDR 파견 (2025.09 ~ 2026.03):** Spring MVC 기반 내방객 관리시스템 풀스택 개발, 카드사 연동 REST API 설계·개발, JBoss 배포 전략 수립
- 하나증권 AI 협업솔루션 POC 그룹웨어 어댑터 엔지니어링 — 금융권 망분리 환경 SSO/DRM/인사연동 (2026.05~07, 완료)
- 삼성디스플레이 폐쇄망 AI 플랫폼 구축 — AI POC (2026.05~06), 반입-배포 사이클 5시간+→30분 단축, 9월 후속 단계 확정
- KBS 통합재난방송시스템 STG 인프라 구축 (2026.04~06) — 검증 환경이 없던 서비스에 AWS CLI로 운영 구성을 확인해 동등한 스테이징 재현, ECS Fargate·CodeDeploy Blue/Green, CloudFront 경로 분기, IAM 최소권한, PRD-STG 대조 검증 불일치 0건
- 사내 문서관리 시스템 스테이징·운영 분리 및 CI/CD 배포 체계 구축 (2026.07, 완료) — Jenkins(JCasC)·사설 레지스트리 기반 자동 파이프라인, 운영은 재빌드 없이 검증 이미지 승격(Build Once, Promote) + 배포 직전 DB 자동 백업, 인수인계 문서 2종(사람용·AI 에이전트용)과 함께 이관

#### 핵심 성과
- 하이브리드 인프라 운영 기준 정립 및 운영 절차 문서화·표준화
- 다층 보안 방어 체계로 봇 트래픽 선제 차단(하루 평균 1,000개 이상 IP) — **AWS 비용 20% 이상 절감**, 서비스 안정성 확보
- 모니터링·알림 자동화로 **장애 트러블슈팅 소요 시간 1주일 → 30분 이내 단축**
- 재현 가능한 배포 파이프라인과 운영 절차 확립
- 원격·해외 협업 환경의 온보딩 시간 단축
- 삼성SDR 내방객 관리시스템 카드연동 API 자동화 및 배포 안정화

---

### 아이비즈소프트웨어
**프로젝트 계약 / Backend Developer · DevOps**  
**2024.08 ~ 2025.01** *(베리드코리아 관계사 — 동일 사업장, 2025.02 베리드코리아 정규 입사)*

#### 주요 업무
- NIPA 블록체인 정부과제 — **의약품 이력관리 시스템** 개발: 백엔드·인프라 담당
- Spring Boot 기반 REST API 설계·개발 — Flutter 모바일 앱(iOS 개발자 협업) 연동
- 관리자 페이지(Thymeleaf) 개발 및 MariaDB 데이터 모델링
- 블록체인 연계 이력 기록·조회 기능 개발 (정부과제 검수 대응)
- AWS EC2 서버 구축·운영 및 배포 자동화

#### 핵심 성과
- 백엔드 개발부터 서버 구축·배포까지 전 과정을 1인으로 수행
- 이 시기의 AWS 서비스 구축 경험이 이후 베리드코리아 하이브리드 인프라 운영의 기반이 됨

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
- 폐쇄망(망분리) 환경에서 AI 서비스 스택(LLM 게이트웨이·Text-to-SQL·보안성검토 에이전트·STT) 오프라인 배포·기동 경험
- 오프라인 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 사전 빌드, 물리 반입(내부망 반입 프로세스) 절차 설계
- LLM 게이트웨이(litellm)·IBM watsonx API 연동 구성, **CPU 아키텍처(ARM↔x86_64) 불일치** 등 오프라인 배포 특화 트러블슈팅
- 제한된 GPU 자원에서 로컬 서빙과 원격 API 위임을 나누는 **워크로드 배치 판단** 경험

### Kubernetes & GitOps
- **k3s 클러스터 직접 구축** — 컨트롤플레인·워커 분리, ingress-nginx 교체 구성, Linkerd 서비스 메시(mTLS), OpenTelemetry·Tempo 트레이싱
- **ArgoCD app-of-apps GitOps** — 클러스터 상태를 Git 단일 소스로 선언적 관리, 서비스별 Helm 차트와 Bitbucket Pipelines + self-hosted runner 연동
- **워크로드 격리 구성** — 실행 1건 = Job 1개, 전용 네임스페이스·ServiceAccount·최소 권한 RBAC, `backoffLimit=0`·`activeDeadlineSeconds`·`ttlSecondsAfterFinished`로 재시도·무한 대기·잔여 리소스 차단
- **egress NetworkPolicy 트러블슈팅** — 화이트리스트에 Linkerd 컨트롤 플레인 포트가 빠져 사이드카가 막히며 `Exit 137`로 죽는 현상을 추적, 재활성 조건을 문서화 (현재 비활성 상태로 관리)
- (관리형 쿠버네티스(EKS·GKE) 운영 경험은 없으며, self-managed 클러스터를 컨트롤플레인부터 직접 구성한 경험 기준)

### IaC (전환 진행 중)
- 물리 서버 3대에 Proxmox 프라이빗 클라우드를 직접 구축하고, Terraform(VM 프로비저닝) + Ansible(k8s 설치·설정)로 **클러스터 전체를 명령 두 번으로 재현**하는 IaC 전환 진행

### CI/CD & Automation
- Jenkins, GitLab CI, Bitbucket Pipelines 기반 CI/CD 파이프라인 구축·개선 및 배포 자동화 경험
- AWS CodeDeploy 기반 Blue/Green 무중단 배포 구성 경험
- 반복 작업의 스크립트 자동화, 배포 절차 표준화, 운영 문서화로 팀 누구나 동일하게 운영 가능한 체계 구축

### Hybrid Infrastructure & FinOps
- AWS와 온프레미스를 연동하는 인프라 설계·구축·운영 경험
- **클라우드 비용 구조를 근거로 온프레미스 전량 이관을 설계·완료한 경험 (월 청구 78%↓)** — 이관 순번을 리스크 기준으로 정하고, 롤백 경로를 먼저 확보한 뒤 도메인 단위로 전환. **못 옮기는 것(지갑에 IP가 하드코딩된 부트노드)과 남길 것(데이터 티어)을 근거와 함께 분리해 판단**
- **과금 모델을 바꿔 비용을 구조적으로 고정한 경험** — 요청당 과금(AWS WAF)이라 공격량이 곧 청구이던 구조를 정액 + DDoS 무제한으로 교체
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

### 폐쇄망 AI 플랫폼 구축
USB 반입이 단방향인 폐쇄망에 AI 서비스 5종을 배포하면서, 실패 비용이 비대칭인 조건에서  
**"내부에서는 빌드하지 않는다"** 로 전략을 바꿔 반입-배포 사이클을 **5시간+ → 30분으로 단축**했습니다.

### 검증 환경이 없던 서비스의 스테이징 구축
AWS CLI로 운영 환경 구성을 확인해 가며 **운영과 동등한 스테이징을 구축**하고,  
PRD-STG 전 항목을 대조 검증해 **불일치 0건**으로 마무리했습니다.

### 사내 문서관리 시스템 CI/CD 배포 체계 구축
수작업 배포되던 시스템에 스테이징·운영 2서버 체계와 Jenkins 자동 파이프라인을 구축하고,  
운영은 **재빌드 없이 검증 이미지를 승격(Build Once, Promote)** + 배포 직전 DB 자동 백업으로 **"push 후 2분 + 말 한마디"** 배포를 만들었습니다.

### DDoS 대응체계 구축
AWS WAF, Nginx, iptables를 결합한 **3계층 방어 아키텍처**로  
일 50GB 이상의 공격 로그를 남기던 무차별 대입·봇 트래픽을 **하루 평균 1,000개 이상 IP 자동 차단**으로 선제 대응하여, **AWS 비용을 20% 이상 절감**하고 핵심 API의 안정성을 확보했습니다.

### 모니터링 · 알림 체계 구축
Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반  
외부 헬스체크 결합 모니터링과 Slack 실시간 알림으로 **장애 트러블슈팅 소요 시간을 1주일에서 30분 이내로** 단축했습니다.

### Kubernetes 기반 AI 에이전트 격리 실행 인프라
쿠버네티스 클러스터(k8s)에서 **에이전트 실행 1건을 Job 1개로 격리**하고,  
전용 네임스페이스·ServiceAccount·최소 권한 RBAC와 Job 옵션(`backoffLimit=0`·deadline·TTL)으로 실행 단위를 봉인했습니다.  
ArgoCD app-of-apps GitOps로 **클러스터 상태를 Git 단일 소스에서 선언적으로 관리**합니다.

### 홈랩 프라이빗 클라우드 & IaC 전환 (개인 프로젝트, 진행 중)
물리 서버 3대에 Proxmox 프라이빗 클라우드를 구축하고,  
Terraform + Ansible로 k8s 멀티노드 클러스터 전체를 **명령 두 번(terraform apply + ansible-playbook)으로 재현**하는 IaC 체계를 만들고 있습니다.

### 글로벌 개발 인프라 구축
AWS와 온프레미스를 연결한 하이브리드 개발 인프라를 구축하고,  
Jenkins 기반 CI/CD 파이프라인과 Slack 연동으로 **해외 개발자가 빠르게 온보딩 가능한** 협업 환경을 정비했습니다.

### VM 서버 백업 시스템 구축
ZFS 스냅샷, 증분 백업, UPS 연동 자동 종료 체계를 설계하여  
정전·장애 상황에서도 **개발 자산이 유실되지 않는 재해복구(DR) 체계**를 확보했습니다.

### AI 실행 인프라 구축
MCP, OpenSearch, S3, Lambda, EC2를 연결해  
질의응답 실행과 데이터 인덱싱·검색이 가능한 **재현형 AI 실행 인프라**를 구축했습니다.

---

## Technical Environment

### Cloud / Infra
AWS, Route 53(Alias Record), ACM, ALB, EC2, ECS(Fargate), ECR, CodeDeploy(Blue/Green), CloudFront, CloudFront Functions, Lambda, VPC, WAF, CloudWatch, OpenSearch, S3, DynamoDB(GSI), IAM, AWS CLI

### AI / LLM Infrastructure
litellm(LLM Gateway), IBM watsonx, MCP, 오프라인 모델·패키지 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 반입

### Container / Orchestration / IaC
Docker, Kubernetes(k3s), Helm, ArgoCD(GitOps·app-of-apps), Linkerd(mTLS), NetworkPolicy·RBAC, Harbor·Kellnr·Verdaccio, Terraform, Ansible, Proxmox

### Blockchain Infrastructure
이더리움 계열 자체 메인넷·부트노드 노드 운영, OpenSearch 기반 체인 데이터 인덱싱

### Server / Network
Linux, Ubuntu, Docker, Apache HTTP Server, Apache Tomcat, Nginx, iptables, WireGuard

### CI/CD / DevOps
Jenkins, GitLab CI, Bitbucket Pipelines, Docker Compose, Git

### Monitoring / Observability
Prometheus, Grafana, Alertmanager, Blackbox Exporter, Tempo, OpenTelemetry, CloudWatch

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
