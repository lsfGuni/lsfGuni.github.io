---
layout: page
title: Career
subtitle: DevOps Engineer — infrastructure that holds up under constraints
---

<p style="text-align:right; font-size:0.9rem;"><a href="{{ '/resume-en/' | relative_url }}">Resume (2-page) →</a> · <a href="{{ '/career/' | relative_url }}">한국어 →</a></p>

<style>
  .iso-btn { display:inline-block; padding:7px 15px; border-radius:8px; font-size:0.85rem; font-weight:600;
             text-decoration:none; background:#0b1b3a; color:#7dd3fc !important; border:1px solid #1e3a6a; }
  .iso-btn:hover { background:#12264f; color:#bae6fd !important; text-decoration:none; }
</style>

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

I'm **Gwonhee Han**, a DevOps engineer. I build and operate infrastructure that has to keep working under constraints — no internet access, no handover documentation, and often no second engineer.

I started as a Spring backend developer and moved into infrastructure: Linux server operations, AWS and on-premise hybrid architecture, CI/CD pipelines, observability, security response, and incident analysis. Most of my recent work has been in environments where the usual tools are unavailable — air-gapped facilities, segmented financial networks, and undocumented production accounts.

When something breaks I don't stop at restoring service. **Root cause → fix → hardening → documentation** is the loop I work in, because the goal is that the same failure doesn't come back.

**3 years of experience · Seoul, South Korea · currently employed, open to opportunities**

---

## Current Operations

### ⛓️ Berith Blockchain Services — Migrating off AWS and Running Unattended *(completed)*

**Aug 2024 – Aug 2026 (2 yrs 1 mo) · DevOps / SRE · infrastructure owner**
*(Aug 2024 – Jan 2025 under affiliate iBiz Software; Berith Korea full-time from Feb 2025)*

> I owned the infrastructure behind a blockchain service suite (BaaS, wallet, explorer) **for two years**.
> I moved every service **off AWS onto in-house hardware** and replaced the entire AWS edge with **Cloudflare Tunnel** —
> bringing monthly spend from **$1,497 to about $330 (−78%)**.
> Because it had to run without anyone on site, I built a platform that **repairs itself**, and set it up so an
> **AI session can carry out incident response** — diagnostics and runbooks included — before handing it over.

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
  <text x="460" y="28" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Berith Infrastructure &#8212; Full Migration off the AWS Edge (Aug 2026)</text>
  <text x="460" y="46" text-anchor="middle" font-size="10.5" fill="#7F8C8D">Route 53 + 8 ALBs + WAF + reverse-proxy EC2 &#8594; Cloudflare + 2 in-house connectors</text>

  <rect x="40" y="60" width="250" height="44" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="165" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">End users &#183; BaaS enterprise clients</text>
  <text x="165" y="96" text-anchor="middle" font-size="9" fill="#DDE1E3">Wallet &#183; Explorer &#183; Samsung Display &#183; Lotte Innovate</text>

  <rect x="302" y="60" width="196" height="44" rx="8" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="400" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Desktop wallet users</text>
  <text x="400" y="96" text-anchor="middle" font-size="9" fill="#DDE1E3">Join the chain as full nodes</text>

  <rect x="510" y="60" width="200" height="44" rx="8" fill="url(#brRed)" filter="url(#brShadow)"/>
  <text x="610" y="80" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Bots &#183; credential stuffing</text>
  <text x="610" y="96" text-anchor="middle" font-size="9" fill="#FADBD8">140-200M req/mo (derived from WAF billing)</text>

  <rect x="722" y="60" width="158" height="44" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="801" y="79" text-anchor="middle" font-size="11" font-weight="700" fill="#fff">AWS monthly bill</text>
  <text x="801" y="96" text-anchor="middle" font-size="11.5" font-weight="700" fill="#fff">$1,497 &#8594; ~$330</text>

  <path d="M165,104 L165,126" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <path d="M400,104 L400,126" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <path d="M610,104 L610,126" stroke="#C0392B" stroke-width="2" marker-end="url(#brArrowR)"/>

  <rect x="30" y="132" width="860" height="96" rx="10" fill="#FEF5E7" stroke="#F5CBA7" stroke-width="1.5"/>
  <text x="46" y="152" font-size="11" font-weight="700" fill="#9C640C">Cloudflare &#8212; edge tier (replacing Route 53 + 8 ALBs + WAF)</text>

  <rect x="48" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="146" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">DNS &#183; TLS termination</text>
  <text x="146" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">5 zones &#183; auto-renewed certs</text>

  <rect x="254" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="352" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">WAF &#183; bots &#183; DDoS</text>
  <text x="352" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">per-request &#8594; flat rate (attack volume irrelevant)</text>

  <rect x="460" y="162" width="196" height="52" rx="8" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="558" y="184" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Pages + R2</text>
  <text x="558" y="201" text-anchor="middle" font-size="9" fill="#FDF2E0">Static site &#183; 119MB wallet installer</text>

  <rect x="666" y="162" width="206" height="52" rx="8" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="769" y="184" text-anchor="middle" font-size="11.5" font-weight="700" fill="#fff">Tunnel</text>
  <text x="769" y="201" text-anchor="middle" font-size="9" fill="#DFF0D8">Outbound-only &#8594; zero inbound ports</text>

  <path d="M769,214 L769,238 L460,238 L460,258" stroke="#E8890C" stroke-width="2" fill="none" marker-end="url(#brArrowO)"/>

  <rect x="230" y="262" width="460" height="66" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
  <text x="246" y="281" font-size="11" font-weight="700" fill="#186A3B">2 connectors on separate physical hosts (survives one host failure)</text>
  <rect x="246" y="288" width="200" height="32" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="346" y="308" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">cf-connector-01 (R740-2)</text>
  <rect x="458" y="288" width="216" height="32" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="566" y="308" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">cf-connector-02 (R740-1)</text>

  <path d="M460,328 L460,348" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <text x="472" y="343" font-size="9" fill="#5A6268">nginx :8080 &#8212; per-domain routing &#183; upstream health checks</text>

  <rect x="30" y="352" width="600" height="150" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="371" font-size="11" font-weight="700" fill="#1B4F72">2 in-house physical servers &#8212; 11 VMs (VirtualBox + systemd)</text>

  <rect x="46" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="114" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Wallet</text>
  <text x="114" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">zero-downtime cutover</text>

  <rect x="190" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="258" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Scan</text>
  <text x="258" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">explorer + indexing</text>

  <rect x="334" y="380" width="136" height="42" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="402" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">BaaS API &#215;2</text>
  <text x="402" y="414" text-anchor="middle" font-size="8.5" fill="#DFF0D8">2-node HA</text>

  <rect x="478" y="380" width="136" height="42" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="546" y="399" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Admin</text>
  <text x="546" y="414" text-anchor="middle" font-size="8.5" fill="#D6EAF8">rebuilt from source</text>

  <rect x="46" y="430" width="180" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="136" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Redis (replaces ElastiCache)</text>
  <text x="136" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">12 nodes &#8594; 1</text>

  <rect x="234" y="430" width="180" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="324" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">MinIO &#215;2 (replaces S3)</text>
  <text x="324" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">backup redundancy</text>

  <rect x="422" y="430" width="192" height="42" rx="7" fill="url(#brPurple)" filter="url(#brShadow)"/>
  <text x="518" y="449" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">Elasticsearch (replaces OpenSearch)</text>
  <text x="518" y="464" text-anchor="middle" font-size="8.5" fill="#E8DAEF">54GB &#183; $262/mo recovered</text>

  <text x="46" y="490" font-size="9.5" fill="#1B4F72">5 standalone machines &#8212; 4 chain nodes (1 RPC &#183; 2 validators &#183; 1 ETH) + Elasticsearch</text>

  <rect x="644" y="352" width="246" height="150" rx="10" fill="#FDEDEC" stroke="#E6B0AA" stroke-width="1.5"/>
  <text x="660" y="371" font-size="11" font-weight="700" fill="#943126">AWS &#8212; deliberately kept</text>

  <rect x="660" y="380" width="214" height="40" rx="7" fill="url(#brRed)" filter="url(#brShadow)"/>
  <text x="767" y="397" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">RDS (production DB)</text>
  <text x="767" y="411" text-anchor="middle" font-size="8.5" fill="#FADBD8">data tier last &#183; migration being designed</text>

  <rect x="660" y="426" width="214" height="40" rx="7" fill="url(#brOrange)" filter="url(#brShadow)"/>
  <text x="767" y="443" text-anchor="middle" font-size="10.5" font-weight="600" fill="#fff">1 boot node</text>
  <text x="767" y="457" text-anchor="middle" font-size="8.5" fill="#FDF2E0">IP hardcoded into wallet binaries</text>

  <text x="660" y="482" font-size="9" fill="#943126">Shutting it down blocks new users from the chain</text>
  <text x="660" y="495" font-size="9" fill="#943126">&#8594; ruled undecommissionable without a wallet re-release</text>

  <rect x="30" y="512" width="430" height="118" rx="10" fill="#FEF9E7" stroke="#F7DC6F" stroke-width="1.5"/>
  <text x="46" y="531" font-size="11" font-weight="700" fill="#9A7D0A">Unattended operation &#8212; designed for no on-site owner</text>
  <rect x="46" y="540" width="184" height="36" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="138" y="556" text-anchor="middle" font-size="10" font-weight="600" fill="#fff">L1 local watchdogs &#215;11</text>
  <text x="138" y="569" text-anchor="middle" font-size="8.5" fill="#DDE1E3">every 2 min &#183; self-healing</text>
  <rect x="240" y="540" width="204" height="36" rx="7" fill="url(#brGray)" filter="url(#brShadow)"/>
  <text x="342" y="556" text-anchor="middle" font-size="10" font-weight="600" fill="#fff">L2 host supervisors &#215;2</text>
  <text x="342" y="569" text-anchor="middle" font-size="8.5" fill="#DDE1E3">VM power tier + L1 liveness</text>
  <text x="46" y="594" font-size="9.5" font-weight="600" fill="#9A7D0A">Health is judged by &#8220;is data advancing&#8221; &#8212; not &#8220;is the process up&#8221;</text>
  <text x="46" y="609" font-size="9" fill="#7D6608">Changed after indexing silently stalled 5 days while the service reported active</text>
  <text x="46" y="623" font-size="9" fill="#7D6608">3 consecutive checks &#183; 30-min cooldown &#183; daily cap &#183; halt all action if a majority fails at once</text>

  <rect x="474" y="512" width="416" height="118" rx="10" fill="#EAF2F8" stroke="#85C1E9" stroke-width="1.5"/>
  <text x="490" y="531" font-size="11" font-weight="700" fill="#1A5276">3-tier backup &#8212; replacing OpenSearch's automatic S3 snapshots</text>
  <rect x="490" y="540" width="126" height="36" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="553" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">Snapshot / 6h</text>
  <text x="553" y="569" text-anchor="middle" font-size="8" fill="#D6EAF8">&#8594; MinIO #1</text>
  <path d="M616,558 L628,558" stroke="#7F8C8D" stroke-width="2" marker-end="url(#brArrow)"/>
  <rect x="632" y="540" width="126" height="36" rx="7" fill="url(#brBlue)" filter="url(#brShadow)"/>
  <text x="695" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">Mirror / 6h</text>
  <text x="695" y="569" text-anchor="middle" font-size="8" fill="#D6EAF8">&#8594; MinIO #2 (pull)</text>
  <rect x="766" y="540" width="110" height="36" rx="7" fill="url(#brGreen)" filter="url(#brShadow)"/>
  <text x="821" y="556" text-anchor="middle" font-size="9.5" font-weight="600" fill="#fff">Logical / hourly</text>
  <text x="821" y="569" text-anchor="middle" font-size="8" fill="#DFF0D8">both hosts, independent</text>
  <text x="490" y="594" font-size="9.5" font-weight="600" fill="#1A5276">Designed as a pull so the source never holds the replica's credentials</text>
  <text x="490" y="609" font-size="9" fill="#21618C">&#8594; deletion or compromise at the source cannot propagate to the copy</text>
  <text x="490" y="623" font-size="9" fill="#21618C">After the mirror logged &#8220;done&#8221; while failing for 9 days, health moved from log freshness to actual object-count comparison</text>

  <rect x="30" y="640" width="860" height="128" rx="10" fill="#F4F6F7" stroke="#D5DBDB" stroke-width="1.5"/>
  <text x="46" y="659" font-size="11" font-weight="700" fill="#2C3E50">Cost &#8212; based on actual invoices, not list-price estimates</text>

  <rect x="46" y="668" width="700" height="26" rx="5" fill="#E74C3C"/>
  <text x="56" y="686" font-size="11" font-weight="700" fill="#fff">Before &#8212; $1,497 / mo</text>
  <text x="700" y="686" font-size="9.5" fill="#FADBD8">Aug 2026 invoice</text>

  <rect x="46" y="700" width="154" height="26" rx="5" fill="#27AE60"/>
  <text x="56" y="718" font-size="11" font-weight="700" fill="#fff">Now &#8212; ~$330 / mo</text>
  <text x="212" y="718" font-size="9.5" fill="#196F3D">~78% reduction &#183; ~$14,000 / yr</text>

  <text x="46" y="742" font-size="9.5" fill="#566573">Decommissioned &#8212; 2 OpenSearch domains ($262) &#183; WAF ($104) &#183; 7 ALBs &#183; all ElastiCache &#183; 2 RDS &#183; 9 EC2 &#183; elastic IPs 23&#8594;4</text>
  <text x="46" y="757" font-size="9.5" fill="#943126">2,874GB of snapshots are retained as recovery insurance, offsetting part of this until they expire (Feb 2027). Net TCO including power and hardware depreciation is still unmeasured</text>
</svg>

#### What this was

I owned the infrastructure for **BaaS** (recording Samsung Display security pledges and Lotte Innovate
asset-custody history on-chain) and consumer services (**wallet and chain explorer**).
It ran on AWS — multiple EC2 instances, RDS and OpenSearch — including an in-house Ethereum-based mainnet,
and being a wallet, it absorbed constant credential-stuffing traffic.

Two problems had to be solved:

- **① Recurring AWS spend.** The actual invoices came to **$1,497/month** — 3.7× the "$400+" the company believed. The gap was in line items nobody tracked, including WAF at $104/month
- **② No dedicated operator.** The platform had to keep running without anyone on site

#### What I did

**Moved the entire edge to Cloudflare**

A single reverse-proxy EC2 behind Route 53 + 8 ALBs + WAF was the only entry point for every service —
and it was **Ubuntu 16.04 (EOL), 5.5 years without a reboot, with zero backups**.
Cloudflare Tunnel brought inbound firewall exposure to **zero**, with two connectors on separate physical hosts for redundancy.
Eight domains cut over one at a time, with no regressions.
Billing shifted from **per-request to flat rate**, so bot traffic no longer drives the invoice.

**Moved every service in-house**

- Wallet — replicated Redis to carry sessions across for a **zero-downtime cutover with no forced re-login**. Moving from AJP to HTTP + Nginx also **closed the exposed AJP (Ghostcat) surface**
- BaaS — rebuilt as **two-node HA** with unhealthy nodes dropped automatically
- Admin console and API docs — found both had **routing migrated but no backend for three years**, and rebuilt them from source. Two services shared the defect, so I added a step verifying "done" against a real response
- ElastiCache 12 nodes → 1 Redis · 2 OpenSearch domains → 1 Elasticsearch · S3 → 2 MinIO

**Decommissioned on evidence, not assumption**

- ElastiCache — confirmed **zero commands on both clusters across 14 days**, then swept configs and code for references
- OpenSearch — compared every index and confirmed **on-premise held equal or more**; proved the one AWS-only index was a subset by sampling
- Elastic IP releases are irreversible, so I swept every DNS zone, config and chain node for references first
- I also documented **what could not be turned off** — the boot node's **IP is compiled into wallet binaries**, so shutting it down would cut new users off from the chain

**Built self-healing for an empty chair**

Eleven local watchdogs (every 2 min) and two host supervisors (every 5 min) repair the platform without a person.
Where monitoring tools produce graphs, this system's output is **a restarted service**.

- 🔑 The key change was judging health by **"is data advancing"** rather than **"is the process up"** — after indexing stalled for **five days** while the service reported `active (running)`
- Guardrails — act only after 3 consecutive failures · 30-min cooldown · daily cap · **skip action when a dependency is unreadable** · **halt everything if a majority fails at once**. That last gate fired for real and **prevented a forced restart of all 6 VMs**

**Built a three-tier backup and proved it restores**

Migrating away from OpenSearch removed the automatic snapshots it had been taking for us.

- 6-hourly snapshots to MinIO #1, a 6-hourly mirror to MinIO #2 on a different physical host, and **hourly logical backups** of indices that cannot be re-derived, taken independently by both hosts
- Built as a **pull**, so the source never holds the replica's credentials and a deletion or compromise cannot propagate
- 🔴 **The mirror failed 36 times over 9 days while logging "done" each time.** Health moved from log freshness to **actual object-count comparison**
- **Ran a real restore drill** — "we have a backup" and "it restores" are different claims

**A call I got wrong, and reversed**

I promoted the WAF ruleset from Log to Block and **reverted within three minutes**.
Twenty-four hours of data showed zero threshold-exceeded events, but overriding the action on a managed ruleset makes
**each rule block on its own, bypassing score aggregation** — something I only confirmed by doing it.
I kept only the verified part: six false-positive-heavy rules disabled, 81% of daily log volume.

#### Results

- **AWS spend $1,497 → ~$330/month (−78%, ~$14,000/yr)** — retired 2 OpenSearch domains, WAF, 7 ALBs, all ElastiCache, 2 RDS instances, 9 EC2 instances, and 19 of 23 elastic IPs
- **Removed the single point of failure at the edge** — replaced an EOL, never-rebooted, unbacked-up proxy with two connectors on separate physical hosts
- **Incident triage from a week to under 30 minutes** — built from nothing, with monitoring, alerting and per-incident RCA writeups
- **Auto-blocking 1,000+ IPs per day**, hardened in stages as attacks moved from a single bot to rotating IPs
- **Most failures now recover before anyone notices**

#### Operational continuity

So the platform keeps running without someone on site, I focused on leaving **things that run**, not just things that are written.

- **Five operations documents** — architecture, backup, credentials, decommissioning, incident response
- **One SSH key covering all 18 in-house machines** — consolidating two key types across two accounts into a single file while leaving existing authentication intact, with deploy, verify and revoke scripts
- **An AI-driven incident-response set** — a diagnostic script covering nine areas of system state plus nine symptom-based runbooks, packaged with entry rules so **a Claude Code session reads them and executes directly**. An operator typing "the explorer is down" is still walked through **establish facts → isolate cause → act** — the rules explicitly forbid restarting on a guess
- **A log of reversed judgements** — on one day eight conclusions were overturned, so each is recorded as "previous understanding → what was actually true → evidence → impact"

---

## Featured Projects

### 🔒 Air-gapped AI Platform — Samsung Display (POC)

**May – Jun 2026 · infrastructure engineer (1 of 5 on the project)**

> Deployed five AI services and a model gateway into a facility with no internet, where **USB media can be carried in but never carried out**.
> With one missing dependency costing an entire cycle, I changed the strategy to **"never build on the inside"** and cut the transfer-to-boot cycle from **5+ hours to 30 minutes**.

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
  <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Air-gapped AI Platform — transfer pipeline &amp; services</text>

  <rect x="30" y="48" width="860" height="112" rx="10" fill="#FFF7E6" stroke="#F0AD4E" stroke-width="1.5" stroke-dasharray="6 4"/>
  <text x="46" y="68" font-size="11" font-weight="700" fill="#B9770E">Internet side (outside the facility)</text>
  <rect x="55" y="80" width="205" height="62" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
  <text x="157" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">Personal laptop</text>
  <text x="157" y="124" text-anchor="middle" font-size="10" fill="#DDE1E3">Built offsite over LTE tethering</text>
  <path d="M262,111 L306,111" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <rect x="315" y="80" width="255" height="62" rx="8" fill="url(#agOrange)" filter="url(#agShadow)"/>
  <text x="442" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">Ready-to-run images · offline bundles</text>
  <text x="442" y="124" text-anchor="middle" font-size="10" fill="#FDF2E0">Target arch pinned: linux/amd64</text>
  <path d="M572,111 L616,111" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <rect x="625" y="80" width="230" height="62" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
  <text x="740" y="105" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">USB load · physical carry-in</text>
  <text x="740" y="124" text-anchor="middle" font-size="10" fill="#DDE1E3">One-way — nothing comes back out</text>

  <path d="M20,182 L900,182" stroke="#C0392B" stroke-width="2" stroke-dasharray="8 5"/>
  <text x="30" y="176" font-size="11" font-weight="700" fill="#C0392B">Air gap</text>
  <text x="898" y="176" text-anchor="end" font-size="10.5" fill="#C0392B">One missing dependency = the whole cycle repeats → “never build on the inside”</text>
  <path d="M740,144 L740,202" stroke="#C0392B" stroke-width="2" marker-end="url(#agArrowR)"/>

  <rect x="30" y="208" width="700" height="360" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="228" font-size="11" font-weight="700" fill="#1B4F72">One air-gapped workstation · 16GB VRAM GPU</text>

  <rect x="48" y="246" width="118" height="44" rx="8" fill="url(#agGray)" filter="url(#agShadow)"/>
  <text x="107" y="273" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">User</text>
  <path d="M107,292 L107,324" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

  <rect x="48" y="330" width="118" height="58" rx="8" fill="url(#agPurple)" filter="url(#agShadow)"/>
  <text x="107" y="354" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">DevAX</text>
  <text x="107" y="371" text-anchor="middle" font-size="9.5" fill="#E8DAEF">Front end · entry point</text>

  <path d="M168,359 L184,359" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M184,266 L184,422" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M184,266 L196,266" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <path d="M184,318 L196,318" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <path d="M184,370 L196,370" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <path d="M184,422 L196,422" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

  <rect x="200" y="244" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
  <text x="315" y="263" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">WrenAI</text>
  <text x="315" y="279" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Text-to-SQL analytics · systemd</text>
  <rect x="200" y="296" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
  <text x="315" y="315" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Security review agent</text>
  <text x="315" y="331" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Application security review · systemd</text>
  <rect x="200" y="348" width="230" height="44" rx="7" fill="url(#agBlue)" filter="url(#agShadow)"/>
  <text x="315" y="367" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">ai-gateway</text>
  <text x="315" y="383" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Document-based security review · systemd</text>
  <rect x="200" y="400" width="230" height="44" rx="7" fill="url(#agGray)" filter="url(#agShadow)"/>
  <text x="315" y="419" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">chat-bot</text>
  <text x="315" y="435" text-anchor="middle" font-size="9.5" fill="#DDE1E3">watsonx integration &amp; deploy · Docker</text>

  <path d="M432,266 L448,266" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M432,318 L448,318" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M432,370 L448,370" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M432,422 L448,422" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M448,266 L448,432" stroke="#7F8C8D" stroke-width="2"/>
  <path d="M448,306 L466,306" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <path d="M448,432 L466,432" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>

  <rect x="468" y="276" width="162" height="60" rx="8" fill="url(#agOrange)" filter="url(#agShadow)"/>
  <text x="549" y="301" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">litellm gateway</text>
  <text x="549" y="319" text-anchor="middle" font-size="9.5" fill="#FDF2E0">Single entry for model calls</text>

  <rect x="468" y="402" width="162" height="60" rx="8" fill="url(#agGreen)" filter="url(#agShadow)"/>
  <text x="549" y="427" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">STT serving (local GPU)</text>
  <text x="549" y="445" text-anchor="middle" font-size="9.5" fill="#DFF0D8">Only self-hosted model</text>

  <text x="46" y="497" font-size="10" fill="#1B4F72">DevAX · WrenAI · security review · ai-gateway run as systemd services · chat-bot as a Docker container (image ships every dependency)</text>
  <text x="46" y="524" font-size="10" fill="#7B5BA6">At POC time DevAX ran on systemd with no isolation — agents modifying their own runtime surfaced here,</text>
  <text x="46" y="540" font-size="10" fill="#7B5BA6">   which became the starting point for the Kubernetes sandbox (one execution = one Job)</text>

  <rect x="752" y="208" width="148" height="360" rx="10" fill="#F4F6F7" stroke="#B2BABB" stroke-width="1.5" stroke-dasharray="6 4"/>
  <text x="768" y="228" font-size="11" font-weight="700" fill="#566573">Partner network</text>
  <text x="768" y="244" font-size="9.5" fill="#7F8C8D">Switch hub</text>
  <path d="M632,306 L764,306" stroke="#7F8C8D" stroke-width="2" marker-end="url(#agArrow)"/>
  <rect x="768" y="266" width="116" height="80" rx="8" fill="url(#agTeal)" filter="url(#agShadow)"/>
  <text x="826" y="300" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">IBM watsonx</text>
  <text x="826" y="318" text-anchor="middle" font-size="9.5" fill="#D6F0EE">LLM inference API</text>

  <text x="460" y="588" text-anchor="middle" font-size="10.5" fill="#566573">16GB VRAM budget → all LLM inference delegated to watsonx; the GPU is reserved for STT</text>
</svg>

**The constraint**

- No internet, no package registry, no CI/CD — `pip install` does not work, and five AI services had to run there
- One cycle is **build → load USB → carry in → boot**. Because media cannot come back out, any missing dependency found at boot meant leaving the facility and starting over. Early cycles took over five hours.
- Advance surveys were restricted, so workstation specs were unknown until arrival — and **the development machines were ARM while the assigned workstation was x86_64**, which only surfaced after carry-in

**What I did**

- **Shifted the strategy to "never build on the inside."** When failure costs are asymmetric, an internal build is the largest risk. I moved to shipping **ready-to-run images with every dependency included**, leaving only loading and boot on the inside — bringing one cycle down to **30 minutes**
- **Identified and fixed the architecture mismatch.** ARM-built images and wheels cannot execute on x86_64 (`exec format error`). I rebuilt every artifact with the target architecture pinned to `linux/amd64`
- **Placed workloads against a single 16GB VRAM GPU.** Not every model fit locally, so **all LLM inference was delegated to the watsonx API and the GPU was reserved for speech-to-text**, with litellm as the single entry point for model calls
- **Chose the deployment form per service** — four long-running services as systemd units, and the on-site developer's chat-bot as a container, where I owned the watsonx integration
- No build environment was provided outside either, so I **took personal hardware offsite and built over LTE tethering** to keep the pipeline moving
- Built trust with skeptical on-site stakeholders first, then mediated between the client PM and the existing development team to get the project back on track

**Results**

- **POC completed** — all services demonstrated working; a positive executive review confirmed the **next phase for September 2026**
- Transfer-to-deploy cycle **5+ hours → 30 minutes (~90% reduction)**
- Deployed and operated all five services plus the gateway **end to end**
- **This created the next project.** DevAX ran on systemd with no isolation here, and agents modifying their own runtime surfaced as a real problem — which led directly to the Kubernetes sandbox below

**Tech:** litellm (LLM gateway), IBM watsonx API, WrenAI, local STT serving, Docker (multi-arch builds), systemd, Linux (x86_64), GPU/CUDA, offline bundling (deb / wheel / Docker / Yarn Berry)

---

### 🏦 Groupware Adapter in a Segmented Financial Network — Hana Securities (POC)

**May – Jul 2026 · adapter engineer (team of 6) · launched 15 Jul 2026**

> From an external SaaS through to internal SSO and DRM applications, **every hop of this path belonged to a different vendor**.
> I isolated integration failures **hop by hop with evidence** and drove the fixes across all parties.

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
  <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Segmented Financial Network — isolating the failing hop</text>

  <rect x="30" y="48" width="860" height="150" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="68" font-size="11" font-weight="700" fill="#1B4F72">Integration path — every hop owned by a different vendor, and no one saw the whole flow</text>

  <rect x="44" y="80" width="152" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
  <text x="120" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Dooray</text>
  <text x="120" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">External groupware SaaS</text>
  <text x="120" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">Groupware vendor</text>
  <path d="M198,108 L218,108" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="222" y="80" width="122" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
  <text x="283" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">VPN</text>
  <text x="283" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">Cross-network hop</text>
  <text x="283" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">VPN vendor</text>
  <path d="M346,108 L366,108" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="370" y="80" width="152" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
  <text x="446" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Hana Securities infra</text>
  <text x="446" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">DNS · firewall · HA</text>
  <text x="446" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">Infra team · HA vendor</text>
  <path d="M524,108 L544,108" stroke="#7B5BA6" stroke-width="2" marker-end="url(#hnArrowP)"/>

  <rect x="548" y="76" width="176" height="64" rx="8" fill="url(#hnPurple)" stroke="#5B3E85" stroke-width="2.5" filter="url(#hnShadow)"/>
  <text x="636" y="100" text-anchor="middle" font-size="12.5" font-weight="700" fill="#fff">SSO · DRM adapter</text>
  <text x="636" y="117" text-anchor="middle" font-size="9" fill="#E8DAEF">Install &amp; runtime scripts</text>
  <text x="636" y="131" text-anchor="middle" font-size="9" fill="#E8DAEF">Spring Boot</text>
  <text x="636" y="152" text-anchor="middle" font-size="9.5" font-weight="700" fill="#6C3483">My scope</text>
  <path d="M726,108 L746,108" stroke="#7B5BA6" stroke-width="2" marker-end="url(#hnArrowP)"/>

  <rect x="750" y="80" width="126" height="56" rx="8" fill="url(#hnGray)" filter="url(#hnShadow)"/>
  <text x="813" y="104" text-anchor="middle" font-size="12" font-weight="600" fill="#fff">Internal SSO/DRM</text>
  <text x="813" y="121" text-anchor="middle" font-size="9" fill="#DDE1E3">In-house application</text>
  <text x="813" y="152" text-anchor="middle" font-size="9" fill="#5D6D7E">Solution vendor</text>

  <text x="46" y="184" font-size="9.5" fill="#1B4F72">With no one owning the whole path, every incident stalled at "not our side" — so I cut the path into hops and produced evidence for each</text>

  <rect x="30" y="214" width="860" height="132" rx="10" fill="#F4ECF7" stroke="#BB8FCE" stroke-width="1.5"/>
  <text x="46" y="234" font-size="11" font-weight="700" fill="#6C3483">Per-hop verification loop — repeated until the cause narrows</text>

  <rect x="48" y="246" width="160" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
  <text x="128" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">1. Check configs</text>
  <text x="128" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">Compare each owner's setup</text>
  <path d="M208,270 L226,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="230" y="246" width="140" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
  <text x="300" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">2. Send test request</text>
  <text x="300" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">One hop at a time</text>
  <path d="M370,270 L388,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="392" y="246" width="140" height="48" rx="7" fill="url(#hnBlue)" filter="url(#hnShadow)"/>
  <text x="462" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">3. Analyze logs</text>
  <text x="462" y="282" text-anchor="middle" font-size="9" fill="#D6EAF8">Did it arrive?</text>
  <path d="M532,270 L550,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="554" y="246" width="150" height="48" rx="7" fill="url(#hnPurple)" filter="url(#hnShadow)"/>
  <text x="629" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">4. Isolate the hop</text>
  <text x="629" y="282" text-anchor="middle" font-size="9" fill="#E8DAEF">Evidence in hand</text>
  <path d="M704,270 L722,270" stroke="#7F8C8D" stroke-width="2" marker-end="url(#hnArrow)"/>

  <rect x="726" y="246" width="146" height="48" rx="7" fill="url(#hnGreen)" filter="url(#hnShadow)"/>
  <text x="799" y="266" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">5. Request the fix</text>
  <text x="799" y="282" text-anchor="middle" font-size="9" fill="#DFF0D8">Evidence to that vendor</text>

  <path d="M799,294 L799,314 L128,314 L128,296" stroke="#7B5BA6" stroke-width="1.8" stroke-dasharray="5 4" fill="none" marker-end="url(#hnArrowP)"/>
  <text x="460" y="330" text-anchor="middle" font-size="9.5" fill="#6C3483">If unresolved, move to the next hop and repeat — weekly sync to align vendors on issues and schedule</text>

  <rect x="30" y="362" width="860" height="118" rx="10" fill="#E9F7EF" stroke="#A9DFBF" stroke-width="1.5"/>
  <text x="46" y="382" font-size="11" font-weight="700" fill="#186A3B">Case — building evidence non-invasively where server access was restricted</text>
  <text x="46" y="404" font-size="9.5" fill="#145A32">SSO init failed in production → located the failing connection in adapter logs → tested name resolution and port reachability separately →</text>
  <text x="46" y="421" font-size="9.5" fill="#145A32">split into two causes, unresolved DNS and a closed firewall port → each team received the exact fix with evidence</text>
  <text x="46" y="448" font-size="11" font-weight="700" fill="#1E8449">Result — all tests passed, launched on schedule 2026-07-15 with no open issues</text>
  <text x="46" y="468" font-size="9.5" fill="#145A32">Traced communication across application, OS and network layers, and ran the diagnosis and coordination process across vendors</text>
</svg>

**The problem**

- I built the SSO/DRM adapter for groupware SaaS integration. Communication failed somewhere along **external SaaS → VPN → client infrastructure → SSO/DRM adapter → internal SSO/DRM applications**
- Each hop was owned by a different company — groupware vendor, VPN vendor, the client's infrastructure team, an HA vendor, the internal solution vendor — and **no single party could see the whole flow**, so the investigation stalled

**How I resolved it**

- Built the adapter installation and runtime scripts
- Split the full path into hops and ran a repeating loop: **check each owner's configuration → send a test request → analyze logs → isolate the failing hop → hand that vendor the evidence and the required fix**
- Where server access was restricted, I produced evidence **non-invasively** — for example, an SSO initialization failure in production was split into two causes, unresolved DNS and a closed firewall port, each handed to the responsible team
- Coordinated the HA vendor, VPN vendor, the client's infrastructure and business teams through weekly syncs

**Results**

- All tests passed, **launched on schedule (15 Jul 2026) with no open issues**
- Integration failures spanning five organizations were resolved hop by hop **without slipping the schedule**
- Gained experience diagnosing communication across application, OS and network layers, and running that process across vendors

---

### 📡 Staging Environment for a National Disaster Broadcasting System — KBS

**Apr – Jun 2026 · infrastructure engineer**

> A public service that existed only in production, with no environment to verify changes.
> I built **staging equivalent to production** and handed it over with **zero mismatches** after comparing every resource via CLI.

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
  <text x="460" y="30" text-anchor="middle" font-size="17" font-weight="700" fill="#2C3E50">Disaster Broadcasting STG — staging built to match production</text>

  <rect x="30" y="48" width="860" height="122" rx="10" fill="#F4ECF7" stroke="#BB8FCE" stroke-width="1.5"/>
  <text x="46" y="68" font-size="11" font-weight="700" fill="#6C3483">Entry tier — single domain</text>

  <rect x="48" y="80" width="140" height="58" rx="8" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="118" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">Users · dev team</text>
  <text x="118" y="124" text-anchor="middle" font-size="9.5" fill="#DDE1E3">Public disaster pages</text>
  <path d="M188,109 L206,109" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

  <rect x="211" y="80" width="180" height="58" rx="8" fill="url(#kbPurple)" filter="url(#kbShadow)"/>
  <text x="301" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">Route 53</text>
  <text x="301" y="124" text-anchor="middle" font-size="9.5" fill="#E8DAEF">STG domain alias records</text>
  <path d="M391,109 L409,109" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

  <rect x="414" y="80" width="205" height="58" rx="8" fill="url(#kbPurple)" filter="url(#kbShadow)"/>
  <text x="516" y="106" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">CloudFront</text>
  <text x="516" y="124" text-anchor="middle" font-size="9.5" fill="#E8DAEF">7 path behaviors</text>

  <path d="M619,98 L640,92" stroke="#7F8C8D" stroke-width="1.5" stroke-dasharray="4 3" marker-end="url(#kbArrow)"/>
  <path d="M619,120 L640,137" stroke="#7F8C8D" stroke-width="1.5" stroke-dasharray="4 3" marker-end="url(#kbArrow)"/>

  <rect x="644" y="72" width="228" height="40" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
  <text x="758" y="90" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">CloudFront Functions</text>
  <text x="758" y="105" text-anchor="middle" font-size="9" fill="#D4EFEC">IP allow-list — stand-in for WAF</text>

  <rect x="644" y="118" width="228" height="40" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
  <text x="758" y="136" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">ACM certificate</text>
  <text x="758" y="151" text-anchor="middle" font-size="9" fill="#D4EFEC">Wildcard matches one label — verified</text>

  <rect x="30" y="186" width="860" height="176" rx="10" fill="#E8F6F3" stroke="#A2D9CE" stroke-width="1.5"/>
  <text x="46" y="206" font-size="11" font-weight="700" fill="#117A65">Content routing — three services share one domain (7 paths total)</text>

  <rect x="48" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="143" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">v1 default path</text>
  <text x="143" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">Static pages</text>
  <path d="M143,264 L143,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
  <rect x="48" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
  <text x="143" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 bucket</text>
  <text x="143" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">Static origin</text>

  <rect x="252" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="347" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">v2 (Next.js)</text>
  <text x="347" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">New front end</text>
  <path d="M347,264 L347,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
  <rect x="252" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
  <text x="347" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 bucket</text>
  <text x="347" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">Build output</text>

  <rect x="456" y="220" width="190" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="551" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Separate portal</text>
  <text x="551" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">Independent content</text>
  <path d="M551,264 L551,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
  <rect x="456" y="294" width="190" height="46" rx="7" fill="url(#kbTeal)" filter="url(#kbShadow)"/>
  <text x="551" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">S3 bucket</text>
  <text x="551" y="331" text-anchor="middle" font-size="9" fill="#D4EFEC">Portal origin</text>

  <rect x="660" y="220" width="210" height="44" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="765" y="240" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">API · dynamic requests</text>
  <text x="765" y="255" text-anchor="middle" font-size="9" fill="#DDE1E3">Handled by the app</text>
  <path d="M765,264 L765,290" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>
  <rect x="660" y="294" width="210" height="46" rx="7" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
  <text x="765" y="315" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Forwarded to ALB</text>
  <text x="765" y="331" text-anchor="middle" font-size="9" fill="#D6EAF8">To the runtime tier</text>

  <text x="46" y="354" font-size="9.5" fill="#117A65">4 S3 buckets — CloudFront behaviors route each path to its origin, reproducing production exactly</text>

  <rect x="30" y="378" width="860" height="190" rx="10" fill="#EBF5FB" stroke="#AED6F1" stroke-width="1.5"/>
  <text x="46" y="398" font-size="11" font-weight="700" fill="#1B4F72">Runtime · zero-downtime deploy</text>

  <rect x="48" y="412" width="200" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
  <text x="148" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">ALB</text>
  <text x="148" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Dual listeners 443 / 444</text>
  <path d="M248,440 L266,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

  <rect x="271" y="412" width="155" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
  <text x="348" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">2 target groups</text>
  <text x="348" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Blue / Green</text>
  <path d="M426,440 L444,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

  <rect x="449" y="412" width="198" height="56" rx="8" fill="url(#kbBlue)" filter="url(#kbShadow)"/>
  <text x="548" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">ECS Fargate</text>
  <text x="548" y="455" text-anchor="middle" font-size="9.5" fill="#D6EAF8">Task definition matched to prod</text>
  <path d="M647,440 L663,440" stroke="#7F8C8D" stroke-width="2" marker-end="url(#kbArrow)"/>

  <rect x="665" y="412" width="205" height="56" rx="8" fill="url(#kbOrange)" filter="url(#kbShadow)"/>
  <text x="767" y="437" text-anchor="middle" font-size="12.5" font-weight="600" fill="#fff">DynamoDB — 3 tables</text>
  <text x="767" y="455" text-anchor="middle" font-size="9.5" fill="#FDF2E0">GSIs included · key schema rebuilt</text>

  <rect x="48" y="496" width="150" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
  <text x="123" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">Jenkins</text>
  <text x="123" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">Deploy pipeline</text>
  <path d="M198,520 L216,520" stroke="#449D44" stroke-width="2" marker-end="url(#kbArrowG)"/>

  <rect x="221" y="496" width="140" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
  <text x="291" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">ECR</text>
  <text x="291" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">Image registry</text>
  <path d="M361,520 L379,520" stroke="#449D44" stroke-width="2" marker-end="url(#kbArrowG)"/>

  <rect x="384" y="496" width="205" height="48" rx="7" fill="url(#kbGreen)" filter="url(#kbShadow)"/>
  <text x="486" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">CodeDeploy</text>
  <text x="486" y="532" text-anchor="middle" font-size="9" fill="#DFF0D8">Blue/Green — listener swap, no downtime</text>
  <path d="M486,496 L486,480 L348,480 L348,470" stroke="#449D44" stroke-width="1.8" stroke-dasharray="5 4" fill="none" marker-end="url(#kbArrowG)"/>

  <rect x="665" y="496" width="205" height="48" rx="7" fill="url(#kbGray)" filter="url(#kbShadow)"/>
  <text x="767" y="516" text-anchor="middle" font-size="11.5" font-weight="600" fill="#fff">IAM least privilege</text>
  <text x="767" y="532" text-anchor="middle" font-size="9" fill="#DDE1E3">STG-only role · read-only on prod</text>

  <rect x="30" y="584" width="860" height="102" rx="10" fill="#FEF9E7" stroke="#F7DC6F" stroke-width="1.5"/>
  <text x="46" y="604" font-size="11" font-weight="700" fill="#9A7D0A">Three decisions made under constraints</text>
  <text x="46" y="625" font-size="9.5" fill="#5D4E07">1. Verified with a real certificate that ACM wildcards match only one label (RFC 6125), heading off the cost of extra certificates</text>
  <text x="46" y="643" font-size="9.5" fill="#5D4E07">2. Kept a single account with naming and tag separation instead of splitting accounts, removing cross-account overhead</text>
  <text x="46" y="661" font-size="9.5" fill="#5D4E07">3. WAF was unavailable on the plan, so IP access control was implemented with CloudFront Functions</text>
  <text x="46" y="681" font-size="9.5" font-weight="600" fill="#1E8449">Every resource compared prod vs staging via CLI — zero mismatches</text>
</svg>

**The problem**

Front-end changes and back-end deployments had to be verified directly in production, on a public-facing disaster information service. The operations contact told me production existed but staging never had, and that they wanted one built. There was no detailed configuration documentation, so reproducing an equivalent environment meant reading the actual resources with the AWS CLI.

**What I did**

- **Mapped the production configuration** — enumerated every resource via AWS CLI to recover ECS task definitions, ALB listeners, CloudFront behaviors, DynamoDB key schemas and VPC subnets, then sequenced the build from that
- **Built zero-downtime deployment on ECS Fargate + CodeDeploy blue/green** — dual ALB listeners, two target groups, ECR integration, verified end to end through the Jenkins pipeline
- **Reproduced 7-path CloudFront routing** — v1, v2 (Next.js) and a separate portal sharing one domain across 4 S3 buckets plus ALB routing, with 3 DynamoDB tables (including GSIs) and IP-based access control
- **Made three decisions under constraints** — verified with a real certificate that ACM wildcards match only one label (RFC 6125), **heading off the cost of additional certificates**; kept a **single account with naming and tag separation** rather than splitting accounts; and implemented IP access control with **CloudFront Functions** where WAF was unavailable on the plan
- **Designed least-privilege IAM** — a staging-only role that leaves developers read-only on production

**Results**

- **Staging built in full** — every item compared against production via CLI, **zero mismatches**
- **Removed the practice of verifying deployments in production**
- Left build guides, checklists and reference documentation so the work survives a change of owner

**Tech:** AWS ECS (Fargate), ECR, CodeDeploy (blue/green), ALB, CloudFront, CloudFront Functions, Route 53, ACM, S3, DynamoDB (GSI), IAM, AWS CLI

---

### 🤖 AI Agent Execution Platform — Kubernetes Isolation *(internal, build complete)*

**May 2026 – Aug 2026 · cluster build and GitOps pipeline**

> Built to solve the problem the Samsung POC exposed: **agents modifying their own runtime**.
> Every agent execution runs as **one Kubernetes Job**, isolated.

**Background**

In the POC above, DevAX ran on systemd with no isolation, and an agent damaged its own runtime by writing to host files. Agents are injected with model API keys and internal service tokens, so the execution unit needed a sandbox.

**What I built**

- **k3s cluster from scratch** — control plane and worker separated on internal VMs, the default traefik replaced with ingress-nginx, Linkerd service mesh for mTLS between services
- **One execution = one Job** — a dedicated namespace (`agent-jobs`) and ServiceAccount per execution, with `backoffLimit=0` (no retry — agent work is not idempotent), `activeDeadlineSeconds` (no infinite wait) and `ttlSecondsAfterFinished` (no leftover Jobs)
- **ArgoCD app-of-apps GitOps** — one root Application managing 18 children, 14 Helm charts deployed declaratively from a single Git source, wired to Bitbucket Pipelines with a self-hosted runner
- **Three self-hosted registries** — Harbor (images), Kellnr (Rust crates), Verdaccio (npm)
- **28 architecture decision records** covering Linkerd adoption, app-of-apps finalizer conventions, sealed secrets and multi-tenancy schema separation

#### Interactive architecture diagram (built by me)

I built an isometric diagram to explain the cluster and share progress. Six modes switch the perspective, clicking a component explains its role, and **implemented / scaffolded / planned** states are color-coded so the diagram shows real progress rather than an aspiration. *(Labels are in Korean.)*

<p><a class="iso-btn" href="{{ '/assets/diagrams/k8s-iso-city.html' | relative_url }}" target="_blank" rel="noopener">🖥️ Open the interactive diagram</a></p>

**Scope delivered**

**The build and end-to-end verification were complete.** Launch was scheduled after this period, so this is not production operating experience.

- **First end-to-end agent execution completed** (29 May 2026) — all 23 automated checks passed
- **Egress NetworkPolicy is applied but intentionally disabled.** The allow-list omitted the Linkerd control plane ports (destination 8086 / policy 8090 / identity 8080), so the sidecar blocked the controller's JWKS fetch → the health port never bound → liveness failed → **`Exit 137` (SIGKILL)**. I traced it to that point, documented the conditions for re-enabling it, and it is off under management until then.
- **True isolation (microVM) and the user-facing surface are not started.** Isolation today is logical — namespace and RBAC — and container-escape-level isolation is tracked as an explicit open risk.

---

## Summary

- **Experience:** 3 years
- **Focus:** DevOps, AI platform infrastructure (LLM serving), backend development
- **Core areas:** CI/CD pipelines, air-gapped delivery, hybrid infrastructure, **FinOps-driven cloud-to-on-prem migration**, observability, incident response and RCA, operational documentation
- **Kubernetes:** built a k3s cluster and an ArgoCD app-of-apps GitOps pipeline for an internal AI agent platform — one execution per Job, isolated by namespace, ServiceAccount and RBAC. *(Self-managed clusters only; no managed Kubernetes — EKS/GKE — experience. Pre-launch, so not production operations.)*
- **In progress:** Terraform and Ansible IaC, practiced on a 3-node Proxmox home lab
- **Interested in:** AI/ML platform infrastructure (LLM serving, GPU), deployment automation, reliability and platform engineering

---

## Professional Experience

### Berith Korea — Developer · DevOps · SRE
**Feb 2025 – Present**

- **Owned the infrastructure** for the company's blockchain services (BaaS, Wallet, Explorer) — an in-house Ethereum-based mainnet, 11 VMs across 2 physical servers, and 5 standalone machines
- **Replaced the entire AWS edge — Route 53, 8 ALBs, WAF and a reverse-proxy EC2 — with Cloudflare Tunnel**, removing inbound firewall exposure and putting two connectors on separate physical hosts for redundancy
- **Migrated the platform off AWS onto in-house hardware — $1,497 → ~$330/month (−78%, ~$14,000/yr).** Sequenced by risk with the rollback path secured before each cutover; 8 domain cutovers with zero regressions. Decommissioning decisions came from measurement — 14 days of zero-traffic data, full index comparison — not assumption
- **Built a two-tier self-healing system for an unstaffed platform** — 11 local watchdogs plus 2 host supervisors, judging health by whether data advances rather than whether a process is up, after indexing once stalled 5 days while reporting healthy. Backed by a three-tier backup chain with a verified restore drill
- **Handed over five documents, a single SSH key covering all 18 in-house machines, and a working incident-response setup** so the platform can be run by someone new
- Built and ran Docker-based web / WAS / DB containers
- Built a layered security architecture across AWS WAF, Nginx and iptables, handling continuous brute-force and bot traffic
- Built monitoring and alerting that combines external health checks with internal metrics, with real-time Slack notifications
- **Building an AI agent execution platform (May 2026 – )** — a sandbox so AI-generated code can run safely: one disposable container per execution, isolated by namespace, ServiceAccount and RBAC, on a self-built Kubernetes cluster with ArgoCD GitOps
- Built CI/CD pipelines on Jenkins and scripts, automating build, test and deploy
- Log-based root cause analysis on every incident, with documented prevention measures
- Documented server access, repositories and deployment procedures to onboard overseas developers
- Built AI execution infrastructure integrating MCP, OpenSearch, S3, Lambda and EC2
- Built the on-premise server room and operate VM backup and disaster recovery
- **On-site at Samsung SDR (Sep 2025 – Mar 2026):** full-stack development of a visitor management system on Spring MVC, card-company REST API integration, JBoss deployment strategy

### iBiz Software — Backend Developer · DevOps (project contract)
**Aug 2024 – Jan 2025** *(affiliate of Berith Korea — same site; joined Berith Korea full-time in Feb 2025)*

- NIPA government blockchain project — owned the backend and infrastructure for a **pharmaceutical traceability system**
- Designed and built Spring Boot REST APIs consumed by a Flutter mobile app (built by a dedicated iOS developer)
- Built the admin console (Thymeleaf) and modeled the MariaDB schema; developed blockchain-backed history recording and lookup features
- Built and operated the AWS EC2 servers and deployment automation

### iBank Consultants — Developer
**Sep 2023 – Jul 2024**

- Full-stack development on React / Thymeleaf / Spring Boot
- Introduced CI/CD with GitLab and Jenkins
- Migrated version control from SVN to Git and ran internal training
- Supported pre-sales: customer meetings, demos, screen and functional specifications

---

## Core Strengths

**Air-gapped delivery & AI platform**
Offline deployment of an AI service stack (LLM gateway, text-to-SQL, security review agents, STT) in segregated networks. Offline bundling (deb / wheel / Docker / Yarn Berry), GPU driver preparation, physical carry-in procedure design. litellm and IBM watsonx integration, and troubleshooting specific to offline delivery such as **ARM ↔ x86_64 architecture mismatches**. Deciding what to serve locally and what to delegate remotely under a fixed GPU budget.

**Kubernetes & GitOps**
k3s cluster built from scratch — control plane and worker separated, ingress-nginx replacing traefik, Linkerd mTLS, OpenTelemetry and Tempo tracing. ArgoCD app-of-apps managing cluster state declaratively from Git, with per-service Helm charts and Bitbucket Pipelines. Workload isolation: one execution per Job with a dedicated namespace, ServiceAccount and least-privilege RBAC, plus `backoffLimit=0`, `activeDeadlineSeconds` and `ttlSecondsAfterFinished`. Traced an egress NetworkPolicy failure to a blocked service-mesh sidecar surfacing as `Exit 137`, and documented the re-enable conditions. *(Self-managed clusters; no managed Kubernetes experience.)*

**Hybrid infrastructure & FinOps**
Designing, building and operating AWS-to-on-premise infrastructure. Planning and executing a cloud-to-on-premise migration from the cost structure up — sequencing by risk, securing the rollback path before cutover, and deciding deliberately what to keep in the cloud and what to move.

**CI/CD & automation**
Jenkins, GitLab CI and Bitbucket Pipelines. AWS CodeDeploy blue/green zero-downtime deployment. Scripting repetitive work and standardizing procedures so anyone on the team can run them.

**Observability & reliability**
Prometheus, Grafana, Alertmanager, Blackbox Exporter and CloudWatch. Health checks, alerts and dashboards to shorten detection time — and alert tuning that keeps only the alerts someone can act on.

**Security & troubleshooting**
Layered defense across AWS WAF, Nginx and iptables. Root cause analysis through log analysis and request-flow tracing, followed by prevention. Non-invasive diagnosis in access-controlled financial environments.

**Collaboration**
A full-stack background that makes it easier to define infrastructure requirements with developers. Leading technical coordination and scheduling across clients, internal teams and vendors. Documentation, alert automation and onboarding guides so status is visible without asking.

---

## Technical Environment

**Cloud / Infra** — AWS: Route 53, ACM, ALB, EC2, ECS (Fargate), ECR, CodeDeploy (blue/green), CloudFront, CloudFront Functions, Lambda, VPC, WAF, CloudWatch, OpenSearch, S3, DynamoDB (GSI), IAM, AWS CLI

**AI / LLM infrastructure** — litellm (LLM gateway), IBM watsonx, MCP, offline model and package bundling, GPU driver delivery

**Containers / Orchestration / IaC** — Docker, Kubernetes (k3s), Helm, ArgoCD (GitOps, app-of-apps), Linkerd (mTLS), NetworkPolicy, RBAC, Harbor, Kellnr, Verdaccio, Terraform, Ansible, Proxmox

**Server / Network** — Linux, Ubuntu, Apache HTTP Server, Tomcat, Nginx, iptables, WireGuard

**CI/CD** — Jenkins, GitLab CI, Bitbucket Pipelines, Docker Compose, Git

**Observability** — Prometheus, Grafana, Alertmanager, Blackbox Exporter, Tempo, OpenTelemetry, CloudWatch

**Backend** — Java, JavaScript, Spring

**Data stores** — Oracle, MySQL, MariaDB, Redis

**Blockchain** — Ethereum-based in-house mainnet and boot node operations, OpenSearch chain indexing

---

## How I work

- I follow the whole flow of a service rather than looking at one piece in isolation
- Preventing recurrence matters more to me than a fast restore
- Repetitive work gets scripted and procedures get documented, so the environment is reproducible
- I don't separate development, operations and networking — it's one system

---

## Contact

**Email** — lsfguni@gmail.com
**GitHub** — [github.com/lsfGuni](https://github.com/lsfGuni)
**Portfolio** — [lsfguni.github.io](https://lsfguni.github.io/)
