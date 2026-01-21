# Incident 02 – Failed Lateral Movement Attempt

## Summary
Investigation identified attempted lateral movement between two workstations using administrative credentials. All network authentication and administrative share access attempts failed, and no evidence of host compromise or credential access was observed.

---

## Severity Assessment
**Medium**

**Rationale:** Activity reflects attempted lateral movement using administrative credentials; however, authentication was unsuccessful, controls functioned as intended, and no persistence or spread occurred.

---

## Scope & Impact
- **Affected hosts:** WS-18, WS-25
- **Accounts involved:** temp.admin, administrator
- **Impact:** No confirmed compromise; attempted access only

---

## Detection Context
Activity was identified during review of authentication failures, administrative share access attempts, and process execution telemetry. Observed behavior warranted investigation due to lateral movement patterns but did not progress beyond initial access attempts.

---

## Analyst Findings

### Initial Authentication
- Successful interactive logon for `temp.admin` on WS-18 (Logon Type 2)

**Assessment:** Interactive logon alone is not inherently malicious but provided context for subsequent activity.

---

### Failed Lateral Movement Attempts
- Repeated NTLM network logon failures from WS-18 to WS-25
- Attempted access to administrative share `\\WS-25\ADMIN$` denied
- Execution of `net.exe` consistent with share or credential validation attempts

**Assessment:** Activity aligns with lateral movement probing; however, authentication controls prevented access.

---

### Additional Credential Testing
- Failed network authentication attempt using `administrator` account
- No successful sessions established

**Assessment:** Indicates possible credential guessing or reuse attempt without success.

---

## Evidence Highlights
- Failed NTLM authentication events (4625)
- Administrative share access denial (5145)
- Process execution consistent with credential testing (`net.exe`)

---

## Conclusion
This activity represents an attempted but unsuccessful lateral movement scenario. Authentication controls prevented access, no persistence mechanisms were established, and no lateral spread occurred. Escalation beyond monitoring is not warranted at this time.

---

## Recommended Actions
- Continue monitoring authentication attempts involving `temp.admin` and `administrator`
- Review account usage patterns for recurrence
- Escalate only if repeated attempts or successful authentication is observed


