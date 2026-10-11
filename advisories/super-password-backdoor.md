# Vendor Super-Password Backdoor in Anjvision IP Camera Firmware

**Researcher:** Bill Swearingen, Trifident Security (hevnsnt@gmail.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-259 (Use of Hard-coded Password), CWE-912 (Hidden Functionality)
**CVSS 3.1:** 9.8 Critical (AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

The device authentication handler contains an undocumented secondary
authentication path. When the user-configured password check fails, the firmware
derives a valid administrator password deterministically from the device serial
number using a fixed algorithm, and accepts it. The serial number is disclosed
without authentication via the ONVIF service, so the backdoor credential can be
computed offline by any remote attacker who can reach the device. The derivation
is identical across the entire device fleet and cannot be disabled or changed by
the device owner. The exact derivation is withheld pending coordinated disclosure.

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
