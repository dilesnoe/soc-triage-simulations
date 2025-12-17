# Incident 02 – Failed Lateral Movement Attempt

## Summary
An account attempted network authentication and administrative share access between two workstations.  
All NTLM authentication attempts failed, and no lateral movement was successful.

## Severity
Medium – Attempted Lateral Movement (Blocked)

## Scope
- Hosts: WS-18, WS-25
- Accounts: temp.admin, administrator

## Initial Detection
The activity was detected when the account `temp.admin` failed to authenticate to WS-25, followed by an attempted access to the ADMIN$ share and subsequent failed network logon attempts.

## Analysis
- A successful interactive logon for `temp.admin` occurred on WS-18 (Event ID 4624, Logon Type 2).
- A network logon attempt to WS-25 using NTLM failed (Event ID 4625).
- An attempted access to the `\\WS-25\ADMIN$` administrative share was observed (Event ID 5145).
- The process `net.exe` executed on WS-25 under the same account (Event ID 4688).
- A second network logon attempt using the `administrator` account failed on WS-18 (Event ID 4625).
- No successful authentication, persistence, or host-to-host spread was identified.

## Conclusion
This activity represents an attempted but unsuccessful lateral movement scenario.  
There is no evidence consistent with a successful compromise.

## Recommended Action
- Continue monitoring authentication attempts involving `temp.admin` and `administrator`
- Monitor for repeated access attempts to administrative shares
