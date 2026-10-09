# Awesome-Security-Event-Monitoring

# Top Security Event Monitoring Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on SIEM, Log Aggregation & Self-Hosted Security Operations Centers*  
**Last updated: October 2026**

This repository tracks notable **commercial security event monitoring platforms** and **open-source projects** that collect, correlate, and analyze security telemetry across enterprise environments — from cloud-native SIEM to self-hosted SOC stacks.

**Examples** include Salesforce Shield Event Monitoring, Splunk Cloud, Datadog Cloud SIEM, Sumo Logic Cloud SIEM, Elastic Security, Microsoft Sentinel, Rapid7 InsightIDR, LogRhythm, Securonix, and Exabeam (the category leaders).

**Open-source emphasis**: Security event monitoring is one of the strongest open-source domains. **Wazuh** leads as the most complete open-source SIEM platform with 4.4-star Gartner ratings and comprehensive threat detection capabilities . **Graylog** delivers centralized log management with an experimental MCP endpoint for LLM integration . **Security Shallots** brings a lightweight, self-hosted SIEM that runs on anything from a Raspberry Pi to a full server . **CNSL** provides correlated network security with ML anomaly detection and live dashboard capabilities . **Sentora** offers an AI-powered self-hosted SIEM, EDR, and SOAR platform with air-gap support . This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Splunk Cloud](https://www.splunk.com/)**  
  **The enterprise SIEM standard** — mature search, correlation, and the largest app ecosystem. **Pricing scales with data volume**. **Best for large SOCs with dedicated teams** .

- **[Datadog Cloud SIEM](https://www.datadoghq.com/)**  
  **Cloud-native SIEM integrated with Datadog observability** — log management, security signals, and threat detection. **Best for Datadog users wanting unified observability and security** .

- **[Sumo Logic Cloud SIEM](https://www.sumologic.com/)**  
  **Cloud-native security analytics** — automated threat detection and compliance. **Best for cloud-first organizations** .

- **[Elastic Security](https://www.elastic.co/security)**  
  **SIEM and EDR on Elastic Stack** — detection rules, timelines, and cases. **Trade-off**: Free version lacks correlation engine and built-in rules; advanced features require subscription . **Best for Elastic Stack users**.

- **[Microsoft Sentinel](https://azure.microsoft.com/en-us/products/microsoft-sentinel)**  
  **Microsoft's cloud-native SIEM and SOAR** — integrated with Azure, Microsoft 365, and third-party sources. **Security Copilot for AI-driven investigation**. **Best for Microsoft-centric organizations** .

- **[Rapid7 InsightIDR](https://www.rapid7.com/products/insightidr/)**  
  **SIEM with UEBA, endpoint detection, and honeypots** — **Best for SIEM + EDR convergence** .

- **[LogRhythm](https://logrhythm.com/)**  
  **SIEM with native log management and SOAR** — **Best for mid-market organizations** .

- **[Securonix](https://www.securonix.com/)**  
  **Cloud-native SIEM with UEBA, SOAR, and NDR** — **Best for integrated security analytics** .

- **[Exabeam](https://www.exabeam.com/)**  
  **SIEM with behavioral analytics (UEBA)** — automated incident timelines. **Rated 4.4 stars with 258 reviews on Gartner** .

- **[Salesforce Shield Event Monitoring](https://www.salesforce.com/)**  
  **Salesforce's native event monitoring** — tracks user activity, API calls, and security events within Salesforce. **Best for Salesforce customers wanting native monitoring** .

## Open-Source GitHub Projects

### Full SIEM Platforms

- **[Wazuh](https://github.com/wazuh/wazuh)**  
  **The most complete open-source SIEM platform**, GPLv2 licensed with **4.4-star Gartner ratings** and **54+ verified reviews** . **Four components**: Indexer (OpenSearch-based), Server (log analysis engine), Dashboard (web UI), and Agent (endpoint telemetry). **Native security log analysis, vulnerability detection, security configuration assessment, and regulatory compliance reports** — no significant third-party integration required . **Wazuh 4.14.0** added unified inventory dashboards for browser extensions, services, users, and groups . **Trade-offs**: Documentation gaps, limited active response scripts, and high resource use due to Elastic backend . **Best for comprehensive open-source SIEM**.

- **[Security Shallots](https://pypi.org/project/security-shallots/)**  
  **Lightweight, self-hosted SIEM that runs on anything** — from Raspberry Pi to full server, no Docker required . **Ingests from Suricata, Syslog, pfSense, Wazuh, CrowdSec, Pi-hole, and Argus agents** . **Auto-detects hardware and adjusts**: Raspberry Pi (2GB) runs Suricata + syslog; Server (16GB+) runs full threat engine with baselines and ML . **Features**: alert normalization, deduplication, severity classification, pattern correlation (port scans, brute force, lateral movement), incident grouping with runbooks, and optional AI triage . **~200-400MB RAM on 4GB machine** . **Best for lightweight home labs and small SOCs**.

- **[Sentora](https://github.com/d3vhex/Sentora)**  
  **AI-powered self-hosted SIEM, EDR, and SOAR platform**, open-source . **Threat intel integration**: AlienVault OTX, VirusTotal, and abuse.ch feeds (Feodo, ThreatFox, URLhaus) with automatic pruning . **Air-gap mode** — all feeds and OSV mirror can be internal, nothing leaves the network . **Fleet exposure reporting** with coverage transparency . **Agent config validation** with regex compilation checking before deployment . **Best for air-gapped environments needing AI-powered security operations** .

### Log Management & Analytics

- **[Graylog](https://github.com/Graylog2/graylog2-server)**  
  **Centralized log management with alerting and dashboards**, SSPL licensed (not OSI-approved) . **Graylog 7.0 introduced experimental Model Context Protocol (MCP) endpoint** — LLM clients can connect for natural language queries . **Four products**: Open (free), Enterprise, Security (SIEM tier), and API Security . **Trade-off**: SIEM-relevant features (anomaly detection, compliance reports) are in paid Security tier . **Best for organizations wanting polished log management UI**.

- **[CNSL (Correlated Network Security Layer)](https://pypi.org/project/cnsl/)**  
  **Correlated network security with ML anomaly detection**, open-source . **Features**: auth log monitoring, tcpdump network capture, GeoIP enrichment, SQLite persistence, live dashboard, 2FA, PDF compliance reports, and Grafana export . **ML anomaly detection** via scikit-learn . **Blocking backends**: iptables or ipset . **Dry-run safe by default** . **Best for network-focused security monitoring**.

- **[ELK Stack](https://github.com/cyberdesserts/elk_stack)**  
  **Elasticsearch, Logstash, and Kibana for security monitoring**, Elastic License 2.0 . **Telemetry scripts for Linux, Windows, and macOS** monitoring auth events, network activity, and suspicious behavior . **Metrics**: failed logins, active connections, network processes, temp files, system load . **Trade-off**: Not a complete SIEM — no built-in correlation engine or security rules in free version . **Best for building custom SIEM-like functionality**.

### Additional Strong Open-Source Options

- **OSSEC** — Host-based intrusion detection (HIDS) that inspired Wazuh, now largely superseded .
- **Suricata** — Network IDS/IPS with deep packet inspection, not a complete SIEM but integrates with Elastic Stack .
- **OpenSearch** — Fork of Elasticsearch/Kibana with Security Analytics including Sigma rules and anomaly detection .
- **Fluentd** — Log collector and forwarder with 500+ plugins, not a SIEM .
- **Fluent Bit** — Lightweight forwarder for Kubernetes (4MB binary vs Fluentd's Ruby process) .
- **Syslog-ng** — Log management with structured processing and automated archiving .
- **Arkime** — Large-scale packet capture and indexing for network security monitoring .

**Frameworks for building custom security event monitoring solutions**: Combine **Wazuh** for comprehensive SIEM with native compliance reporting and threat detection . Use **Security Shallots** for lightweight, hardware-adaptive monitoring in resource-constrained environments . Deploy **Sentora** for AI-powered security operations in air-gapped environments . Choose **CNSL** for network-focused monitoring with ML anomaly detection . Integrate **Graylog** for polished log management with LLM query capabilities . Note that true enterprise SIEM with curated threat intelligence, managed detection content, and vendor-supported SLAs (Splunk, Microsoft Sentinel, Exabeam) remains primarily commercial territory; open-source stacks provide strong log aggregation, correlation, and compliance foundations that require integration for complete security operations .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Security event monitoring platforms handle sensitive security telemetry and may process PII. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.
- **Open-source SIEM has hidden costs** — engineering overhead, detection coverage gaps, limited UEBA, and higher false-positive rates increase analyst triage time . A senior security engineer dedicated to SIEM maintenance costs more than many commercial licenses.
- **Resource requirements are real** — Wazuh single-node handles 5,000-10,000 EPS on 8 vCPU / 16 GB RAM. Security Shallots uses ~200-400MB on 4GB machines . Size infrastructure before committing.
- **License considerations**: Wazuh uses GPLv2, Graylog uses SSPL (not OSI-approved), Security Shallots is open-source, and CNSL is open-source . Verify licensing against your use case before committing.
- The open-source ecosystem provides strong log aggregation, correlation, and compliance foundations, but **curated threat intelligence, managed detection content, and vendor-supported SLAs** remain primarily commercial offerings.
