## 📬 Step 2: Mail Flow & Shared Mailbox Escalation — labadmin Diagnostic + Delegation

---

### 🌟 Objective

In this simulation, I worked through a Tier 1.5 help desk escalation involving both **mail flow delay diagnostics** and **shared mailbox access troubleshooting**. I encountered a scenario where I couldn't send emails from the shared mailbox `Support Team`, and email delivery was delayed. I resolved the issue by creating the mailbox, assigning permissions, and diagnosing the mail flow using trace tools and header-level analysis.

---

### 🛠️ Tools & Technologies Utilized

* **Exchange Admin Center (EAC)** — Admin interface for mailbox creation and permissions
* **Outlook Web Access (OWA)** — Verification of mailbox access and Send As functionality
* **Microsoft 365 Defender > Message Trace** — Tool for tracking email delivery and delay
* **Microsoft Header Analyzer** — Diagnostic tool for inspecting delivery hops and throttling
* **Email Header Metadata** — Used to detect root cause when message trace lacked detail

---

### ✅ Actions Performed & Key Outcomes

| Task                      | Outcome / Detail                                                 | Rationale / Best Practice Applied                        |
| ------------------------- | ---------------------------------------------------------------- | -------------------------------------------------------- |
| Shared Mailbox Created    | `Support Team` mailbox provisioned in EAC                        | Enables collaborative team communication                 |
| Full Access Delegated     | `labadmin@micocoopergmail.onmicrosoft.com` granted Full Access   | User can open and read the mailbox                       |
| Send As Delegated         | Same user granted Send As permissions                            | Allows sending emails as the mailbox identity            |
| Mail Flow Delay Simulated | User experienced delay in email receipt                          | Mimics common Tier 1 ticket scenario                     |
| Message Trace Run         | Trace showed a 3-minute delay during intermediate processing     | Message trace helped confirm delivery route and delay    |
| Header Analyzed           | Microsoft Header Analyzer used to pinpoint throttling            | Bypasses surface-level logs and gives hop-by-hop insight |
| Send As Validated         | Successfully sent a test email from `Support Team` to `labadmin` | Confirms proper delegation + permission propagation      |

---

### 📸 Screenshots

Below are key steps and confirmations captured during the shared mailbox setup and mail flow escalation process:

#### ✅ Shared Mailbox Created in Exchange Admin Center (EAC)
![Shared Mailbox Creation - EAC](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%202:%20Shared%20Mailbox%20Setup%20&%20Mail%20Flow/shared-mailbox-creation-eac.png?raw=true)

#### 🔑 Full Access Permissions Assigned to labadmin
![Shared Mailbox Full Access Confirmation](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%202:%20Shared%20Mailbox%20Setup%20&%20Mail%20Flow/shared-mailbox-fullaccess-confirmation.png?raw=true)

#### ✉️ Send As Permissions Assigned to labadmin
![Send As Permissions Confirmation](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%202:%20Shared%20Mailbox%20Setup%20&%20Mail%20Flow/shared-mailbox-sendas-confirmation.png?raw=true)

#### 📥 Test Email Successfully Received by labadmin
![Send As Email Received](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%202:%20Shared%20Mailbox%20Setup%20&%20Mail%20Flow/sendas-received-confirmation.png?raw=true)

---

### 🔠 Key Learnings & Strategic Insights

* **Delegation vs. Permission Propagation**: Full Access applies quickly, but **Send As may take 15–30 minutes** to propagate across Microsoft 365 systems.
* **GUI Admin > PowerShell fallback**: When PowerShell fails due to platform issues, the Exchange Admin Center is a reliable alternative.
* **Header-level troubleshooting**: In real-world support, message trace alone may not be enough — **headers give the full picture**.
* **Permission testing is key**: Granting access is only half the work — **validating that it works end-to-end matters most.**

---

### 🧠 Final Thoughts

I ran into multiple realistic support challenges during this phase — from PowerShell module issues on Linux to Send As delays. But working through them gave me hands-on insight into real-life Tier 1.5 troubleshooting. Getting permissions right, testing them, and being able to explain delays to users — that’s the job. This lab made the process real.

---
