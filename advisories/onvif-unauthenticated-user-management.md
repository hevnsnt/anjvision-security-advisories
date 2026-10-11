# Unauthenticated ONVIF User Creation, Deletion, and Enumeration

**Researcher:** Bill Swearingen, Trifident Security (hevnsnt@gmail.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-306 (Missing Authentication for Critical Function)
**CVSS 3.1:** 9.8 Critical (AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

The ONVIF device service accepts user-management operations (create, delete, and
enumerate users), including creation of Administrator-level accounts, without
validating authentication. An unauthenticated remote attacker can create an admin
account, use it against the device's authenticated interfaces, and delete it
afterward. This is the entry point for a complete pre-authentication remote code
execution chain.

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
