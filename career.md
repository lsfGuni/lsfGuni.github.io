---
layout: page
title: Career
subtitle: 근본 원인까지 해결하는 DevOps 엔지니어
---

# Career

안녕하세요.  
저는 **배포 자동화와 근본 원인 분석(RCA)으로 안정적인 인프라를 만드는 DevOps 엔지니어** 한권희입니다.

현재는 **자사 블록체인 BaaS 서비스의 AWS·온프레미스 하이브리드 인프라를 상시 운영**하며,  
CI/CD 파이프라인, 모니터링·알림 체계, 그리고 상시 유입되는 봇·무차별 대입 공격 방어를 담당하고 있습니다.

Spring 기반 백엔드 개발자로 커리어를 시작해,  
실무에서는 **Linux 서버 구축·운영, AWS·온프레미스 하이브리드 인프라, CI/CD 파이프라인 구축·개선, 모니터링·알림 체계 구축을 통한 관측성(Observability) 확보, 보안 대응, 장애 대응 및 재발 방지, 운영 절차 문서화·표준화**까지 역할을 확장해 왔습니다.

최근에는 **폐쇄망(air-gapped) 환경의 LLM 서빙 인프라 구축**, 금융권 망분리 환경 연동 트러블슈팅 등  
**제약이 큰 환경에서 서비스를 안정적으로 동작시키는 문제**를 주로 다루고 있습니다.

또한 사내 AI 에이전트 실행 플랫폼에서 **쿠버네티스 클러스터(k8s)와 ArgoCD GitOps 기반 배포 체계를 구축**하여,  
**Job·NetworkPolicy·RBAC로 신뢰할 수 없는 워크로드를 격리**하는 실행 인프라를 운영하고 있습니다.

문제가 발생했을 때는 단순 복구에 그치지 않고,  
**근본 원인 분석 → 해결 → 고도화 → 문서화**로 이어지는 방식으로  
재발을 방지하고 재현 가능한 운영 체계를 만드는 것을 중요하게 생각합니다.

---

## Current Operations — 자사 서비스 상시 운영

### ⛓️ Berith 블록체인 서비스(BaaS·Wallet·Scan) 하이브리드 인프라 운영

**2024.08 ~ 현재 · DevOps / SRE 담당**

> 기업용 블록체인 기록 서비스(BaaS)와 B2C 지갑·익스플로러 서비스를  
> **AWS(EC2 7대 + RDS + OpenSearch) + 온프레미스 이중화**의 하이브리드 구성으로 상시 운영합니다.

#### 운영 대상
- **BaaS (주력, B2B)**: 삼성디스플레이 보안서약서, 롯데이노베이츠 물품관리 이력을 블록체인에 기록하는 기업용 서비스
- **Berith Wallet / Berith Scan (B2C)**: 코인 지갑과 블록체인 익스플로러 — 지갑 서비스 특성상 **계정 탈취를 노리는 무차별 대입·봇 공격이 상시 유입**되는 환경
- **인프라 구성**: 부트노드 2대·메인넷 노드(이더리움 계열 자체 메인넷) 포함 AWS EC2 7대, RDS, OpenSearch(체인 데이터 인덱싱·Scan 연동), Nginx 웹 계층(Route 53 기반으로 AWS와 온프레미스에 요청 라우팅), 온프레미스 이중화 서버

#### 주요 성과
- 인수인계 없이 운영을 맡은 초기에는 "뭔가 안 된다" 수준의 신고에서 원인 규명까지 1주일가량 걸렸으나, 모니터링·알림 체계 구축과 장애별 RCA 문서가 쌓이면서 **트러블슈팅 소요 시간을 30분 이내로 단축**
- **일 50GB 이상의 공격성 트래픽 로그, 하루 평균 1,000개 이상의 IP를 자동 차단** — 단일 봇 차단 이후 다수 IP가 로테이션하며 공격하는 패턴으로 진화하자 WAF·Nginx·iptables 3계층 방어를 단계적으로 고도화, **AWS 비용 20% 이상 절감**
- 이중화 구성 일부를 온프레미스로 이관하는 하이브리드 재설계로 AWS 비용 추가 절감
- 대규모 트랜잭션 유입 시 반복되던 메인넷 노드 다운의 근본 원인을 **디스크 I/O 병목 + 체인 데이터 용량 부족**(블록체인 노드 특성상 전체 체인 데이터를 로컬 디스크에 보관)으로 특정 — EBS 증설로 용량을 해결하고, 장비 증설 없이 **BaaS 요청을 온프레미스 메인넷으로 분산**(Wallet은 AWS 유지)하는 구조 변경으로 I/O 병목까지 해소하여 재발 방지

