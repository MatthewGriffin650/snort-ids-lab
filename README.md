# Snort IDS Labs

Hands-on Snort IDS rule development and testing completed in a controlled cybersecurity lab environment.

## Overview

This project contains custom Snort rules created and tested as part of a network intrusion detection lab.

The lab focused on writing Snort rules to detect specific network activity and verifying that each rule generated the expected alert when triggered.

## Rules

The custom rules are stored in `rules/local.rules`.

| SID | Detection |
|---|---|
| 100001 | ICMP ping traffic |
| 100002 | FTP download of `myfile.txt` |
| 100003 | FTP login attempt using the configured NetID |
| 100004 | HTTP request for `/Secret-Plans.txt` |
| 100005 | `cat` command over TCP port 4444 |

## Testing

Each rule was tested individually in the lab environment.

The `testing/` directory contains documentation for each test, including the commands used to trigger the rules.

The `screenshots/` directory contains screenshots showing the test activity and corresponding Snort alerts.

## Repository Structure

```text
snort-ids-lab/
├── README.md
├── rules/
│   └── local.rules
├── screenshots/
│   ├── snort-screenshot-01.png
│   ├── snort-screenshot-02.png
│   ├── snort-screenshot-03.png
│   ├── snort-screenshot-04.png
│   └── snort-screenshot-05.png
└── testing/
    └── README.md
```

## Skills Demonstrated

- Snort IDS rule development
- Network traffic analysis
- Signature-based detection
- ICMP, FTP, and HTTP traffic analysis
- Content-based detection
- Snort rule syntax
- IDS alert validation
- Testing security detection rules in a controlled environment
