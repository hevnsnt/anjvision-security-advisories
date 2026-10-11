# Hardcoded DES Key for Vendor SOAP API Authentication

**Researcher:** Bill Swearingen, Trifident Security (hevnsnt@gmail.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-321 (Use of Hard-coded Cryptographic Key), CWE-327 (Broken Cryptographic Algorithm)
**CVSS 3.1:** 7.5 High (AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

The vendor SOAP API authenticates using a DES-ECB construction with a static key
embedded in the firmware. Any party with the publicly downloadable firmware image
can compute valid authentication tokens for any credential pair, rendering the
authentication scheme effectively plaintext.

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