---

## Featured Projects

### 🔒 삼성디스플레이 폐쇄망 AI 플랫폼 구축 (AI POC)

**2026.05 ~ 2026.06 · 폐쇄망 인프라 단독 담당 (총 5인 중 인프라 1인)**

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
- 폐쇄망 AI 서비스 5종 + 게이트웨이 전체를 **단독으로 배포·기동**
- **다음 프로젝트의 출발점을 만듦** — 이 POC에서 DevAX는 격리 인프라 없이 systemd로 구동했는데, 여기서 **에이전트가 자기 실행 환경을 수정하는 문제**가 드러났습니다. 이 경험이 아래 **Kubernetes 샌드박스 구축**으로 이어졌습니다.

**Tech:** litellm(LLM Gateway), IBM watsonx API, WrenAI, STT 모델 로컬 서빙, Docker(멀티 아키텍처 빌드), systemd, Linux(x86_64), GPU/CUDA, deb·wheel 오프라인 번들링, Yarn Berry 오프라인 빌드

---

### 🏦 하나증권 AI 협업솔루션 POC — 그룹웨어 어댑터 엔지니어링

**2026.05 ~ 2026.07 (완료) · 어댑터 엔지니어 (총 6인) · 2026.07.15 정상 오픈**

> 외부망 SaaS부터 내부 SSO·DRM 애플리케이션까지, **업체가 모두 다른 시스템이 다단계로 이어지는 금융권 망분리 환경**에서  
> **구간별 통신 검증으로 연동 장애의 원인을 특정**하고 다자간 업무 조율로 해결했습니다.

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

### 📡 KBS 통합재난방송시스템 STG(스테이징) 인프라 구축

**2026.04 ~ 2026.06 · 인프라 설계·구축 단독 (1인)**

> 아는 사람도 문서도 없는 운영 AWS 계정을 **CLI로 역분석해 동등한 스테이징 환경을 혼자 처음부터 구축**했습니다.  
> 5일간 멈춰 있던 도메인 이슈는 **DNS 위임 계층을 추적해 원인이 어디에 있는지 증거로 증명**했습니다.

#### 문제 상황
재난 유형별 페이지를 제공하는 대국민 서비스인데 검증 환경 없이 운영만 존재해, 프론트 변경도 백엔드 배포도 운영에서 직접 확인해야 했습니다.
운영 환경의 구성을 아는 담당자도, 인수인계 문서도 없는 상태에서 동등한 환경을 재현하는 것이 과제였습니다.

#### 해결 과정
- **운영 환경 역분석** — AWS CLI로 리소스를 전수 조회해 ECS 태스크 정의·ALB 리스너·CloudFront 동작·DynamoDB 키 스키마·VPC 서브넷 구성을 복원하고, 이를 기준으로 구축 순서를 설계
- **ECS Fargate + CodeDeploy Blue/Green 무중단 배포 구축** — ALB 이중 리스너·타겟그룹 2조·ECR 연동, Jenkins 배포 파이프라인 동작까지 검증
- **CloudFront 7개 경로 분기 구성** — v1·v2(Next.js)·별도 포털이 한 도메인에서 병행되는 구조를 그대로 재현(S3 4버킷 + ALB 라우팅), DynamoDB 3테이블(GSI 포함)·IP 화이트리스트 접근제어 구성
- **비용과 제약이 걸린 판단 3건을 근거로 결정** — ACM 와일드카드가 한 레벨만 매칭한다는 점(RFC 6125)을 실제 인증서로 검증해 **인증서 추가 발급 비용을 사전 차단**, 계정 분리 대신 **단일 계정 + 네이밍·태그 분리**로 cross-account 관리 부담 제거, WAF를 붙일 수 없는 요금제 제약은 **CloudFront Functions로 IP 접근제어를 대체 구현**
- **IAM 최소권한 설계** — STG 전용 역할을 분리해, 개발자가 **운영 리소스는 조회만 가능**하도록 통제
- **5일간 원인 미상이던 도메인 이슈 규명** — `dig +trace`로 위임 계층을 따라가고 정상 도메인과 응답 코드를 대조(NOERROR vs NXDOMAIN)해 **상위 존의 NS 위임 레코드 누락**임을 증명. 호스팅존 네임서버를 바꿀 수 없는 AWS 제약은 **Reusable Delegation Set으로 존을 재생성**해 우회

