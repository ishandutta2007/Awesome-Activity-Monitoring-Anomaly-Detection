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
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Datadog Security Monitoring**
  **Cloud security monitoring** with anomaly detection and correlation. **Pricing**: **Pro $15/host/month**; **Enterprise $23/host/month** adds Machine Learning, Anomaly Detection, and Forecast Insights; **DevSecOps Enterprise $34/host/month** adds Data Security and cloud workload monitoring . **Free tier**: Trial available; no perpetual free tier. **Best for**: teams already on Datadog wanting security anomalies alongside observability—**trade-off**: ML anomaly detection requires Enterprise tier; per-host costs scale with infrastructure .

- **Splunk Enterprise Security**
  **Enterprise SIEM** with deep detection content and UEBA in Premier tier. **Pricing**: **Ingest-based (GB/day)**: at 100–199 GB/day, **ES Essentials $759/GB/day/year**, **ES Premier $1,783.65/GB/day/year** (plus platform license) . **UEBA is included only in Premier** . **Free tier**: None. **Best for**: large enterprises with heavy custom detection needs—**trade-off**: costs scale steeply with data volume; UEBA gated to Premier .

- **Sumo Logic Cloud SIEM**
  **Cloud-native SIEM** with behavioral analytics. **Pricing**: **Cloud SIEM ingest costs 40 credits/GB**—the most expensive data type on the platform, higher than tracing (35) or standard logs (25) . Credits priced at **$0.25 (Credits model)** or **$1.50 suggested resale (Flex)** . **Free tier**: Trial available. **Best for**: cloud-first teams wanting managed SIEM with usage-based pricing—**trade-off**: SIEM ingest is separately metered and expensive; log volume is the primary cost driver .

- **Dynatrace Davis AI**
  **Causal AI for root cause analysis** and anomaly detection. **Pricing**: **Per-module consumption**—infrastructure, APM, logs, and security are priced separately; **no permanent free tier** . **Free tier**: Trial only. **Best for**: teams wanting deterministic root cause analysis rather than correlated alerts—**trade-off**: per-module pricing makes costs hard to forecast; learning curve is steep .

- **New Relic Alerts**
  **Observability platform** with anomaly detection and alerting. **Pricing**: **Free tier includes 100 GB/month ingest, one full platform user, unlimited basic users**; paid data **$0.40/GB (Original)** or **$0.60/GB (Data Plus)**; **Pro full platform users $349/user/year (annual)** . **Free tier**: Yes, perpetual 100 GB/month. **Best for**: teams wanting observability with anomaly detection without per-host charges—**trade-off**: anomaly detection is part of the broader platform, not a dedicated security tool .

- **Elastic Security**
  **SIEM with ML anomaly detection on Platinum+**. **Pricing**: **Basic self-managed free** (prebuilt detection rules, Kibana dashboards, **no ML**); **Platinum (~$131/month)** adds **ML anomaly detection** and cross-cluster replication . **Free tier**: Yes, Basic self-managed. **Best for**: teams wanting an open-core SIEM with a free entry point—**trade-off**: anomaly detection requires Platinum; free tier lacks ML and response actions .

- **Rapid7 InsightIDR**
  **SIEM with UEBA and anomaly detection**. **Pricing**: **Quote-only**; **log ingestion volume is the critical cost driver**—negotiate higher baseline limits and lower overage rates upfront; **annual escalation typically 3–7%** . **Free tier**: None. **Best for**: mid-market to enterprise teams wanting managed SIEM with behavioral detection—**trade-off**: overage rates can be significant; professional services add 10–20% .

- **Darktrace**
  **AI-driven network detection and response** with unsupervised anomaly detection. **Pricing**: **Quote-only**; reviewers consistently cite **cost as a barrier**—"pricing can be difficult to justify for a mid-sized organization"; **licensing tied to IP addresses scales quickly** . **Free tier**: None. **Best for**: organizations wanting autonomous, behavior-based network anomaly detection—**trade-off**: expensive; UI is "tricky and not very user friendly"; overwhelming during learning phase .

- **Exabeam New-Scale Fusion**
  **UEBA-driven SIEM** with behavioral analytics and automated investigations. **Pricing**: **Quote-only**; Gartner reviewers note **strong UEBA and reduced false positives**, but **deployment complexity and data onboarding take time**; confusion between old and new rule sets . **Free tier**: None. **Best for**: SOC teams prioritizing user behavior analytics and automated timelines—**trade-off**: setup and tuning require effort; version confusion in rule sets .

- **Zoho Watch**
  **Note**: No public information found for a Zoho security monitoring/anomaly detection product named "Watch" in available search results. Zoho offers security features within its admin console but not a standalone anomaly detection platform. **Best for**: verify directly with Zoho before evaluating.

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
