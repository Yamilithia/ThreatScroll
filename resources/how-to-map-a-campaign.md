# How to Analyze a Campaign Using MITRE ATT&CK

Understanding how to analyze a threat campaign using the MITRE ATT&CK framework can help defenders map real-world attacks to known techniques, improve detection logic, and communicate better across teams.

This guide is written for anyone getting started in Threat Intelligence or threat hunting.

---

## Step 1: Read the Campaign Carefully

Start by identifying:
- What happened? (Phishing, ransomware, info-stealer…)
- How did the threat actor get in? (Initial access)
- What did they do once inside? (Execution, persistence, exfiltration)

---

## Step 2: Extract Tactics and Techniques

For each part of the campaign, ask:

| Phase           | Example Action                          | MITRE Technique |
|-----------------|------------------------------------------|------------------|
| Initial Access  | Sent malicious email with link           | T1566.002        |
| Execution       | Victim clicked link, JS executed         | T1059.007        |
| Credential Access | Dumped credentials with LSASS          | T1003.001        |

 Use [MITRE ATT&CK Navigator](https://attack.mitre.org/resources/navigator/) to visually map the techniques.

---

## Step 3: Organize Your Findings

Create a folder in your repo (or notebook) with:

- `summary.md`: Short description of what happened
- `mitre_mapping.md`: List of TTPs used
- `iocs.csv`: Any indicators mentioned (URLs, hashes, IPs)
- `recommendations.md`: What can defenders do?

---

## Final Thoughts

Mapping campaigns is not about having all the answers — it’s about learning to see how adversaries behave in patterns. The more you practice, the faster you’ll recognize those patterns.

If this guide helped you, feel free to copy it and adapt it for your own learning or team.

---

*Written by [@Yamilithia](https://github.com/Yamilithia) as part of the [ThreatScroll](https://github.com/Yamilithia/ThreatScroll) project.*