#### 성과
- **STG 전 리소스 구축 완료** — PRD-STG 전 항목을 CLI로 대조 검증, **불일치 0건**
- **운영에서 직접 배포를 검증하던 구조를 제거** — 개발팀이 안전하게 테스트할 환경 확보
- 원인 미상으로 정체되던 이슈를 **추측이 아닌 증거로 정리**해, 발주처가 무엇을 조치해야 하는지 명확히 정의
- 구축 가이드·체크리스트·인계 문서로 **담당자가 바뀌어도 이어갈 수 있는 상태** 유지

**Tech:** AWS ECS(Fargate), ECR, CodeDeploy(Blue/Green), ALB, CloudFront, CloudFront Functions, WAF, Route 53(Reusable Delegation Set, Alias Record), ACM, S3, DynamoDB(GSI), IAM, AWS CLI, dig/DNS

---

### 🤖 AI 에이전트 실행 플랫폼 — Kubernetes 기반 격리 실행 인프라 (사내 프로젝트, 진행 중)

**2026.05 ~ 진행 중 · 클러스터 구축·GitOps 배포 파이프라인 담당**

> 스스로 코드를 수정하는 AI 에이전트를 안전하게 실행하기 위해,  
> **실행 1건을 Job 1개로 격리**하는 쿠버네티스 기반 인프라를 구축하고 있습니다.

#### 문제 상황
**위 삼성디스플레이 POC에서 이어진 과제입니다.** 그때 DevAX는 격리 인프라 없이 systemd로 구동했는데,  
에이전트가 호스트 파일을 건드려 자기 실행 환경을 망가뜨리는 일이 발생했습니다.  
에이전트에는 모델 API 키와 사내 서비스 토큰이 주입되기 때문에, 실행 단위를 격리하는 sandbox 인프라가 필요했습니다.

#### 구축 내용
- 사내 VM에 **쿠버네티스 클러스터 구축** — 기본 traefik을 ingress-nginx로 교체하고, Linkerd 서비스 메시로 서비스 간 mTLS 적용
- **에이전트 실행 1건 = Job 1개**로 격리. 전용 네임스페이스와 최소 권한 ServiceAccount를 부여하고, 실패 재실행·무한 대기·잔여 리소스를 Job 옵션으로 차단
- **egress NetworkPolicy**로 에이전트 Pod의 아웃바운드를 사내 서비스와 모델 API로만 제한해 시크릿이 밖으로 나갈 경로를 차단. API 키는 Sealed Secrets로 Git에 암호문 보관
- **ArgoCD app-of-apps**로 클러스터 상태를 Git에서 관리(Helm 차트). Bitbucket Pipelines + self-hosted runner로 배포하고, 배포 후 스모크 검증 자동 실행
- 레지스트리(Harbor·Kellnr·Verdaccio)를 전량 self-host하고, Prometheus·Grafana·Tempo로 관측성 확보

---

## Career Summary

- **총 경력:** 2년 11개월+
- **핵심 분야:** DevOps, AI Platform Infrastructure(LLM Serving), Backend Development
- **중심 역량:** CI/CD 파이프라인 구축·개선, Air-gapped(폐쇄망) 배포, Hybrid Infrastructure, 관측성(Observability), 장애 대응·RCA, 운영 절차 문서화·표준화
- **Kubernetes:** 사내 AI 에이전트 실행 플랫폼에서 쿠버네티스 클러스터(k8s) 구축 및 ArgoCD GitOps 기반 운영 — Job·NetworkPolicy·RBAC 기반 워크로드 격리 (관리형 서비스(EKS·GKE) 운영 경험은 없으며, self-managed 클러스터 구축·운영 기준)
- **전환 진행 중:** Terraform·Ansible 기반 IaC — 홈랩(Proxmox 3대) 실습 병행
- **관심 방향:** AI 플랫폼 인프라(LLM 서빙, GPU), 배포 자동화, 신뢰성 엔지니어링(SRE), 플랫폼 엔지니어링

