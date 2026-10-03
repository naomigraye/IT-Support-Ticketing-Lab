# Network Troubleshooting Lab

## Scenario
A user is experiencing network connectivity issues. The goal of this lab was to troubleshoot IPv4 connectivity, renew the network configuration, test DNS resolution, and verify that connectivity was restored.

## Environment
- Windows 10
- Command Prompt
- Wi-Fi connection

## Troubleshooting Performed

### 1. IPv4 / DHCP Troubleshooting
- Verified the computer's current network connectivity.
- Used `ipconfig /release` to release the existing IPv4 address.
- Checked the network configuration with `ipconfig`.
- Used `ipconfig /renew` to request a new IPv4 address from DHCP.
- Confirmed that the computer received a new IPv4 address and default gateway.
- Used `ping -4 google.com` to verify IPv4 connectivity after the renewal.

### 2. DNS Troubleshooting
- Used `ipconfig /displaydns` to inspect the local DNS resolver cache.
- Used `nslookup google.com` to verify DNS name resolution.
- Used `ipconfig /flushdns` to clear the DNS resolver cache.
- Ran `nslookup google.com` again to confirm DNS resolution was working after the cache was cleared.

## Resolution
The IPv4 configuration was successfully renewed and network connectivity was verified. DNS resolution was also tested, the DNS resolver cache was cleared, and name resolution continued to work correctly.

## Commands Used

`ipconfig /release`

`ipconfig /renew`

`ipconfig`

`ping -4 google.com`

`ipconfig /displaydns`

`nslookup google.com`

`ipconfig /flushdns`

## Skills Practiced
- Windows network troubleshooting
- TCP/IP fundamentals
- DHCP troubleshooting
- IPv4 configuration
- DNS troubleshooting
- Command Prompt
- Connectivity testing
- Technical documentation
