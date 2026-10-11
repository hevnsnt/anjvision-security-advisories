# Hard-coded Digest Authentication Nonce

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-323 (Reusing a Nonce, Key Pair in Encryption)
**CVSS 3.1:** 4.8 Medium (CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:L/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

**Note:** NEEDS LIVE VERIFICATION.

## Summary

The ONVIF Digest authentication challenge appears to contain a compile-time-constant nonce. If the nonce is not regenerated per request at runtime, Digest authentication challenges are replayable. Runtime confirmation is pending. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

web_server gSOAP ONVIF Digest challenge

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
