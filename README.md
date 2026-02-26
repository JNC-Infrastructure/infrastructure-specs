# JNC Egress Path Integrity & Routing Policy
**Version:** 1.0.4  
**Project:** JNC-FL-2026 (Sovereign Infrastructure Rollout)

## 1. Carrier Pinning Requirements
To ensure path stability for high-frequency data ingestion, JNC mandates dedicated egress pinning to the following Autonomous Systems:
* **Primary:** AS7018 (AT&T Services)
* **Secondary:** AS701 (Verizon Business / MCI)

## 2. Technical Specifications
* **MTU Configuration:** Strict 1500-byte path integrity. No fragmentation permitted at the edge.
* **Protocol:** Unencapsulated Layer 2/3 handoff.
* **VLAN Tagging:** 802.1Q tagging required for multi-tenant isolation within the JNC cluster.
* **Latency Thresholds:** < 5ms to the Miami/Tampa peering points (Equinix MI1 / Hivelocity TPA1).

## 3. Resilience & Compliance (DORA)
This architecture is designed to meet the **Digital Operational Resilience Act (DORA)** standards for financial entities:
* **ICT Risk Management:** Redundant carrier paths (Multi-homed BGP) to prevent single-point-of-failure in egress.
* **Incident Reporting:** Real-time telemetry monitoring via hardware-level probes.
* **Digital Testing:** Monthly stress-testing of unencapsulated paths to ensure throughput consistency.

[Download Institutional Framework ([PDF](https://github.com/JNC-Infrastructure/infrastructure-specs/blob/fda9afc22266a362ec001e94d33ff0862cfd4a7a/JNC_Global_Sovereign_Infrastructure_2026.pdf)
