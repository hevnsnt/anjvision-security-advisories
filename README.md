# Anjvision ODM IP Camera Firmware Security Advisories

Security research by **Bill Swearingen, SixCyber LLC** (bill@sixcyber.com).

These advisories cover vulnerabilities in the Anjvision / Anjoy Technology ODM IP
camera firmware, which ships under 20+ brand labels including ANPVIZ, SV3C,
GWSecurity, Faleemi, KKB, CCDCAM, Sannce, Loosafe, Hiseeu, Eyoyo, and Jennov.

**Tested device:** ANPVIZ IPC-D3243W-S, firmware V3.4.0.10 (build 2025-05-06).
**Affected versions:** all builds through V3.4.0.10. Vulnerable primitives were
observed in 1,163 of 1,511 analyzed firmware builds (earliest 2017). No patched
build has shipped as of this writing.

## Status

**29 CVE requests were filed with the MITRE CNA of Last Resort (CNA-LR) on 2026-10-11.**
CVE IDs are pending assignment and will be listed here as MITRE issues them. One further
finding (ONVIF Digest authentication nonce) is held pending live verification and has not
been submitted.

| Date | Milestone |
|------|-----------|
| 2026-10-11 | 29 CVE IDs requested from MITRE CNA-LR; publication deferred (coordinated disclosure) |
| pending | CVE IDs assigned by MITRE — to be published here |

Coordinated disclosure is in progress. Full technical details, binary offsets, and
proof-of-concept code are **withheld** from these public pages pending vendor notification
and the coordinated disclosure window. Vendors and CNAs may request the full technical
package under coordinated disclosure by contacting bill@sixcyber.com.

## Advisory Index

| Advisory | Class (CWE) | CVSS 3.1 |
|----------|-------------|----------|
| [Vendor super-password backdoor](advisories/super-password-backdoor.md) | CWE-259 / CWE-912 | 9.8 Critical |
| [Unauthenticated ONVIF user management](advisories/onvif-unauthenticated-user-management.md) | CWE-306 | 9.8 Critical |
| [SMTP configuration command injection](advisories/smtp-command-injection.md) | CWE-78 | 9.8 Critical |
| [FTP configuration command injection](advisories/ftp-command-injection.md) | CWE-78 | 9.8 Critical |
| [File-deletion handler command injection](advisories/file-delete-command-injection.md) | CWE-78 | 9.8 Critical |
| [Log-file deletion handler command injection](advisories/logfile-delete-command-injection.md) | CWE-78 | 9.8 Critical |
| [Device hostname command injection](advisories/hostname-command-injection.md) | CWE-78 | 7.2 High |
| [DDNS configuration command injection](advisories/ddns-command-injection.md) | CWE-78 | 7.2 High |
| [MAC-address command injection](advisories/mac-address-command-injection.md) | CWE-78 | 7.2 High |
| [Systemic unsanitized shell execution](advisories/systemic-command-injection.md) | CWE-78 / CWE-676 | 7.2 High |
| [Hardcoded DES "WebLogin" API key](advisories/des-weblogin-hardcoded-key.md) | CWE-321 / CWE-327 | 7.5 High |
| [Unauthenticated ONVIF information disclosure](advisories/onvif-unauthenticated-info-disclosure.md) | CWE-200 | 7.5 High |

### Additional advisories (batch 2)

| Advisory | Class (CWE) | CVSS 3.1 |
|----------|-------------|----------|
| [Unauthenticated Firmware Upload](advisories/unauthenticated-firmware-upload.md) | CWE-306/CWE-345 | 9.8 Critical |
| [Unauthenticated Tls Certificate Replacement](advisories/unauthenticated-tls-certificate-replacement.md) | CWE-306 | 8.6 High |
| [Unauthenticated Arbitrary File Upload](advisories/unauthenticated-arbitrary-file-upload.md) | CWE-306/CWE-434 | 9.1 Critical |
| [Fleet Identical Root Password Hash](advisories/fleet-identical-root-password-hash.md) | CWE-798/CWE-916 | 9.8 Critical |
| [Unconditional Telnet Daemon](advisories/unconditional-telnet-daemon.md) | CWE-306/CWE-319 | 9.8 Critical |
| [Default Administrator Credentials](advisories/default-administrator-credentials.md) | CWE-1392 | 9.8 Critical |
| [Unauthenticated Udp Broadcast Control](advisories/unauthenticated-udp-broadcast-control.md) | CWE-306 | 9.1 Critical |
| [Hikvision Sdk Authentication Disabled](advisories/hikvision-sdk-authentication-disabled.md) | CWE-306 | 7.5 High |
| [Unsalted Md5 Password Hashes](advisories/unsalted-md5-password-hashes.md) | CWE-916 | 7.5 High |
| [Timing Side Channel Password Comparison](advisories/timing-side-channel-password-comparison.md) | CWE-208 | 5.9 Medium |
| [Hardcoded Digest Auth Nonce](advisories/hardcoded-digest-auth-nonce.md) (held, not submitted — pending live verification) | CWE-323 | 4.8 Medium |
| [Fleet Wide Ec License Key](advisories/fleet-wide-ec-license-key.md) | CWE-321 | 7.2 High |
| [Uboot Env Write Persistence](advisories/uboot-env-write-persistence.md) | CWE-306 | 7.8 High |
| [Cloud Platform Reregistration](advisories/cloud-platform-reregistration.md) | CWE-284 | 7.1 High |
| [Wifi Psk Cleartext Storage](advisories/wifi-psk-cleartext-storage.md) | CWE-312 | 5.5 Medium |
| [Credentials In Shared Memory](advisories/credentials-in-shared-memory.md) | CWE-312 | 5.5 Medium |
| [Default Wifi Ssid Psk](advisories/default-wifi-ssid-psk.md) | CWE-1188 | 7.5 High |
| [Alarm Snapshots Cleartext Http](advisories/alarm-snapshots-cleartext-http.md) | CWE-319 | 6.5 Medium |

## Disclosure Contact

Bill Swearingen, SixCyber LLC, bill@sixcyber.com
