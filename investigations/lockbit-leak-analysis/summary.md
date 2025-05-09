# 🔓 LockBit Leak – Technical Analysis (May 2025)

## Context

On May 7, 2025, the LockBit ransomware group suffered a major breach. Their dark web admin panel was defaced with an anonymous message and a link was shared to download their internal MySQL database (`paneldb`). This dump provided rare visibility into the operational structure of one of the most active Ransomware-as-a-Service (RaaS) operations.

The dataset includes detailed records of victim management, affiliate IDs, negotiation metadata, and access timelines, giving analysts an unprecedented view into how LockBit organized, tracked, and monetized extortion campaigns.

---

## Key Findings

- Over **2,200 victims** listed in the `clients` table.
- Each record includes:
  - `advid`: ID of the affiliate managing the victim.
  - `views`: number of times the victim’s page was accessed.
  - `date_first` / `date_last`: first and last access timestamps.
- Evidence of structured automation to track progress, publish leaks, and assign cases by affiliate.

---

## CTI Relevance

This leak is highly valuable for defenders and researchers. It allows for:

- Mapping LockBit TTPs to MITRE ATT&CK:
  - `T1486` – Data Encrypted for Impact  
  - `T1490` – Inhibit System Recovery  
  - `T1071.001` – Web Protocols (C2)
- Understanding affiliate behavior patterns.
- Improving threat models by studying real durations of extortion cycles.
- Supporting timeline reconstruction and incident response simulations.

---

This analysis was conducted by [@Yamilithia](https://github.com/Yamilithia) as part of [ThreatScroll](https://github.com/Yamilithia/ThreatScroll).
