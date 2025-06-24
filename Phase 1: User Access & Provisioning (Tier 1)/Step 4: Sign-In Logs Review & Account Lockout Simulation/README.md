🔐 Step 4: Sign-In Logs Review & Account Lockout Simulation — labadmin Diagnostic Troubleshooting

🌟 Objective

This simulation replicates a Tier 1–2 escalation scenario involving an account lockout. Using Microsoft Entra ID, we simulate failed login attempts to trigger a lockout and then analyze sign-in logs to identify the root cause. This reinforces diagnostic skills required to respond to user access issues and potential credential compromise.

🛠️ Tools & Technologies Utilized

* Microsoft Entra Admin Center – Used to access user sign-in logs
* Sign-In Logs Panel – Provides detailed visibility into authentication attempts
* IP Address and Device Metadata – Helps correlate repeated failures or suspicious behavior
* Error Code & Diagnostic Layer – Interprets system feedback for actionable resolution

✅ Actions Performed & Key Outcomes

| Task                         | Outcome / Detail                                                                                                        | Rationale / Best Practice Applied                                                      |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Manual Lockout Triggered     | Repeated incorrect login attempts for `labadmin@micocoopergmail.onmicrosoft.com` resulted in temporary account lockout. | Simulated a realistic Tier 1 ticket scenario involving credential failure and lockout. |
| Lockout Screen Verified      | Microsoft login screen confirmed lockout: *"Your account is temporarily locked to prevent unauthorized use."*           | Validated account status and reproduced error message for user-side awareness.         |
| Sign-In Log Accessed         | Navigated to **Users → labadmin → Sign-in logs** in Entra Admin Center.                                                 | Proactively accessed diagnostic logs to identify cause and history of failure.         |
| Diagnostic Insights Reviewed | Entra diagnostic results indicated repeated credential failures and sign-in error code **50126**.                       | Demonstrated interpretation of system feedback to isolate error origin.                |
| Metadata Correlated          | Logged IP address, OS, browser client, and session data to confirm legitimate activity.                                 | Confirmed whether issue was localized or indicated potential compromise.               |

📸 Account Lockout & Diagnostic Review Screenshots

**Lockout Screen**
User is temporarily locked out due to multiple failed sign-in attempts.\\

**Basic Log Info**
Captured details from the failed login attempt including device, OS, and client type.\\

**Diagnostic Panel**
Microsoft Entra diagnostic tool flags repeated failures and potential stale password use.\\

**Activity Metadata**
Extended metadata including app ID, session ID, tenant IDs, and resource logs.\\

**Failure Reason – Error 50126**
Error validating credentials due to invalid username or password.\\

💠 Key Learnings & Strategic Insights

* **Tier 1 Impact**: Account lockouts are among the most common daily support escalations—mastery of sign-in logs ensures rapid, evidence-based resolution.
* **Root Cause Isolation**: IP and client context help distinguish between user error, automation loops, or unauthorized attempts.
* **Response Playbooks**: Recognizing patterns like error code `50126` allows support teams to route cases more efficiently or resolve autonomously.

🧠 Final Thoughts

Sign-in diagnostics offer powerful insight into access issues. Understanding how to interpret failure codes, device metadata, and sign-in patterns is a core skill I see on plenty of job descriptions so I wanted to make sure i showcased my skills here.

👉 Proceed to Step 5: License Assignment

Simulate license provisioning by adding or removing Microsoft 365 licenses for labadmin using the Admin Center interface.
