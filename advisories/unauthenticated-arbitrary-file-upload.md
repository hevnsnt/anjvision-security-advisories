# Unauthenticated Arbitrary File Upload

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-306 (Missing Authentication for Critical Function), CWE-434 (Unrestricted Upload of File with Dangerous Type)
**CVSS 3.1:** 9.1 Critical (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

An arbitrary file can be written to the device filesystem through an upload endpoint reachable without authentication via the request-routing flag bypass. A remote unauthenticated attacker can write files to attacker-influenced paths. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

multipart upload handler (libcgibin.so), POST /WebUploadFormFile

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
