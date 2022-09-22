# 01 Installing Domain Controller

1. Use 'sconfig' to:
    - Change the hostname
    - Change the IP address to static
    - Change the DNS server to our own IP address

2. Install Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools

Get-NetIPAddress
```
# 02 Joining workstation to domain

```shell
Add-Computer -Domainname xyz.com -Credential xyz\Administrator -Force -Restart
```