---

## Professional Experience

### 베리드코리아
**개발팀 / 주임**  
**2024.08 ~ Present**  
**Role:** Developer · DevOps · SRE

#### 주요 업무
- 자사 블록체인 서비스(BaaS·Berith Wallet·Berith Scan)의 AWS·온프레미스 하이브리드 인프라 상시 운영 — 메인넷·부트노드 노드 운영, EC2 7대·RDS·OpenSearch, 온프레미스 이중화
- AWS(Route 53, ALB, EC2)와 온프레미스를 연동하는 하이브리드 인프라 설계·구축·운영 및 운영 절차 표준화
- Docker 기반 Web / WAS / DB 컨테이너 운영 체계 구축·운영
- AWS WAF, Nginx, iptables를 활용한 다층 보안 아키텍처 구축 및 무차별 대입·봇 트래픽 상시 대응
- 외부 헬스체크와 내부 지표를 결합한 모니터링·알림 체계 구축으로 관측성(Observability) 확보, Slack 실시간 알림 운영
- 사내 AI 에이전트 실행 플랫폼 인프라 구축 (2026.05~) — **AI가 스스로 작성한 코드를 안전하게 실행**하기 위한 격리 환경 구축. 실행 1건마다 일회용 컨테이너로 분리하고 외부로 나가는 통신을 차단해 **API 키 유출 경로 제거**, 쿠버네티스 클러스터 직접 구축 + ArgoCD GitOps 배포 자동화
- Jenkins 및 스크립트 기반 CI/CD 파이프라인 구축과 빌드·테스트·배포 자동화
- 장애 대응 시 로그 기반 근본 원인 분석(RCA) 및 재발 방지 대책 수립
- 해외 개발자 온보딩을 위한 서버 접근, 레포지토리, 배포 절차 문서화
- MCP, OpenSearch, S3, Lambda, EC2를 연동한 AI 실행 인프라 구축·운영
- 온프레미스 서버실 구축 및 VM 백업·재해복구(DR) 체계 운영
- **삼성SDR 파견 (2025.09 ~ 2026.03):** Spring MVC 기반 내방객 관리시스템 풀스택 개발, 카드사 연동 REST API 설계·개발, JBoss 배포 전략 수립
- 하나증권 AI 협업솔루션 POC 그룹웨어 어댑터 엔지니어링 — 금융권 망분리 환경 SSO/DRM/인사연동 (2026.05~07, 완료)
- 삼성디스플레이 폐쇄망 AI 플랫폼 구축 — AI POC (2026.05~06), 반입-배포 사이클 5시간+→30분 단축, 9월 후속 단계 확정
- KBS 통합재난방송시스템 STG 인프라 단독 구축 (2026.04~06) — 문서 없는 운영 계정을 CLI로 역분석해 동등 환경 재현, ECS Fargate·CodeDeploy Blue/Green, IAM 최소권한, DNS 위임 이슈 규명

#### 핵심 성과
- 하이브리드 인프라 운영 기준 정립 및 운영 절차 문서화·표준화
- 다층 보안 방어 체계로 봇 트래픽 선제 차단(하루 평균 1,000개 이상 IP) — **AWS 비용 20% 이상 절감**, 서비스 안정성 확보
- 모니터링·알림 자동화로 **장애 트러블슈팅 소요 시간 1주일 → 30분 이내 단축**
- 이중화 구성 일부 온프레미스 이관으로 AWS 비용 추가 절감
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
- 폐쇄망(망분리) 환경에서 AI 서비스 스택(LLM 게이트웨이·Text-to-SQL·보안성검토 에이전트·STT) 오프라인 배포·기동 경험
- 오프라인 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 사전 빌드, 물리 반입(내부망 반입 프로세스) 절차 설계
- LLM 게이트웨이(litellm)·IBM watsonx API 연동 구성, **CPU 아키텍처(ARM↔x86_64) 불일치** 등 오프라인 배포 특화 트러블슈팅
- 제한된 GPU 자원에서 로컬 서빙과 원격 API 위임을 나누는 **워크로드 배치 판단** 경험

