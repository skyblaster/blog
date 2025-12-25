---
draft: false
comments: true
icon: simple/gnometerminal
date: 2025-12-09 
title: Posh-ACME Article
---

# Test

```powershell title="install_poshacme.ps1"
Install-Module -Name Posh-ACME
Import-Module -Name Posh-ACME
Set-PAServer LE_PROD
New-PACertificate '*.example.com' -AcceptTOS
(Get-PACertificate).Cert
```

```powershell title="copy_certs.ps1"
cp (Get-PACertificate).Cert /var/mcc
```