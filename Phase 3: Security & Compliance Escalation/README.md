## 📁 Step 3: Security & Compliance Escalation — labadmin Log Investigation + File Access Remediation

---

### 🌟 Objective

This simulation represents a realistic Tier 2 escalation scenario where a user reports potential account compromise and data leakage. I conducted a full identity investigation using Microsoft Entra sign-in logs, cross-verified file activity through Microsoft Purview Audit Search, simulated an external sharing misconfiguration in OneDrive, and performed remediation to resecure the environment. This lab showcases layered investigation and end-to-end incident response.

---

### 🛠️ Tools & Technologies Utilized

* **Microsoft Entra ID** — Sign-in logs to review failed logins, error codes, IP patterns
* **Microsoft Purview (Unified Audit Log)** — Tracked file access, deletion, and sharing across workloads
* **OneDrive for Business** — Verified link-level access exposure and performed secure revocation
* **Microsoft 365 Compliance Experience** — Responded to portal redirection and enabled auditing
* **Microsoft 365 Identity Platform** — Interpreted error codes and investigated user sign-in events

---

### ✅ Actions Performed & Key Outcomes

| Task                       | Outcome / Detail                                                                 | Rationale / Best Practice Applied                              |
| -------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Entra Sign-In Log Reviewed | Error 50053 (account locked out) observed for `labadmin` on June 23, 6:09 PM UTC | Indicates brute-force or credential stuffing attack vector     |
| Audit Search Configured    | Search scoped to file access and sharing (June 24–26) for `labadmin`             | Focused on potential data exfiltration after account lockout   |
| Audit Logs Returned Empty  | No records found for scoped criteria                                             | Simulates real-world ingestion delays or missing logging gaps  |
| File Shared Publicly       | `Support-Incident-Report.docx` shared with “Anyone with the link”                | Demonstrates high-risk permission misconfiguration             |
| Access Validated via GUI   | Verified external link and edit permissions through Manage Access                | Manual confirmation of exposure when audit logs are incomplete |
| Access Revoked Immediately | Removed public link to resecure file and terminate unauthorized access           | Quick, effective containment of a simulated breach             |

---

### 📸 Screenshots

#### 📛 Failed Sign-in from Unusual Activity

*Microsoft Entra sign-in details showing error 50053 (account lockout) for labadmin.*
![Sign-in Failure Details – 50053](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/entra-signin-details-failure-50053.png?raw=true)

#### 🧾 Full Sign-in Log Summary for labadmin

*Filtered sign-in log displaying multiple failed and interrupted attempts.*
![Sign-in Log Summary](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/entra-signin-log-summary-filtered.png?raw=true)

#### 🔄 Unified Audit Log Search Configured in Purview

*Scoped audit search configured for labadmin activity across OneDrive and SharePoint.*
![Audit Log Search Configured](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/purview-auditlog-search-configured.png?raw=true)

#### 🌐 OneDrive Link Set to “Anyone”

*File sharing settings showing public access granted to “Anyone with the link.”*
![External Link Sharing Enabled](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/onedrive-file-shared-link.png?raw=true)

#### ✅ Public Sharing Confirmed via UI

*Confirmation dialog showing link copied with edit access enabled.*
![Link Copied Confirmation](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/onedrive-share-dialog-link-copied.png?raw=true)

#### 🚫 Manage Access – Revocation in Progress

*Manage Access panel showing the active public link prior to deletion.*
![Access Revocation - Before](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/onedrive-access-revoked-confirmation.png?raw=true)

#### 🧹 Confirmation of Link Deletion

*Final confirmation dialog for removing external access to the document.*
![Link Deletion Confirmation](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%203:%20Security%20&%20Compliance%20Escalation/onedrive-delete-link-confirmation.png?raw=true)

---

### 🔠 Key Learnings & Strategic Insights

* **Audit Logs Aren’t Always Enough** — Just because logs return empty doesn’t mean nothing happened. Support must rely on secondary validation methods (e.g., UI-based access confirmation).
* **Error Codes = Diagnostic Power** — Recognizing error 50053 let me instantly frame the problem as a lockout scenario, not user error.
* **Simulating Risk Strengthens Readiness** — Knowing how to reproduce a file exposure case helps prepare for real-world incident triage and escalation.
* **Remediation is Tier 2’s Job** — Detection is only half the battle. Immediate response — like revoking a public link — is what makes the difference.

---

### 🧠 Final Thoughts

Interesting lab. It sharpened my understanding of Tier 2 responsibilities and helped reinforce why layered verification and rapid remediation are non-negotiable in cloud support roles.

---
