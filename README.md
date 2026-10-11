# Anjvision ODM IP Camera Firmware Security Advisories

Security research by **Bill Swearingen, Trifident Security** (hevnsnt@gmail.com).

These advisories cover vulnerabilities in the Anjvision / Anjoy Technology ODM IP
camera firmware, which ships under 20+ brand labels including ANPVIZ, SV3C,
GWSecurity, Faleemi, KKB, CCDCAM, Sannce, Loosafe, Hiseeu, Eyoyo, and Jennov.

**Tested device:** ANPVIZ IPC-D3243W-S, firmware V3.4.0.10 (build 2025-05-06).
**Affected versions:** all builds through V3.4.0.10. Vulnerable primitives were
observed in 1,163 of 1,511 analyzed firmware builds (earliest 2017). No patched
build has shipped as of this writing.

## Status

Coordinated disclosure is in progress. CVE IDs have been requested from the MITRE
CNA of Last Resort. Full technical details, binary offsets, and proof-of-concept
code are **withheld** from these public pages pending vendor notification and the
coordinated disclosure window. Vendors and CNAs may request the full technical
package under coordinated disclosure by contacting hevnsnt@gmail.com.

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

## Disclosure Contact

Bill Swearingen, Trifident Security, hevnsnt@gmail.com
