🔐 **Step 2 – Microsoft 365 Password Reset Lab: labadmin Credential Management**

### 🌟 Objective

Simulate a high-frequency Tier 1 support scenario: securely resetting a user password using the Microsoft 365 Admin Center. This exercise demonstrates technical fluency in identity management, emphasizes secure access handoff, and reinforces best practices in user authentication workflows.

---

### 🛠️ Tools & Technologies Utilized

* Microsoft 365 Admin Center
* Built-in Password Reset Workflow
* MFA-secured Global Administrator Account

---

### ✅ Actions Performed & Key Outcomes

| Task                       | Outcome / Detail                                          | Rationale / Best Practice Applied                                          |
| -------------------------- | --------------------------------------------------------- | -------------------------------------------------------------------------- |
| User Selected              | `labadmin@micocoopergmail.onmicrosoft.com`                | Ensured correct target by verifying UPN in the Active Users list.          |
| Reset Method               | Auto-generated secure password                            | Adhered to best practices by avoiding predictable or reused credentials.   |
| First Login Enforcement    | "Change password at next sign-in" enabled                 | Ensured user sets a unique credential during initial login.                |
| Secure Credential Handling | Temporary password copied for secure delivery (simulated) | Reinforced concept of out-of-band delivery to reduce risk of interception. |

---

### 📸 Password Reset Process

**Password Reset Dialog**  
*Initiating a password reset for the user in Microsoft 365 Admin Center*  
![Password Reset Dialog](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%202%20%E2%80%93%20Microsoft%20365%20Password%20Reset%20Lab:%20labadmin%20Credential%20Management/m365-reset-password-dialog.png?raw=true)

**Password Reset Confirmation**  
*Password reset confirmation showing the newly generated temporary password and sign-in requirement*  
![Password Reset Confirmation](https://github.com/miadco/M365-Support-Escalation/blob/main/Phase%201:%20User%20Access%20&%20Provisioning%20(Tier%201)/Step%202%20%E2%80%93%20Microsoft%20365%20Password%20Reset%20Lab:%20labadmin%20Credential%20Management/m365-reset-password-confirmation.png?raw=true)

---

### 💠 Key Learnings & Strategic Insights

* **Security-Aware Helpdesk Execution**: Demonstrated the importance of credential lifecycle control and access hardening during onboarding.
* **Efficiency with Accuracy**: Reinforced the need for quick resolution in high-volume support environments without compromising user safety.
* **Real-World Relevance**: Password resets are one of the most common Tier 1 support tasks — mastering this workflow boosts day-one readiness.

---

### 🧠 Final Thoughts

I’ve completed password resets before using Microsoft Entra ID, but I found the Admin Center interface to be intuitive, efficient, and well-aligned with security best practices.

👉 Proceed to **Step 3: Configure MFA** to expand on identity hardening and authentication assurance.
