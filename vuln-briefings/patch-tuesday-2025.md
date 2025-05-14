# Patch Tuesday - Mayo 2025 (Microsoft)

## Vista General

El martes 14 de mayo de 2025, Microsoft publicó actualizaciones de seguridad que corrigen un total de 83 vulnerabilidades, incluyendo 5 zero-days explotadas activamente y 2 zero-days divulgadas públicamente, con varias fallas críticas que afectan componentes como Azure DevOps, Power Apps, Visual Studio y el sistema operativo Windows.

---

## Resumen de vulnerabilidades

| Tipo de vulnerabilidad               | Cantidad |
|-------------------------------------|----------|
| Elevación de privilegios            | 20       |
| Ejecución remota de código          | 28       |
| Divulgación de información          | 16       |
| Denegación de servicio              | 7        |
| Suplantación de identidad           | 3        |
| Omisión de funciones de seguridad   | 2        |

- Zero-days explotadas activamente: 5
- Zero-days divulgadas públicamente: 2
- Vulnerabilidades críticas: 11

---

## Zero-days explotadas activamente

| CVE             | Componente                 | Impacto                   |
|-----------------|----------------------------|----------------------------|
| CVE-2025-30400  | dwmcore.dll (DWM Core)     | Elevación de privilegios   |
| CVE-2025-32701  | clfs.sys (CLFS)            | Elevación de privilegios   |
| CVE-2025-32706  | clfs.sys (CLFS)            | Elevación de privilegios   |
| CVE-2025-32709  | afd.sys (WinSock)          | Elevación de privilegios   |
| CVE-2025-30397  | Motor de scripting de MS   | Ejecución remota de código |

---

## Zero-days divulgadas públicamente

| CVE             | Componente                 | Impacto                   |
|-----------------|----------------------------|----------------------------|
| CVE-2025-26685  | Defender for Identity      | Suplantación de identidad |
| CVE-2025-32702  | Visual Studio              | Ejecución remota de código |

---

## Vulnerabilidades críticas en la nube

| CVE             | Servicio afectado          | Tipo de vulnerabilidad          | CVSS |
|-----------------|----------------------------|----------------------------------|------|
| CVE-2025-29813  | Azure DevOps               | Elevación de privilegios por token | 10.0 |
| CVE-2025-29827  | Azure Automation           | Escalada de privilegios         | 9.x  |
| CVE-2025-29972  | Azure Storage RP           | Server-Side Request Forgery     | 9.x  |
| CVE-2025-47733  | Microsoft Power Apps       | Server-Side Request Forgery     | 9.x  |

---
## Related Hunting Queries

For in-depth detection logic and hunting rules associated with each actively exploited zero-day, refer to the following detection files under the `/hunting-queries/patch-tuesday/` folder:
- **CVE-2025-30400 – dwmcore.dll (LPE):** [`2025-05-CVE-2025-30400.md`](../hunting-queries/patch-tuesday-may-2025.md/2025-05-CVE-2025-30400.md)
- **CVE-2025-32701 & 32706 – clfs.sys (LPE):** [`2025-05-CVE-2025-32701-32706.md`](../hunting-queries/patch-tuesday-may-2025.md/2025-05-CVE-2025-32701-32706.md)
- **CVE-2025-32709 – afd.sys (LPE):** [`2025-05-CVE-2025-32709.md`](../hunting-queries/patch-tuesday-may-2025.md/2025-05-CVE-2025-32709.md)
- **CVE-2025-30397 – jscript9.dll (RCE):** [`2025-05-CVE-2025-30397.md`](../hunting-queries/patch-tuesday-may-2025.md/2025-05-CVE-2025-30397.md)

---

## Referencias

- Microsoft security - https://msrc.microsoft.com/update-guide/en-us/releaseNote/2025-May
- Microsoft Patch Tuesday – Mayo 2025 (BleepingComputer): https://www.bleepingcomputer.com/news/microsoft/microsoft-may-2025-patch-tuesday-fixes-5-exploited-zero-days-72-flaws/
- Tenable Analysis: https://www.tenable.com/blog/microsofts-may-2025-patch-tuesday-addresses-71-cves-cve-2025-32701-cve-2025-32706l
