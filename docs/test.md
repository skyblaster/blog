---
draft: false 
icon: simple/gnometerminal
date: 2025-12-09 
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

## Sub Heading

### Sub sub heading
