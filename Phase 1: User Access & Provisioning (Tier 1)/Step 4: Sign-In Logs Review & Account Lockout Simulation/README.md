🔐 **Step 4: Sign-In Logs Review & Account Lockout Simulation** — `labadmin` Diagnostic Troubleshooting

---

🌟 **Objective**
This simulation replicates a realistic Tier 1–2 escalation scenario involving an account lockout. Using Microsoft Entra ID, we simulate failed login attempts to trigger a lockout and then analyze sign-in logs to identify the root cause. This strengthens core diagnostic and access troubleshooting skills.

---

🛠️ **Tools & Technologies Utilized**

* **Microsoft Entra Admin Center** — Interface for identity and access management
* **Sign-In Logs Panel** — Detailed tracking of authentication attempts
* **IP & Device Metadata** — Contextual information to investigate patterns or risk
* **Error Codes & Diagnostic Layer** — Reveal sign-in failures and security flags

---

✅ **Actions Performed & Key Outcomes**

| **Task**                     | **Outcome / Detail**                                                                                                      | **Rationale / Best Practice Applied**                                                   |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Manual Lockout Triggered     | Repeated incorrect login attempts for `labadmin@micocoopergmail.onmicrosoft.com` resulted in a temporary account lockout. | Simulated a realistic Tier 1 scenario involving credential failure and lockout.         |
| Lockout Screen Verified      | Microsoft login screen confirmed lockout: *"Your account is temporarily locked to prevent unauthorized use."*             | Reproduced user error for visibility and downstream troubleshooting.                    |
| Sign-In Log Accessed         | Navigated to **Users → labadmin → Sign-in logs** in Entra Admin Center.                                                   | Accessed logs to determine failure timeline and correlate potential risk.               |
| Diagnostic Insights Reviewed | Entra results showed repeated failures and error code **50126** (invalid credentials).                                    | Identified error patterns and user behavior through automated insights.                 |
| Metadata Correlated          | Reviewed IP address, OS, client app, and session ID across failed attempts.                                               | Confirmed logins originated from the correct region and device, eliminating compromise. |

---

📸 **Account Lockout & Diagnostic Review Screenshots**

**🔒 Lockout Screen**  
User is temporarily locked out after repeated failed sign-in attempts.  
![Account Lockout](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%204:%20Sign-In%20Logs%20Review%20&%20Account%20Lockout%20Simulation/m365-account-lockout-screen.png?raw=true)

**🧾 Basic Log Info**  
Captured OS, browser, and app context from the failed sign-in.  
![Sign-In Basic Info](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%204:%20Sign-In%20Logs%20Review%20&%20Account%20Lockout%20Simulation/entra-signin-log-basic-info.png?raw=true)

**🛠️ Diagnostic Panel**  
Microsoft Entra surfaced the lockout cause and flagged old credential submission.  
![Sign-In Diagnostic](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%204:%20Sign-In%20Logs%20Review%20&%20Account%20Lockout%20Simulation/entra-signin-diagnostic-results.png?raw=true)

**🔍 Activity Metadata**  
Detailed session, app, and tenant-level metadata for the failed login.  
![Activity Metadata](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%204:%20Sign-In%20Logs%20Review%20&%20Account%20Lockout%20Simulation/entra-signin-log-activity-details.png?raw=true)

**❌ Failure Reason – Error 50126**  
Sign-in failed due to incorrect credentials; commonly seen with typos or stale passwords.  
![Error 50126](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%204:%20Sign-In%20Logs%20Review%20&%20Account%20Lockout%20Simulation/entra-signin-error-50126.png?raw=true)


---

💠 **Key Learnings & Strategic Insights**

* **Tier 1 Relevance**: Account lockouts are one of the most frequent real-world escalations.
* **Context Matters**: IPs, browsers, and OS logs provide crucial context to assess user intent vs. threat.
* **Pattern Recognition**: Error codes like `50126` become repeat indicators—speeding up triage.

---

🧠 **Final Thoughts**

There are so many logs auditing tools in Entra. Finding the one that gets you the information that you need is sometimes a challenge for me. This lab gives me more exposure to finding the logs i need and how to interpret the data to make decisions that improve security and administrative posture
