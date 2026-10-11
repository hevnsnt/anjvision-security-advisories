# OS Command Injection via FTP Test Configuration

**Researcher:** Bill Swearingen, Trifident Security (hevnsnt@gmail.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-78 (OS Command Injection)
**CVSS 3.1:** 9.8 Critical (AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

The FTP test configuration handler passes multiple user-controlled configuration
values into a shell script invocation without sanitization, executing them as
root. A secondary injection exists within the invoked shell script itself. This is
a distinct code path and sink from the SMTP injection.

## Affected products

Anjvision / Anjoy Technology ODM IP camera firmware shipped under 20+ brands
(ANPVIZ, SV3C, GWSecurity, Faleemi, KKB, CCDCAM, Sannce, Loosafe, Hiseeu, Eyoyo,
Jennov, and others). Confirmed on ANPVIZ IPC-D3243W-S V3.4.0.10.

## Technical details

Full technical details, affected binary offsets, and proof-of-concept code are
withheld from this public page pending coordinated disclosure. Vendors and CNAs
may request the complete technical package by contacting hevnsnt@gmail.com.

## Credit

Discovered and reported by Bill Swearingen, Trifident Security.
