# Day-16 – Microsoft Graph Authentication & User Management

## 🎯 Objective

Continue progressing through the MS-102 learning path by exploring:

- Microsoft Graph authentication
- Microsoft Graph PowerShell
- User administration through Graph
- Modern Microsoft management tools
- Tenant automation concepts

---

## 🌐 Microsoft Graph Connection

Following the successful installation of the Microsoft Graph PowerShell module, the next step was connecting to the tenant.

Used the command:

```powershell
Connect-MgGraph -Scopes "Group.ReadWrite.All","User.ReadWrite.All"
```

Purpose:

```plaintext
Authenticate to Microsoft Graph
Request permissions to manage users and groups
```

---

## 🔐 Authentication

Authenticated using:

```plaintext
rg@rg-wutanglan.co.uk
```

The connection was successful because the account already exists within the Microsoft 365 tenant.

Learning point:

If connecting from outside the organisation or in more complex environments, it may be necessary to specify:

```plaintext
Tenant ID
```

during authentication.

---

## ✅ Microsoft Graph Connection Validation

After successful authentication, Microsoft Graph was able to communicate with the tenant.

This provided practical experience with:

- Microsoft Graph authentication
- Delegated permissions
- Modern Microsoft administration
- Graph PowerShell workflows

---

## 👥 Retrieving Tenant Users

Used Microsoft Graph to retrieve all users currently within the tenant.

Command:

```powershell
Get-MgUser -All
```

Purpose:

```plaintext
Display all users in the tenant
```

This demonstrated how Microsoft Graph can retrieve tenant information without navigating through multiple administration portals.

---

## 🚀 User Creation with Microsoft Graph

Created a new user directly through Microsoft Graph PowerShell.

Command used:

```powershell
New-MgUser `
-AccountEnabled:$true `
-DisplayName "Jurriën Timber" `
-MailNickname "jurrientimber" `
-UserPrincipalName "jtimber@rg-wutanglan.co.uk" `
-PasswordProfile @{
    ForceChangePasswordNextSignIn = $true
    Password = "P@ssword123!"
}
```

---

## ⚙️ User Configuration

User created:

```plaintext
Jurriën Timber
```

UPN:

```plaintext
jtimber@rg-wutanglan.co.uk
```

Account Status:

```plaintext
Enabled
```

Password Configuration:

```plaintext
Force password change on first sign-in
```

This follows a common onboarding practice used in many organisations.

---

## 🏆 Football-Themed Tenant Expansion

To maintain consistency with the existing football-themed tenant structure, added:

```plaintext
Jurriën Timber
```

to the Microsoft 365 environment.

Current tenant users now include:

```plaintext
Saka
Yamal
Jude Bellingham
Gabriel
Declan Rice
William Saliba
David Raya
Jurriën Timber
```

along with existing administration and lab accounts.

---

## 📚 Learning Reflection

Today's session introduced practical Microsoft Graph administration.

Key concepts explored:

```plaintext
Microsoft Graph Authentication
Graph Permissions
User Retrieval
User Creation
Modern Administration
PowerShell Automation
```

A major takeaway was seeing how Microsoft Graph allows administrators to perform management tasks through code rather than relying solely on graphical portals.

Traditional workflow:

```plaintext
Portal
↓
Click
↓
Create User
```

Microsoft Graph workflow:

```plaintext
PowerShell
↓
Command
↓
Create User
```

This provides opportunities for:

- Automation
- Bulk administration
- Consistency
- Large-scale management

---

## 🔜 Next Steps

Potential future labs:

- Create groups using Microsoft Graph
- Add users to groups using Graph
- Assign licences using Graph
- Query device information
- Explore Microsoft Graph permissions further
- Continue MS-102 automation topics
