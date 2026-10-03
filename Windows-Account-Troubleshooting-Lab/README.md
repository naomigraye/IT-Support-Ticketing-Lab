# Windows User Account Troubleshooting Lab

## Scenario
A user reported that they were unable to sign in to their Windows account. The goal was to identify the account issue, restore access, and verify that the user could successfully sign in.

## Environment
- Windows 10
- Local Windows user account
- Administrator Command Prompt
- Standard user account: SupportUser

## Troubleshooting Process
1. Created a standard local user account named `SupportUser`.
2. Used `net user SupportUser` to verify the account configuration.
3. Disabled the account to simulate a user being unable to sign in.
4. Used `net user SupportUser` to investigate the account and found that `Account active` was set to `No`.
5. Re-enabled the account using:
   `net user SupportUser /active:yes`
6. Ran `net user SupportUser` again and confirmed that `Account active` was now set to `Yes`.
7. Signed into the SupportUser account to verify that access had been restored.

## Resolution
The login issue was caused by the local user account being disabled. After re-enabling the account, the user was able to successfully sign in.

## Skills Practiced
- Windows user account management
- Command Prompt
- `net user`
- Account troubleshooting
- User access management
- Problem identification and resolution
- Verification and documentation
