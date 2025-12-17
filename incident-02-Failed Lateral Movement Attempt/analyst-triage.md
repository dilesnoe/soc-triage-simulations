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
The activity was detected following failed NTLM network authentication attempts from WS-18 to WS-25, followed by an attempted access to the administrative share (`\\WS-25\ADMIN$`).

## Analysis
- A successful interactive logon for `temp.admin` occurred on WS-18 (Event ID 4624, Logon Type 2).
- Subsequent NTLM network logon attempts to WS-25 failed (Event ID 4625).
- An attempted access to the administrative share `\\WS-25\ADMIN$` was observed (Event ID 5145).
- The process `net.exe` executed on WS-25 under the same account (Event ID 4688).
- A second NTLM network logon attempt using the `administrator` account failed on WS-18 (Event ID 4625).
- No evidence of successful authentication, persistence, or host-to-host spread was identified.

## Conclusion
This activity represents an attempted but unsuccessful lateral movement scenario.  
There is no evidence consistent with a successful compromise.

## Recommended Action
- Continue monitoring authentication attempts involving `temp.admin` and `administrator`
- Monitor for repeated administrative share access attempts

