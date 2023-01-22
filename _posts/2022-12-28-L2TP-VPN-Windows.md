---
title: L2TP VPN Setup for Windows
date: 2022-12-28 12:00:00
categories: [Windows]
tags: [Windows,VPN]
---

# L2TP VPN Setup for Windows 

Create the following registry entry (restart PC after)

```
Location = HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\PolicyAgent
Type = DWORD (32-bit) Value
Name = AssumeUDPEncapsulationContextOnSendRule
Value = 2
```

When creating the L2TP VPN
Make sure to:

Select Microsoft: Secured Password (EAP-MSCHAP v2) under Security > Authentication

Enter Pre-shared key

Disable Use default gateway on remote network under IPv4 settings, Advanced
