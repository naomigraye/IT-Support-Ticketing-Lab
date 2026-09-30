# IT Support Ticketing Lab

## Overview

This project documents my hands-on practice with IT support and help desk ticket simulations. I worked through common user issues, diagnosed problems, performed troubleshooting, documented my findings, and resolved or escalated tickets based on the issue.

The goal of this project is to build practical experience with the types of tasks performed in entry-level Help Desk, IT Support, and Technical Support roles.

## Environment

- SysDesks Workstation / Help Desk Console
- Windows
- Active Directory
- Command Prompt
- PowerShell
- VPN and network troubleshooting
- Ticket documentation

## Skills Practiced

- Help desk ticket management
- Troubleshooting user-reported issues
- Active Directory account management
- User account deprovisioning
- Windows troubleshooting
- Application troubleshooting
- VPN troubleshooting
- Network connectivity testing
- IP and routing troubleshooting
- Command-line diagnostics
- Printer troubleshooting
- Browser troubleshooting
- File and workstation troubleshooting
- Writing resolution notes
- Communicating technical issues to users
- Determining when an issue should be resolved or escalated

## Ticket Examples

### 1. VPN / Internal Application Connectivity

**Issue:**  
A user reported that internal applications and network shares repeatedly became unavailable while connected to the VPN.

**Troubleshooting:**
- Reviewed the active VPN connection.
- Checked the networks being routed through the VPN tunnel.
- Identified that the target internal network was not included in the current VPN route.
- Connected to the appropriate VPN gateway.
- Tested connectivity to the internal resource using `ping`.

**Verification:**  
Successfully received responses from the internal host with 0% packet loss.

**Resolution:**  
Connected the user to the appropriate VPN gateway and verified that the internal network was reachable.

---

### 2. Active Directory Account Deprovisioning

**Issue:**  
An unused test account from a previous migration was identified during a security review.

**Troubleshooting / Action:**
- Located the account in Active Directory.
- Reviewed the account information before making changes.
- Confirmed the requested account.
- Removed the unused account.
- Verified that the account no longer appeared in the directory.

**Resolution:**  
Successfully removed the unused test account from Active Directory.

---

### 3. Windows Drive / File System Issue

**Issue:**  
A user reported that applications were crashing while saving files and Windows was reporting a drive problem.

**Troubleshooting:**
- Used PowerShell to review volume health.
- Identified a warning on the system volume.
- Ran `chkdsk C: /scan`.
- Confirmed that Windows detected file system problems.
- Determined that the required repair needed elevated permissions.

**Resolution:**  
Documented the diagnostic results and escalated the issue for elevated repair rather than attempting changes outside Tier 1 support scope.

---

### 4. Network Connectivity Troubleshooting

**Issue:**  
A workstation was unable to properly access network resources.

**Troubleshooting:**
- Reviewed the device's network connection.
- Checked the active network configuration.
- Used command-line tools to test connectivity.
- Verified whether the workstation could communicate with network resources.

**Resolution:**  
Restored and verified network connectivity using standard troubleshooting and connectivity testing.

---

### 5. General Help Desk Troubleshooting

During the lab, I also worked through tickets involving:

- Printer problems
- Browser configuration issues
- Application problems
- User account issues
- File recovery
- Workstation troubleshooting
- Network and internet connectivity

For each ticket, I practiced identifying the reported problem, gathering information, troubleshooting the issue, documenting the work performed, and selecting the appropriate resolution or escalation path.

## What I Learned

These simulations helped me practice a structured troubleshooting process instead of immediately making changes to a system. I learned to gather information first, test possible causes, verify whether a solution worked, and document the final result.

I also practiced recognizing when an issue requires elevated permissions or should be escalated instead of attempting changes outside the scope of Tier 1 support.

## Areas I Am Continuing to Improve

- Verifying user identity before account-related changes
- Confirming resolution with the requester before closing tickets
- Active Directory and identity management
- Windows command-line troubleshooting
- Network diagnostics
- Ticket documentation
- Troubleshooting issues independently

## Career Focus

I am currently building hands-on technical skills for entry-level roles in:

- IT Support
- Help Desk
- Technical Support
- Desktop Support

I plan to continue adding troubleshooting labs and IT support projects as I develop my skills.
