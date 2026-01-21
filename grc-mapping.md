# GRC Mapping – Incident-Based Control Assessment

This document demonstrates how operational incident evidence informs governance, risk, and compliance decisions.

---

## Incident 01 – Domain Compromise

**Control Domains Impacted:**
- NIST CSF PR.AC
- NIST SP 800-53 AC-2, AC-6
- ISO 27001 A.5.18

**Observed Control Gaps:**
- Credential reuse not detected pre-exploitation
- Excessive privilege allowed lateral spread

**Risk Statement:**
Compromise of administrative credentials enabled unauthorized domain-level access, increasing the risk of data compromise and service disruption.

**Residual Risk:**
Moderate, mitigated through credential reset, privilege review, and enhanced monitoring.

---

## Incident 02 – Blocked Lateral Movement

**Control Domains Validated:**
- NIST CSF PR.AC
- NIST SP 800-53 AC-7, IA-2

**Observed Control Effectiveness:**
- Authentication failures enforced
- Administrative share access denied

**Risk Statement:**
Attempted lateral movement was prevented by access controls, reducing likelihood of impact.

**Residual Risk:**
Low, with continued monitoring recommended.
