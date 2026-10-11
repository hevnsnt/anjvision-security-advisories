# Stored OS Command Injection via Device Hostname

**Researcher:** Bill Swearingen, Trifident Security (hevnsnt@gmail.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-78 (OS Command Injection)
**CVSS 3.1:** 7.2 High (AV:N/AC:L/PR:H/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

A stored configuration value (the device hostname) is interpolated into a shell
command built by a test routine and executed as root without sanitization. An
attacker sets a hostname containing shell metacharacters, then triggers the routine
to execute injected commands.

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
