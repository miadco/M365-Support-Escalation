# 🔰 Phase 1: User Access & Provisioning (Tier 1)

## 🎯 Objective

This phase simulates core Tier 1 helpdesk responsibilities within a Microsoft 365 environment, empowering IT support professionals to manage the full user access lifecycle. These scenarios mirror real-world support tickets, focusing on fast resolution, user security, and audit-ready documentation. You’ll build hands-on confidence using **Microsoft 365 Admin Center** and **Microsoft Entra ID** to support:

* ✅ New user onboarding
* 🔐 Password resets
* 🔒 MFA setup and re-registration
* 🚫 Account lockout diagnosis and recovery

Each task is grounded in **industry best practices** for identity security and operational excellence.

---

## 🛠️ Tools & Portals Used

* **Microsoft 365 Admin Center** – Manage users, licenses, and credentials
* **Microsoft Entra ID (Azure AD)** – Identity and access management
* **Microsoft Authenticator** – MFA setup and user verification
* **Outlook / Teams Web** – Validate user sign-in and access

---

## ✅ Step-by-Step Tasks

### 👤 Step 1: Create a New User (Provisioning)

📌 *Simulate onboarding a new employee with secure account setup and service access.*

**Why this matters:** Proper provisioning ensures users have the access they need on day one, with secure defaults that align with least privilege principles.

**Actions:**

1. Go to **M365 Admin Center → Users → Active users → Add a user**
2. Fill in identity fields (e.g., `john.doe@yourtenant.onmicrosoft.com`)
3. Select **auto-generate password** for complexity and security
4. Ensure **"Require password change"** is enabled to protect against shared credentials
5. Assign a license (e.g., Microsoft 365 E5) to activate necessary services

---

### 🔐 Step 2: Reset User Password

📌 *Execute a standard credential recovery procedure for locked-out or compromised accounts.*

**Why this matters:** Password resets are high-frequency, high-risk actions. Enforcing secure password practices and verification policies is essential to prevent escalation or abuse.

**Actions:**

1. Select the affected user → Click **Reset password**
2. Choose **auto-generate** for strong password generation
3. Confirm **"Require password change on next sign-in"** is enabled
4. Copy the temporary password securely and simulate out-of-band delivery

---

### 🔒 Step 3: Configure MFA

📌 *Ensure the user has strong authentication methods configured or reset, mitigating risk from stolen passwords.*

**Why this matters:** MFA is one of the most effective defenses against unauthorized access. Support teams must understand how to audit, re-register, and guide users through the process.

**Actions:**

1. Go to **Microsoft Entra ID → Users → Select user → Authentication methods**
2. Set default sign-in method (e.g., Authenticator app)
3. Trigger **"Require re-register multifactor authentication"** to reset MFA and simulate new registration

---

### 🚫 Step 4: Simulate Account Lockout & Review Sign-In Logs

📌 *Reproduce a common scenario involving repeated failed logins and demonstrate root cause analysis using diagnostic logs.*

**Why this matters:** Fast and accurate diagnosis of account lockouts is crucial to reduce downtime, identify potential threats, and support user confidence.

**Actions:**

1. Attempt incorrect sign-ins to trigger lockout (`labadmin` account)
2. Navigate to **Microsoft Entra ID → Users → Troubleshoot sign-in**
3. Filter logs by user and date to identify failure patterns
4. Analyze key log fields:

   * `Error code 50126` (invalid credentials)
   * Client IP, location, device
5. Simulate support actions: reset password, verify MFA, or escalate if suspicious behavior is detected

---

## 🧠 Skills Demonstrated

* 🧾 **User provisioning & licensing** – Creating secure, well-scoped user accounts
* 🔁 **Credential recovery workflows** – Managing passwords with built-in security controls
* 🔐 **MFA setup & reset procedures** – Strengthening identity assurance
* 🕵️‍♂️ **Sign-in troubleshooting** – Interpreting diagnostic logs to guide resolution
* 🎟️ **Tier 1 ticket realism** – Mirroring everyday helpdesk issues with professional resolution paths