### Kubernetes & GitOps
- **쿠버네티스 클러스터 직접 구축·운영** — ingress-nginx 교체 구성, Linkerd 서비스 메시(mTLS), Sealed Secrets, Prometheus·Grafana·Tempo·OpenTelemetry 관측성 스택
- **ArgoCD app-of-apps GitOps** — 클러스터 상태를 Git 단일 소스로 선언적 관리, 서비스별 Helm 차트와 Bitbucket Pipelines + self-hosted runner 연동
- **워크로드 격리 설계 적용** — 실행 1건 = Job 1개, 전용 네임스페이스·ServiceAccount·최소 권한 RBAC, egress NetworkPolicy 화이트리스트로 시크릿 반출 경로 차단
- kubeadm으로 컨트롤플레인·워커 클러스터를 직접 구축한 경험 — 관리형 서비스에 가려진 클러스터 내부 구조를 손으로 익힘
- (관리형 쿠버네티스(EKS·GKE) 운영 경험은 없으며, self-managed 클러스터를 컨트롤플레인부터 직접 구성한 경험 기준)

### IaC (전환 진행 중)
- 물리 서버 3대에 Proxmox 프라이빗 클라우드를 직접 구축하고, Terraform(VM 프로비저닝) + Ansible(k8s 설치·설정)로 **클러스터 전체를 명령 두 번으로 재현**하는 IaC 전환 진행

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

### 폐쇄망 AI 플랫폼 구축
USB 반입이 단방향인 폐쇄망에 AI 서비스 5종을 배포하면서, 실패 비용이 비대칭인 조건에서  
**"내부에서는 빌드하지 않는다"** 로 전략을 바꿔 반입-배포 사이클을 **5시간+ → 30분으로 단축**했습니다.

### 운영 환경 역분석 기반 스테이징 구축
아는 사람도 문서도 없는 운영 AWS 계정을 CLI로 역분석해 **동등한 스테이징 환경을 혼자 구축**하고,  
PRD-STG 전 항목을 대조 검증해 **불일치 0건**으로 인계했습니다.  
5일간 멈춰 있던 도메인 이슈는 `dig +trace` 계층 추적과 정상 도메인 응답 코드 대조로 **원인이 어디에 있는지 증거로 증명**했습니다.

### DDoS 대응체계 구축
AWS WAF, Nginx, iptables를 결합한 **3계층 방어 아키텍처**로  
일 50GB 이상의 공격 로그를 남기던 무차별 대입·봇 트래픽을 **하루 평균 1,000개 이상 IP 자동 차단**으로 선제 대응하여, **AWS 비용을 20% 이상 절감**하고 핵심 API의 안정성을 확보했습니다.

### 모니터링 · 알림 체계 구축
Prometheus, Grafana, Alertmanager, Blackbox Exporter 기반  
외부 헬스체크 결합 모니터링과 Slack 실시간 알림으로 **장애 트러블슈팅 소요 시간을 1주일에서 30분 이내로** 단축했습니다.

### Kubernetes 기반 AI 에이전트 격리 실행 인프라
쿠버네티스 클러스터(k8s)에서 **에이전트 실행 1건을 Job 1개로 격리**하고,  
전용 ServiceAccount·최소 권한 RBAC와 **egress NetworkPolicy 화이트리스트**로 시크릿 반출 경로를 차단했습니다.  
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
AWS, Route 53(Reusable Delegation Set, Alias Record), ACM, ALB, EC2, ECS(Fargate), ECR, CodeDeploy(Blue/Green), CloudFront, CloudFront Functions, Lambda, VPC, WAF, CloudWatch, OpenSearch, S3, DynamoDB(GSI), IAM, AWS CLI

### AI / LLM Infrastructure
litellm(LLM Gateway), IBM watsonx, MCP, 오프라인 모델·패키지 번들링(deb/wheel/Docker/Yarn Berry), GPU 드라이버 반입

### Container / Orchestration / IaC
Docker, Kubernetes(k8s·kubeadm), Helm, ArgoCD(GitOps·app-of-apps), Linkerd(mTLS), NetworkPolicy·RBAC·Sealed Secrets, Harbor, Terraform, Ansible, Proxmox

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
