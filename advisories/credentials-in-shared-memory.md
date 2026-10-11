# Plaintext Credentials in SysV Shared Memory

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-312 (Cleartext Storage of Sensitive Information)
**CVSS 3.1:** 5.5 Medium (CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:N/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

**Note:** POST-EXPLOITATION.

## Summary

Inter-process communication passes authentication credentials in plaintext through a SysV shared-memory segment readable by any process, all of which run as root with no privilege separation, enabling silent credential harvesting. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

libtools.so IPC shared-memory segment

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
