---
layout: page
title: Gwonhee Han — DevOps Engineer
subtitle: Resume
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
  <p class="name">Gwonhee Han</p>
  <p class="role">DevOps Engineer · SRE</p>
  <p class="contact">
    lsfguni@gmail.com · Seoul, South Korea<br>
    Portfolio <a href="https://lsfguni.github.io/">lsfguni.github.io</a> ·
    Full CV <a href="https://lsfguni.github.io/career-en/">lsfguni.github.io/career-en</a> ·
    GitHub <a href="https://github.com/lsfGuni">github.com/lsfGuni</a>
  </p>
</div>

## Summary

DevOps engineer with 3 years of experience, starting in Spring backend development and moving into **hybrid AWS/on-premise operations, CI/CD, observability and security response**.
**Sole infrastructure owner** for a blockchain service platform, where I moved every service off AWS onto in-house hardware and cut monthly spend by **78%**.
Most of my work has been in environments where the usual tools are unavailable — air-gapped facilities, segmented financial networks, undocumented production accounts. I don't stop at restoring service: root cause, fix, then documentation.

## Core Strengths

- **Cloud-to-on-premise migration & FinOps** — planned and executed a full migration off AWS from the cost structure up, including replacing the AWS edge (Route 53, ALB, WAF) with Cloudflare Tunnel
- **Air-gapped delivery** — offline deployment of an AI service stack with no internet or package registry; multi-architecture builds and offline bundling
- **Kubernetes & GitOps** — k3s cluster built from scratch, ArgoCD app-of-apps, workload isolation by namespace, ServiceAccount and RBAC *(self-managed only; no managed EKS/GKE experience)*
- **Observability & incident response** — Prometheus, Grafana, Alertmanager and Blackbox Exporter; log-based root cause analysis and prevention
- **Security** — layered defense across WAF, Nginx and iptables; non-invasive diagnosis in access-controlled financial environments

## Experience

### Berith Korea <span class="meta">| DevOps · SRE · sole infrastructure owner | Feb 2025 – Present</span>

Sole owner of the infrastructure behind the company's blockchain services (BaaS, wallet, chain explorer), migrated from AWS to in-house hardware.

- Inherited the platform with no handover; built monitoring and alerting from nothing and documented an RCA for every failure, **cutting incident troubleshooting from about a week to under 30 minutes**
- As attacks evolved from a single bot to rotating IPs, hardened a **three-layer defense across WAF, Nginx and iptables** — **auto-blocking 1,000+ IPs per day** out of 50GB of daily attack logs
- Traced repeated mainnet node crashes under transaction spikes to **disk I/O contention and chain data growth**, then split traffic across on-premise nodes — resolved **without buying hardware**
- **Migrated the platform off AWS onto in-house hardware — $1,497 → ~$330/month (−78%).** Replaced the entire AWS edge (Route 53, 8 ALBs, WAF, reverse-proxy EC2) with **Cloudflare Tunnel**, eliminating inbound firewall exposure. Migration order followed risk, rollback was secured before every cutover — 8 domain cutovers, zero regressions
- **Built a two-tier self-healing system for an unstaffed platform** — 11 local watchdogs plus 2 host supervisors, judging health by whether data advances rather than whether the process is up, after indexing once stalled 5 days while reporting healthy
- **Building a Kubernetes (k3s) isolation platform** — one Job per agent execution with a dedicated namespace, ServiceAccount and RBAC, deployed declaratively via ArgoCD app-of-apps across 14 Helm charts *(pre-launch)*
- Built CI/CD on Jenkins and scripts, ran Docker-based web/WAS/DB tiers, and set up the on-premise server room with VM backup and disaster recovery

### iBiz Software <span class="meta">| Backend Developer · DevOps (project contract) | Aug 2024 – Jan 2025</span>

Affiliate of Berith Korea (same site, separate entity); joined Berith Korea full-time in Feb 2025.

- NIPA government blockchain project — sole owner of the backend and infrastructure for a **pharmaceutical traceability system**
- Designed and built Spring Boot REST APIs consumed by a Flutter mobile app (built by a dedicated iOS developer)
- Built the admin console (Thymeleaf), modeled the MariaDB schema, and developed blockchain-backed history recording and lookup features
- Built and operated the AWS EC2 servers and deployment automation

### iBank Consultants <span class="meta">| Developer | Sep 2023 – Jul 2024</span>

- Full-stack development on React, Thymeleaf and Spring Boot
- **Introduced the team's first CI/CD pipeline** (GitLab + Jenkins), replacing manual builds and deployments
- **Led the migration from SVN to Git**, including branching conventions and internal training
- Supported pre-sales: customer meetings, demos, screen and functional specifications

## Selected Projects

- **Air-gapped AI platform, Samsung Display** (2026, sole infrastructure engineer) — deployed five AI services into a facility with no internet and one-way USB transfer. Eliminating the causes of re-entry, starting with an ARM ↔ x86_64 architecture mismatch, cut one cycle from **5+ hours to 30 minutes (~90%)**. Next phase confirmed for September 2026
- **Staging for a national disaster broadcasting system** (2026, sole engineer) — built staging equivalent to production for a public service that had none: ECS Fargate with CodeDeploy blue/green, 7-path CloudFront routing, least-privilege IAM. **Every resource compared via CLI — zero mismatches**
- **Groupware SSO/DRM adapter in a segmented financial network, Hana Securities** (2026) — isolated integration failures hop by hop across five vendors. **Launched on schedule with no open issues**
- **Home lab private cloud & IaC** (personal, ongoing) — Proxmox across three physical servers, with Terraform and Ansible reproducing the whole cluster in two commands

## Technical Environment

<div class="stack" markdown="1">
**Cloud** AWS (EC2, ECS Fargate, ECR, CodeDeploy, ALB, CloudFront, CloudFront Functions, Route 53, ACM, S3, DynamoDB, Lambda, VPC, WAF, CloudWatch, OpenSearch, IAM)
**Containers · Orchestration** Docker, Kubernetes (k3s), Helm, ArgoCD, Linkerd, NetworkPolicy, RBAC, Harbor
**IaC · Automation** Terraform, Ansible, Proxmox, Jenkins, GitLab CI, Bitbucket Pipelines
**Observability** Prometheus, Grafana, Alertmanager, Blackbox Exporter, OpenTelemetry, Tempo
**Server · Network** Linux, Nginx, Apache, Tomcat, iptables, WireGuard
**AI infrastructure** litellm, IBM watsonx, MCP, offline model and package bundling
**Backend · Data** Java, Spring, JavaScript / Oracle, MySQL, MariaDB, Redis
</div>

## Education

**Chung-Ang University** — B.A. in Economics

</div>
