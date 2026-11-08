# Awesome-Activity-Monitoring-Anomaly-Detection

# Awesome-Activity-Monitoring-Anomaly-Detection

**Top Activity Monitoring Anomaly Detection (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Behavioral Analytics, UEBA, SIEM Correlation & Self-Hosted Anomaly Detection*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Activity Monitoring & Anomaly Detection**. These tools enable security and operations teams to establish behavioral baselines, detect deviations that signal threats or incidents, and correlate anomalies across logs, metrics, and user activity—from fully managed platforms with AI-driven root cause analysis to open-source SIEMs and lightweight detectors that give teams control over their detection pipeline.



**Examples** include Datadog Security Monitoring, Splunk Enterprise Security, Sumo Logic Cloud SIEM, Dynatrace Davis AI, New Relic Alerts, Elastic Security, Rapid7 InsightIDR, Darktrace, Exabeam, and Zoho Watch (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted anomaly detection, behavioral analytics, and open SIEM infrastructure. **Critical note**: The open-source landscape splits by depth—**Wazuh** provides the most complete free SIEM with behavioral rules , **Elastic Security** adds ML anomaly detection only on paid Platinum tiers , and **Security Shallots** offers the lightest possible starting point running on a Raspberry Pi . No open-source project matches Darktrace's unsupervised network behavioral AI or Exabeam's mature UEBA, but for rule-based detection and log correlation, the options are production-proven.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global activity monitoring, SIEM, and UEBA market is valued at approximately $9.5B–$12B in 2025–2026 (with core SIEM at ~$8.4B–$12B and dedicated UEBA rapidly expanding past $4B at >35% CAGR). The sector exhibits a moderately concentrated core dominated by multi-product tech giants (Cisco/Splunk, Microsoft Sentinel, Datadog) bundled alongside a fragmented long-tail of specialized behavioral AI, niche UEBA providers, and open-source ecosystems.

## SaaS/Hosted Platforms

| Company / Product | Valuation / Revenue | Starting Price | Free Tier / Trial Limits | Key Capabilities & Trade-offs |
| :--- | :--- | :--- | :--- | :--- |
| **Datadog Security Monitoring** | **~$70B+ Market Cap** ($2.68B+ ARR) | **$15/host/mo** (Pro); **$23/host/mo** (Enterprise with ML Anomaly Detection); **$34/host/mo** (DevSecOps) | **14-day free trial** (Full platform access, no credit card required); permanent free tier capped at 5 hosts with 1-day metric retention (no security ML) | Cloud security monitoring with anomaly detection and correlation. Best for teams already using Datadog observability; trade-off is ML anomaly detection is gated to Enterprise tier and per-host infrastructure costs scale rapidly. |
| **Splunk Enterprise Security** (Cisco) | **$28B Acquisition Valuation** (~$4B Revenue) | **$759/GB/day/yr** (ES Essentials at 100–199 GB/day); **$1,783.65/GB/day/yr** (ES Premier) | **14-day free trial** for Splunk Cloud Platform (up to 5 GB/day data limit, hosted sandbox); **60-day trial** for Splunk Enterprise (500 MB/day limit, converts to perpetual free license capped at 500 MB/day without alerts/auth) | Enterprise SIEM with deep detection content and UEBA (UEBA included only in Premier). Best for large enterprises with heavy custom detection requirements; costs scale steeply with ingest volume. |
| **Zoho (ManageEngine Log360 / Anomaly Watch)** | **~$12.4B–$15B Estimated Valuation** (~$1.5B Revenue) | **$1,095/yr** (Log360 Cloud Professional, 10 log sources); **$1,395/yr** (Log360 Cloud Enterprise with UEBA); On-prem from **$495/yr** | **30-day free trial** (Log360 Enterprise with full UEBA, SOAR, and threat analytics, no credit card required); permanent free edition capped at 5 log sources without UEBA/correlation | Integrated SIEM and user behavior monitoring across Cloud and on-prem assets. Cost-effective for mid-market and Zoho/ManageEngine environments; trade-off is less advanced network traffic behavioral modeling than pure-play NDRs. |
| **Dynatrace Davis AI** | **~$12.4B Market Cap** (~$1.4B+ Revenue) | **$0.01/host-hr (~$7/host/mo)** (Foundation); **$0.04/host-hr (~$29/host/mo)** (Infrastructure); **$58/mo per 8 GiB host** (Full-Stack APM & Davis AI) | **15-day free trial** (Full platform access including Davis AI and Grail, no credit card required); no permanent free tier (public playground with preloaded data available) | Causal AI for root cause analysis and anomaly detection. Best for deterministic root cause analysis rather than simple correlated alerts; trade-off is consumption-based module billing makes costs difficult to forecast. |
| **Elastic Security** | **~$9.3B Market Cap** (~$1.3B+ Revenue) | **~$131/mo** (Elastic Cloud Platinum with unsupervised ML Anomaly Detection); Standard starts at **$99/mo** (no ML) | **14-day free trial** (Elastic Cloud with up to 1 deployment capped at 8 GB total RAM and 3 Serverless projects, no credit card required); Basic self-managed edition is perpetual free but lacks ML anomaly detection | Open-core SIEM with out-of-the-box detection rules. Best for teams already running Elasticsearch; trade-off is behavioral and ML anomaly detection requires Platinum tier. |
| **New Relic Alerts** (Francisco Partners & TPG) | **$6.5B Acquisition Valuation** (~$926M Revenue) | **$349/user/yr** (Pro full platform user) + **$0.40/GB** (Original data ingest) or **$0.60/GB** (Data Plus) | **Perpetual Free Tier**: **100 GB/month ingest**, 1 full platform user, unlimited basic users; paid tier free trial is **30 days** | Full-stack observability platform with automated anomaly alerts and baselining. Best for unified APM and infrastructure telemetry without per-host charges; trade-off is anomaly detection is part of general observability rather than a dedicated security SIEM. |
| **Darktrace** (Thoma Bravo) | **$5.3B Acquisition Valuation** (~$680M Revenue) | **~$20,000/yr** (Starting enterprise baseline, scales by monitored IP addresses & modules) | **30-day Proof of Value (POV) free trial** (Vendor-assisted deployment across production network/cloud/email environment, no financial commitment) | Self-learning AI-driven network detection and response (NDR) with unsupervised anomaly detection. Best for autonomous behavior baselining across zero-trust networks; trade-off is high cost and complex configuration tuning. |
| **Exabeam New-Scale Fusion** | **~$2.4B–$2.5B Valuation** (~$200M+ Revenue) | **~$31,000/yr** (Security Log Management baseline at ~50 GB/day); **~$36,000–$75,000/yr** (Full Fusion SIEM with UEBA) | **30 to 60-day Proof of Value (POV) guided trial** (Coordinated through sales engineering to ingest telemetry and train UEBA baselines; no instant self-service trial) | Cloud-native SIEM centered around User and Entity Behavior Analytics (UEBA) and automated timeline reconstruction. Best for SOC teams prioritizing behavioral deviation over static rules; trade-off is complex onboarding and tuning. |
| **Sumo Logic Cloud SIEM** (Francisco Partners) | **$1.7B Acquisition Valuation** (~$300M Revenue) | **$0.25/credit** (Credits model) or **$1.50/credit** (Flex model); Cloud SIEM ingest metered at **40 credits/GB** | **30-day free trial** (Ingest up to 1 GB/day, 20 users, 30 days retention) or 14-day agentic sandbox; permanent free tier capped at **1.25 credits/day (~500 MB/day)**, 3 users, 7-day retention | Cloud-native SIEM with behavioral analytics and automated insight generation. Best for cloud-first environments; trade-off is Cloud SIEM ingest is the highest-priced data category on the platform (40 credits/GB). |
| **Rapid7 InsightIDR** | **~$1.05B Market Cap** (~$820M Revenue) | **$2,156/mo (~$25,870/yr)** billed annually (500 asset baseline minimum pack, ~**$5.89/asset/mo**) | **30-day free trial** (Full InsightIDR access for testing endpoint agents, log search, and UEBA analytics upon sales validation) | Cloud SIEM with integrated endpoint detection and behavioral analytics. Best for mid-market to enterprise SOCs seeking managed detection rules; trade-off is steep minimum asset tiers and overage rates. |



## Open-Source GitHub Projects



- **Wazuh**

  **Open Source Security Platform: Unified XDR and SIEM** (GPLv2) — **the most complete free open-source SIEM with behavioral detection**, with no feature paywall . **Features**: **Host intrusion detection** (FIM, rootkit detection, log analysis); **vulnerability detection**; **security configuration assessment** (CIS, PCI DSS, HIPAA, NIST); **active response**; **MITRE ATT&CK mapping**; **container security** for Docker and Kubernetes. **Pricing**: **Entire platform free, self-hosted**—agent, server, indexer, dashboard, active response, FIM, vulnerability detection . **Wazuh Cloud** starts at **$571/month flat** (100 agents, 1-month indexed retention, 3-month archive); Medium **$923/month** (250 agents); Large **$1,467/month** (500 agents) . **Tech stack**: C, Python, OpenSearch. **Deploy**: Self-hosted (Docker, packages) or Wazuh Cloud. **Trade-off**: **Rule-based detection, not ML anomaly detection**—requires tuning and maintenance; Indexer consumes substantial resources. **Best for**: organizations wanting a free, comprehensive SIEM with behavioral rules and compliance mapping—willing to operate and tune the stack. **Detection method**: prebuilt, signature-style rules .



- **Elastic Security (Open Source)**

  **SIEM with prebuilt detection rules** (Elastic License 2.0/SSPL) — **the open-core SIEM with a usable free tier**, though anomaly detection is gated. **Features**: **Basic self-managed free**—core log ingestion, Kibana dashboards, prebuilt detection rules; **no ML, no LDAP/SAML SSO, no cross-cluster replication** . **Platinum** (~$131/month starting) adds **ML anomaly detection** (unsupervised jobs scoring behavioral anomalies against statistical baselines) and cross-cluster replication . **Tech stack**: Java, Elasticsearch. **Deploy**: Self-hosted (Basic) or Elastic Cloud. **Trade-off**: **Anomaly detection requires Platinum**; free tier lacks ML and endpoint response; source-available, not OSI open source. **Best for**: teams already on Elastic Stack wanting SIEM detection rules with a paid path to ML anomaly detection—accepting license restrictions .



- **Security Shallots**

  **Lightweight, self-hosted SIEM that runs on anything** (PyPI) — **the easiest open-source anomaly detection starting point**, from a Raspberry Pi to a full server with just Python and SQLite . **Features**: **Ingests** Suricata, Syslog, pfSense, Wazuh, CrowdSec, Pi-hole, Argus agents, and web logs; **normalizes, deduplicates, and auto-classifies** severity; **correlates patterns** (port scans, brute force, lateral movement); **groups into incidents** with response runbooks; **AI triage** via OpenAI/Anthropic API (optional, no GPU); **hardware auto-detection**—adjusts profile based on available RAM/CPU . **Profiles**: Lite (<2 GB RAM, Suricata+syslog only); Micro (2–4 GB, +CrowdSec); Standard (4–8 GB, +Wazuh, VictoriaLogs, Grafana, tuned-down threat engine); Full (8+ GB, everything including baselines, graph, ML, kill chain) . **Tech stack**: Python, SQLite. **Deploy**: `pip install .`; `shallot run`; systemd service . **Trade-off**: **Small-scale focus**—not enterprise SIEM; threat engine disabled on low-RAM profiles; SQLite storage limits retention at high volume. **Best for**: homelabs, small businesses, and branch offices wanting functional anomaly detection without Elastic or Splunk infrastructure—especially those wanting to start on a Raspberry Pi .



### Additional Strong Open-Source Options



- **Apache Doris** — Real-time analytical database (Apache 2.0). Not an anomaly detector but often paired with monitoring pipelines for behavioral baselines. **Note**: Database, not SIEM. **Best for**: storing and querying behavioral telemetry at scale.

- **VictoriaLogs** — Log management (Apache 2.0). Included in Shallots' Standard/Full profiles for log storage and search . **Note**: Log store, not an anomaly detector. **Best for**: teams wanting lightweight log storage alongside detection.



**Frameworks for building custom systems**: Combine **Wazuh** for rule-based SIEM detection with **Elastic Security Platinum** for ML anomaly detection and **Security Shallots** for lightweight correlation—creating a layered open-source anomaly detection stack. **None of these match Darktrace's unsupervised network behavioral AI or Exabeam's mature UEBA**, but for rule-based detection, log correlation, and lightweight anomaly scoring, the options are production-capable.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Activity monitoring platforms handling telemetry and user behavior data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **The "ML anomaly detection" vs. "rule-based behavioral detection" vs. "lightweight correlation" distinction is critical.** **Datadog Enterprise, Elastic Platinum, Darktrace, and Exabeam** provide **ML/unsupervised anomaly detection**—they score deviations against learned baselines . **Splunk ES Premier, Sumo Logic, Rapid7 InsightIDR, and Wazuh** provide **rule-based behavioral detection**—they match known patterns and correlations . **Security Shallots** provides **lightweight correlation**—pattern matching and incident grouping on minimal hardware . **Choose based on whether you need learned baselines, known-pattern matching, or lightweight correlation.**

- **Elastic Security's anomaly detection is paywalled.** The free Basic tier has prebuilt detection rules but **no ML**; Platinum (~$131/month) unlocks unsupervised anomaly jobs . **Do not evaluate Elastic Basic for anomaly detection.**

- **Darktrace's cost is consistently cited as a barrier.** Reviewers note "pricing can be difficult to justify for a mid-sized organization" and "licensing tied to IP addresses can scale quickly" . **Model IP count before evaluating.**

- **Sumo Logic's Cloud SIEM ingest is 40 credits/GB**—the most expensive data type on the platform, higher than tracing or standard logs . **A poorly scoped SIEM feed can consume the budget faster than any other data source.**

- **Wazuh is the most complete free open-source SIEM**—no feature paywall, active response, FIM, and vulnerability detection included . **The trade-off**: rule-based, not ML; requires tuning and infrastructure.

- **Security Shallots is the pragmatic starting point for homelabs and small offices**—runs on a Raspberry Pi, auto-detects hardware, and provides correlation and incident grouping . **The trade-off**: not enterprise-scale; ML threat engine requires 8+ GB RAM.

- Self-hosted open-source solutions require proper infrastructure (Wazuh Indexer is resource-heavy; Shallots needs Python/SQLite), security hardening, and ongoing maintenance. **Activity monitoring tools process sensitive telemetry**—ensure your deployment meets your organization's privacy and security requirements before collecting production data.



---



**Made for SOC teams, security engineers, and organizations building transparent anomaly detection solutions.**

Let's make Activity Monitoring & Anomaly Detection more open, data-driven, and behavior-aware.
