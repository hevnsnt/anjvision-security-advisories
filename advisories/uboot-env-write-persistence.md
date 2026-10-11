# U-Boot Environment Write From Userspace

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-306 (Missing Authentication for Critical Function)
**CVSS 3.1:** 7.8 High (CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

**Note:** POST-EXPLOITATION.

## Summary

A userspace utility writes arbitrary name/value pairs directly to the U-Boot environment partition. Combined with any code execution, an attacker can rewrite the boot command to achieve bootloader-level persistence that survives firmware reflash and factory reset. Post-exploitation persistence primitive. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

/opt/ch/ssn binary; U-Boot environment partition

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
