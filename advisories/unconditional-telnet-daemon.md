# Unconditional Telnet Daemon on Every Boot

**Researcher:** Bill Swearingen, SixCyber LLC (bill@sixcyber.com)
**Vendor:** Anjvision / Anjoy Technology
**Product:** Anjvision ODM IP camera firmware
**Affected versions:** all builds through V3.4.0.10
**Weakness:** CWE-306 (Missing Authentication for Critical Function), CWE-319 (Cleartext Transmission of Sensitive Information)
**CVSS 3.1:** 9.8 Critical (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** CVE ID requested from MITRE CNA-LR. Coordinated disclosure in progress.

## Summary

The production boot script unconditionally starts a telnet daemon on every boot, binding a cleartext root shell service to all interfaces with no feature flag or lockout. Combined with the fleet-identical root hash, cracking the hash once yields root shell access to every reachable device. The firmware ships under more than 20 brand labels including ANPVIZ, SV3C, GWSecurity, Faleemi, Sannce, and Jennov.

## Affected component

boot script; BusyBox telnetd on TCP/23

## Technical details

Full technical details, affected binary offsets, secret values, and proof-of-concept
code are withheld from this public page pending coordinated disclosure. Vendors and
CNAs may request the complete technical package by contacting bill@sixcyber.com.

## Credit

Discovered and reported by Bill Swearingen, SixCyber LLC.
