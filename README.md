# Awesome-Network-Management-System-NMS-IOT-Framework

# Awesome Network Management System (NMS) & IoT Framework

> A curated list of top Network Management System (NMS) and IoT Framework platforms — both SaaS/Hosted commercial solutions and open-source alternatives for monitoring network health, managing devices, and orchestrating IoT deployments.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [SolarWinds Network Performance Monitor](#solarwinds-network-performance-monitor)
  - [PRTG Network Monitor](#prtg-network-monitor)
  - [ManageEngine OpManager](#manageengine-opmanager)
  - [Datadog Network Monitoring](#datadog-network-monitoring)
  - [LogicMonitor](#logicmonitor)
- [Open-Source Software](#-open-source-software)
  - [Zabbix](#zabbix)
  - [LibreNMS](#librenms)
  - [OpenNMS](#opennms)
  - [NetXMS](#netxms)
  - [Checkmk Raw](#checkmk-raw)
  - [ThingsBoard](#thingsboard)
  - [FIWARE](#fiware)
  - [Eclipse Kapua](#eclipse-kapua)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Network Management and IoT platforms. These are not open-source but are included as reference points for feature comparison.

### SolarWinds Network Performance Monitor
**Type:** Enterprise network monitoring with fault and performance management
SolarWinds NPM is the long-standing enterprise standard for network monitoring, offering automated discovery, fault management, performance analysis, and hop-by-hop network path tracing. It is positioned for large enterprises and service providers willing to pay for a polished, vendor-supported platform.

### PRTG Network Monitor
**Type:** Sensor-based monitoring with Windows-native agent
PRTG (Paessler) uses a sensor-based licensing model where each monitored metric (port, disk, ping) counts as a sensor. It runs best on Windows hosts and is positioned for small to mid-sized IT teams wanting a straightforward, all-in-one monitoring appliance. **Trade-off:** Costs rise quickly with large device counts due to per-sensor pricing [citation:12].

### ManageEngine OpManager
**Type:** Integrated network, server, and application monitoring
OpManager provides network monitoring with fault management, performance management, and configuration management, with support for multi-vendor environments. It is positioned for mid-market to enterprise organizations wanting an integrated IT management suite.

### Datadog Network Monitoring
**Type:** Cloud-native network observability
Datadog provides network performance monitoring (NPM) alongside its broader observability platform, correlating network traffic with application traces and logs. It is positioned for cloud-native and DevOps teams wanting unified infrastructure and network visibility.

### LogicMonitor
**Type:** SaaS-based infrastructure monitoring
LogicMonitor provides automated discovery, hybrid cloud monitoring, and predictive alerting for network, server, and application infrastructure. It is positioned for enterprises wanting a managed monitoring platform without deploying and maintaining collectors on-premises.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Network Management and IoT Framework tools. The open-source ecosystem spans **mature all-in-one NMS platforms**, **auto-discovery-focused network monitors**, **enterprise-scale event processors**, and **IoT platforms**.

### Zabbix
**Stack:** C / PHP / MySQL/PostgreSQL | **License:** GPL-2.0
Zabbix is the most widely deployed open-source NMS, offering a complete platform for network, server, and application monitoring. It supports agent-based and agentless (SNMP, IPMI, JMX) monitoring, with automatic discovery, distributed monitoring via proxies, and a rich web UI. Zabbix is described as the "one tool that can replace multiple commercial products," with no device or sensor limits under GPL-2.0 [citation:2][citation:15]. It is positioned for organizations willing to invest setup time to build a scalable monitoring platform. **Trade-off:** Resource-hungry and complex to configure, with alerting that can be difficult to tune [citation:8].
**Best for:** Organizations wanting a comprehensive, scalable open-source NMS that can replace commercial tools, accepting the configuration complexity.

### LibreNMS
**Stack:** PHP / MySQL | **License:** GPL-3.0
LibreNMS is an auto-discovering network monitoring system with an extensive device library covering **10,000+ devices** [citation:15]. It uses CDP, FDP, LLDP, OSPF, and BGP for automatic topology discovery, with a mobile-responsive interface and an API for automation. It is positioned for network teams wanting fast time-to-value—going from unknown to fully mapped in under a day [citation:2][citation:6]. **Trade-off:** Linux-only and requires a web server (Apache/Nginx + PHP); not designed for server or application monitoring.
**Best for:** Network engineers wanting rapid auto-discovery of routers and switches with minimal configuration, particularly for small to medium networks.

### OpenNMS
**Stack:** Java | **License:** AGPL-3.0
OpenNMS is an enterprise-scale, event-driven network management platform designed for **large distributed environments** (10,000+ device fleets) [citation:6]. It uses a scalable event processing pipeline, supports Newts or TimescaleDB backends for long-term metric retention, and provides a RESTful API for integration with SOAR and ITSM tools. It is positioned for telecommunications providers, ISPs, and large enterprises. **Trade-off:** The UI can feel heavy for small deployments, and documentation depth varies between versions [citation:6].
**Best for:** Service providers and large enterprises needing a distributed, event-driven platform built for massive device fleets.

### NetXMS
**Stack:** C++ / Java | **License:** GPL-2.0
NetXMS is a unified monitoring platform with **best-in-class Windows monitoring** among open-source tools [citation:4]. Its native Windows agent collects PerfMon counters, event logs, and service statuses without scripting. The object-based hierarchy lets you model business services (e.g., a "customer portal" depending on web server, database, and firewall). It includes dynamic network maps, proxy agents for remote sites, and webhook actions for ticketing integration. **Trade-off:** Smaller community than Zabbix or Nagios, and the web UI is less polished than LibreNMS [citation:4].
**Best for:** IT generalists managing a mix of Windows servers, network devices, and custom applications needing a single pane of glass with deep Windows integration.

### Checkmk Raw
**Stack:** Python / C++ | **License:** GPL-2.0 (Raw Edition)
Checkmk Raw takes a rule-based approach to monitoring, with a web-based configuration GUI for defining hosts, services, and thresholds. Its ruleset engine applies threshold changes across matching hosts automatically, reducing configuration toil. It combines agent-based checks with SNMP in a single interface. **Trade-off:** The Raw edition is limited to **750 services per site**, and advanced features like distributed monitoring require the paid Enterprise tier [citation:6].
**Best for:** Small to mid-sized IT operations wanting to minimize configuration effort with rule-based management, without per-device licensing costs.

### ThingsBoard
**Stack:** Java / PostgreSQL / Cassandra | **License:** Apache-2.0
ThingsBoard is the most starred open-source IoT platform on GitHub (**14,713 stars**), supporting development, management, and scaling of IoT applications with both cloud and on-premises deployment [citation:13]. It handles **hundreds of thousands of devices per server node** and millions at cluster level, with no single point of failure. Key capabilities include device management with RPC control, time-series telemetry storage, a highly customizable rule engine for complex event processing, and data visualization dashboards. A 2026 IEEE study found ThingsBoard performed strongly in technical reliability and interoperability, though usability issues (finding device credentials) contributed to lower NPS [citation:5].
**Best for:** Organizations wanting a proven, scalable open-source IoT platform with strong device management and rule-engine capabilities, accepting some UI complexity.

### FIWARE
**Stack:** Various (context brokers, IoT agents) | **License:** Open Source (various)
FIWARE is an open-source IoT platform identified as the **top overall performer** in a comparative analysis of 10 open-source IoT platforms by De Nardis et al. [citation:9]. It provides a curated framework of components including context brokers (Orion), IoT agents for protocol translation (MQTT, LwM2M, etc.), and data processing tools. It is positioned for smart city, smart agriculture, and cross-domain IoT deployments, with a strong European open-source ecosystem.
**Best for:** Organizations building smart city or multi-domain IoT solutions wanting a proven, standards-based open-source framework with strong European backing.

### Eclipse Kapua
**Stack:** Java | **License:** EPL-1.0
Eclipse Kapua is an open-source IoT platform providing device management, data ingestion, and security capabilities. It is one of the platforms included in the IEEE comparative survey of open-source IoT alternatives alongside FIWARE and ThingSpeak [citation:3]. It is positioned for organizations wanting an Eclipse Foundation-governed IoT platform with modular architecture and device lifecycle management.
**Best for:** Teams in the Eclipse ecosystem wanting an open-source IoT platform with strong device management and modular extensibility.

---

## 📊 Comparison at a Glance

| Software | License | Stack | SNMP | IoT Focus | Self-Hosted | Best For |
|----------|---------|-------|------|-----------|-------------|----------|
| **SolarWinds NPM** | Proprietary | Cloud/On-prem | ✅ | ❌ | (On-prem) | Enterprise network monitoring |
| **PRTG** | Proprietary | Cloud/On-prem | ✅ | ❌ | (On-prem) | Sensor-based monitoring |
| **Zabbix** | GPL-2.0 | C/PHP/DB | ✅ | (Limited) | ✅ | Comprehensive NMS + servers |
| **LibreNMS** | GPL-3.0 | PHP/MySQL | ✅ | ❌ | ✅ | Fast network auto-discovery |
| **OpenNMS** | AGPL-3.0 | Java | ✅ | ❌ | ✅ | Large-scale event processing |
| **NetXMS** | GPL-2.0 | C++/Java | ✅ | (Limited) | ✅ | Windows-heavy environments |
| **Checkmk Raw** | GPL-2.0 | Python/C++ | ✅ | ❌ | ✅ | Rule-based quick setup |
| **ThingsBoard** | Apache-2.0 | Java/DB | (Check) | ✅ 14.7k stars | ✅ | Scalable IoT platform |
| **FIWARE** | Open Source | Various | (Check) | ✅ Top performer | ✅ | Smart city/multi-domain IoT |
| **Eclipse Kapua** | EPL-1.0 | Java | (Check) | ✅ | ✅ | Eclipse-governed IoT |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Network Management System (NMS) or IoT Framework that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The NMS and IoT landscape splits into two distinct categories. For **network monitoring**, **Zabbix** is the most comprehensive all-in-one platform that can replace multiple commercial tools, while **LibreNMS** and **Observium** are the fastest paths to auto-discovered network visibility [citation:2]. **OpenNMS** is the only choice for service providers with complex event flows [citation:6], and **NetXMS** is unmatched for Windows-heavy environments [citation:4]. For **IoT platforms**, **ThingsBoard** leads GitHub stars (14.7k) and technical performance, though its UI has usability gaps [citation:5][citation:13]. **FIWARE** was identified as the top overall performer in a comparative analysis of 10 open-source IoT platforms [citation:9]. No single tool dominates both network and IoT requirements—the right choice depends on whether your primary need is infrastructure monitoring or device orchestration.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
