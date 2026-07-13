# Windows Server 2022 Setup & Domain Controller

## Step 1: Select Roles and Features for Active Directory Domain Services

![Active Directory roles and features selection dialog showing required role services and features](./images/screenshot-1.png)

This screen displays the Add Roles and Features Wizard where you select which roles to install. The dialog shows:

**Left Panel - Available Roles:**
- Active Directory Certificate Services
- Active Directory Domain Services (highlighted)
- Active Directory Federation Services
- Active Directory Lightweight Directory Services
- Active Directory Rights Management Services
- DHCP Server
- DNS Server
- Fax Server
- File and Storage Services
- Host Guardian Service
- Hyper-V
- Network Policy and Access Services
- Print and Document Services
- Remote Access
- Remote Desktop Services
- Volume Activation Services

**Right Panel - Required Dependencies:**
The wizard displays a warning indicating that you cannot install Active Directory Domain Services unless the following role services or features are also installed:
- **[Tools] Group Policy Management**
- **Remote Server Administration Tools**
  - Role Administration Tools
    - AD DS and AD LDS Tools
    - Active Directory module for Windows PowerShell
  - **[Tools] AD DS Tools**
    - Active Directory Administrative Center
    - AD DS Snap-Ins and Command-Line Tools

---

## Step 2: Administrator Login

![Windows login screen with DALE\\Administrator user account selected](./images/screenshot-2.png)

The Windows Server 2022 login screen displays:

- **User Account:** DALE\Administrator (Domain Account)
- **Password field:** Ready for credential entry
- **Additional users available:** Other user account option shown in the bottom left
- **Accessibility features:** Language and accessibility options available in bottom right

Log in with your Administrator credentials to proceed with the domain controller setup.

---

## Step 3: Add Roles and Features Wizard - Before You Begin

![Server Manager Add Roles and Features Wizard showing prerequisites checklist](./images/screenshot-3.png)

The wizard presents a "Before You Begin" screen with important prerequisites to verify:

**Prerequisite Checklist:**
- ✓ The Administrator account has a strong password
- ✓ Network settings, such as static IP addresses, are configured
- ✓ The most current security updates from Windows Update are installed

**Navigation Steps (Left Panel):**
1. Before You Begin (current)
2. Installation Type
3. Server Selection
4. Server Roles
5. Features
6. Confirmation
7. Results

**Important Note:** If you need to remove roles, role services, or features, use the "Remove Roles and Features Wizard" from the Server Manager dashboard. Click "Next" to continue after verifying all prerequisites are complete.

---

## Step 4: Customize Administrator Settings

![Windows setup screen for customizing administrator account password](./images/screenshot-4.png)

The "Customize settings" screen prompts you to configure the built-in administrator account:

**Fields to Configure:**
- **User name:** Administrator (pre-filled)
- **Password:** [Hidden for security]
- **Reenter password:** [Hidden for security]

**Important:** Type a strong password for the built-in administrator account that you will use to sign in to this computer. This is a critical security step for your Domain Controller.

Click the "Finish" button (bottom right) to complete the setup process.

---

## Summary

This guide covers the essential steps to set up Windows Server 2022 as a Domain Controller:

1. Select Active Directory Domain Services and its required role services
2. Log in with administrator credentials
3. Verify all prerequisites are met (strong password, static IP, security updates)
4. Configure a strong administrator password for the domain controller
5. Complete the wizard to finalize the installation

After these steps, your Windows Server 2022 Domain Controller will be configured and ready for use in your Active Directory environment.