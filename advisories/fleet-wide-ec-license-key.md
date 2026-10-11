# Hard-coded Fleet-Wide EC Public Key for License Verification

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-321 (Use of Hard-coded Cryptographic Key)
**CVSS 3.1:** 7.2 High (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:L/I:L/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

A single elliptic-curve public key on a deprecated curve is shared across the entire fleet for AI detection license verification, with no per-device key provisioning. If the matching private key leaks, unlimited forged licenses can be produced for the entire product line. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

/etc/*.pem license key; mainctrl

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
