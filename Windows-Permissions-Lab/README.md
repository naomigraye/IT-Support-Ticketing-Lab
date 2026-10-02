# Windows File Permissions Troubleshooting Lab

## Scenario
A user reported that they could see a required folder on the computer but received an access denied message when attempting to open it.

## Objective
Troubleshoot the user's folder access issue, identify the cause, correct the permissions, and verify that the user could access the folder successfully.

## Environment
- Windows
- Local User Accounts
- Command Prompt
- NTFS File Permissions
- ICACLS

## Lab Setup
Created a local test user named `LabUser` using Command Prompt.

Created a test folder:

`C:\SupportLab`

Created a test file inside the folder:

`employee-data.txt`

An explicit DENY permission was intentionally assigned to LabUser to simulate a real user access issue.

## Troubleshooting Process

### 1. Reproduced the Issue
Signed into Windows as LabUser and attempted to open `C:\SupportLab`.

Windows displayed an error indicating that the user did not have permission to access the folder.

### 2. Investigated Folder Permissions
Checked the folder's security permissions and confirmed that LabUser could not read the folder permissions.

Returned to the administrator account and used the following command:

`icacls C:\SupportLab`

The ACL showed an explicit DENY permission assigned to LabUser.

### 3. Identified the Root Cause
The explicit DENY entry prevented LabUser from accessing the folder even though other user groups had permissions.

### 4. Resolved the Issue
Removed the incorrect DENY permission using:

`icacls C:\SupportLab /remove:d LabUser`

Windows confirmed that the folder was processed successfully.

### 5. Verified the Resolution
Ran `icacls C:\SupportLab` again to confirm that the LabUser DENY entry had been removed.

Signed back into the LabUser account and opened `C:\SupportLab`.

The user was able to successfully access the folder and view `employee-data.txt`.

## Resolution
Removed the incorrect explicit DENY permission from the affected user account and verified successful folder access.

## Skills Practiced
- Windows Troubleshooting
- NTFS File Permissions
- User Account Management
- Access Control Lists (ACLs)
- Command Prompt
- ICACLS
- Root Cause Analysis
- User Access Troubleshooting
- Issue Verification
- Technical Documentation

## What I Learned
This lab helped me understand how Windows file permissions can prevent users from accessing resources and how to use ICACLS to inspect and modify access control entries. I also practiced reproducing an issue from the user's perspective, identifying the root cause, applying a fix, and verifying the resolution.
