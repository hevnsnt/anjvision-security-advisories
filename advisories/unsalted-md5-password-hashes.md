# Unsalted MD5 Storage of Web UI Credentials

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-916 (Use of Password Hash With Insufficient Computational Effort)
**CVSS 3.1:** 7.5 High (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

All web UI account passwords are stored as unsalted MD5 digests with no per-user salt or iteration count. Identical passwords produce identical hashes across the fleet, and any party obtaining the configuration recovers plaintext passwords via rainbow tables. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

device configuration (config.xml) password attributes

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
