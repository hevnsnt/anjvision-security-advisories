# Unauthenticated Firmware Upload Without Signature Verification

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-306 (Missing Authentication for Critical Function), CWE-345 (Insufficient Verification of Data Authenticity)
**CVSS 3.1:** 9.8 Critical (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

A multipart firmware-upload endpoint can be reached without authentication through a request-routing flag that skips the authentication check, and the uploaded image is written and flashed without any cryptographic signature verification. A remote unauthenticated attacker can install malicious firmware that survives factory reset. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

multipart upload handler (libcgibin.so), POST /IPC_FirmwareUpgrade

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
