# Cloud Platform Re-Registration Without Authentication

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-284 (Improper Access Control)
**CVSS 3.1:** 7.1 High (CVSS:3.1/AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

**Note:** POST-EXPLOITATION.

## Summary

A userspace utility supports re-registering the camera to any of several cloud platforms without additional authentication. An attacker with code execution can silently redirect the video feed, control channel, and alarm events to an attacker-controlled cloud, persisting across reboots. Post-exploitation primitive. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

/opt/ch/ssn binary

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
