# 00 Installation process

1- Add a computer with WinRM
```
//Enter Creds
New-PSSession -ComputerName 192.168.24.128 -Credential (Get-Credential)


Enter-PSSession 1
```

+ Change the core server `sconfig`
    + Change the host name
    + Change the IP address to static
    + Change the DNS server to our own IP Address


+ Install AD features
    + To see the windows feature that related to active directory

```shell
Get-WindowsFeature | ? {$_.Name -LIKE "Ad*"}
```
```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```
