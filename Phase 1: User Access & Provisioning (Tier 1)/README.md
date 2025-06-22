🔰 Phase 1: User Access & Provisioning (Tier 1)
🎯 Objective:
Simulate the most common Tier 1 helpdesk requests for Microsoft 365 users:

Password resets

MFA issues

User account creation

License assignments

Account lockouts

🛠 Tools You’ll Use:
Microsoft 365 Admin Center

Microsoft Entra ID (Azure AD)

Microsoft Authenticator / MFA settings

Outlook / Teams web portals

✅ Step-by-Step Tasks
Step 1: Create a New User (Provisioning)
Go to Microsoft 365 Admin Center → Users → Active users → Add a user.

Fill in:

Name, username (e.g., john.doe@yourtenant.onmicrosoft.com)

Auto-generate password

Leave "Require password change" enabled

Assign at least one license (Microsoft 365 E5 preferred for full features).

📸 Screenshot: User creation summary page
📛 Caption: Creating a new user with a Microsoft 365 license

Step 2: Reset User Password
Select the user → Reset password.

Choose Auto-generate or custom password.

📸 Screenshot: Reset password dialog
📛 Caption: Resetting a user password from the M365 Admin Center

Step 3: Configure MFA
Go to Microsoft Entra ID → Users → Select the user → Authentication methods.

Ensure default sign-in method is set (Authenticator App or Phone).

Simulate registration or initiate a re-registration if needed.

📸 Screenshot: Authentication methods blade
📛 Caption: Viewing and editing MFA settings in Microsoft Entra

Step 4: Simulate Account Lockout
Manually attempt login with incorrect credentials until lockout (optional).

Go to Entra ID → Users → Troubleshoot sign-in.

Review sign-in logs and clear lockout if needed.

📸 Screenshot: Troubleshoot sign-in logs
📛 Caption: Investigating user sign-in failures using Entra ID logs

Step 5: Assign or Remove Licenses
Go to the user → Licenses and apps → Assign or unassign E5, Teams, etc.

Save and verify license assignment propagates.

📸 Screenshot: License assignment screen
📛 Caption: Assigning Microsoft 365 E5 licenses during user provisioning

