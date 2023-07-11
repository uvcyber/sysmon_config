# Ultraviolet Sysmon Config

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Attribution

This is based on the work of others in the community. Most of this is credited to the amazingly detailed configuration created by ion-storm, with only a few additions and tweaks.

* [ion-storm/sysmon-config](https://github.com/ion-storm/sysmon-config).

These additional configs lent some inspiration and a few rules.

* [olafhartong/sysmon-modular](https://github.com/olafhartong/sysmon-modular)
* [swiftonsecurity/sysmon-config](https://github.com/SwiftOnSecurity/sysmon-config)
* [neo23x0/sysmon-config](https://github.com/Neo23x0/sysmon-config/)

## Methodology

Detect the most Techniques per data source in MITRE ATT&CK. Provide visibility into forensic artifact events for UEBA. Detect exploitation events with wide CVE coverage. Risk scoring of CVE, UEBA, Forensic, and MITRE ATT&CK events.

## Primary Tags

* `Attack`: Mitre ATT&CK Identifier
* `Technique`: Mitre ATT&CK Technique
* `Tactic`: Mitre ATT&CK Tactic
* `DS`: Mitre ATT&CK Datasource
* `Alert`: Alert Text for SIEM/XDR
* `Info`: Informational Alert Text
* `Level`: The level field contains one of five string values. It describes the criticality of a triggered rule. While low and medium level events have an informative character, events with high and critical level should lead to immediate reviews by security analysts.
* `Desc`: Description of non-alerting Behavioral Based Rules
* `Forensic`: Forensic Artifacts
* `CVE`: CVE Vulnerability Identification
* `FP`: False Positive Rate
* `Author`: Author of rule

---

### Tag Details

#### Risk Score ratings (Risk=??)

* Low Risk: 1-39
* Medium Risk: 40-69
* High Risk: 70-89
* Critical Risk: 90-100

#### Levels (from Sigma)

* (0) informational:
Rule is intended for enrichment of events, e.g. by tagging them. No case or alerting should be triggered by such rules because it is expected that a huge amount of events will match these rules.
* (1) low:
Notable event but rarely an incident. Low rated events can be relevant in high numbers or combination with others. Immediate reaction shouldn't be necessary, but a regular review is recommended.
* (2) medium:
Relevant event that should be reviewed manually on a more frequent basis.
* (3) high:
Relevant event that should trigger an internal alert and requires a prompt review.
* (4) critical:
Highly relevant event that indicates an incident. Critical events should be reviewed immediately.

#### False Positive Rates (FP=?)

* (0) Zero False Positives rate
* (1) Some False Positives rate
* (2) Medium False Positive rate
* (3) High False Positive rate

#### Other Notes

The Rulename field has a hard limit of 255 characters, make the best of the size available, shorten tags and descriptions as needed. Add exclusions in line enclosed within a Compound rule rather than a global exclusion list.
