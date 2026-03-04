# 🔎 Security Incident Investigation

## 📌 Scenario

A company security monitoring system detected suspicious activity on an internal workstation.
The workstation attempted multiple login attempts followed by unusual outbound network connections.

The SOC team initiated a full investigation to determine if the system was compromised.

---

## 📂 Initial Alert

Alert Type: Suspicious Login Activity

Example log:

```text
Timestamp            User     Source IP       Action
-----------------------------------------------------
2026-03-04 11:15:03  admin    203.45.77.12    Login Failed
2026-03-04 11:15:07  admin    203.45.77.12    Login Failed
2026-03-04 11:15:12  admin    203.45.77.12    Login Success
```

Observation:

Multiple failed login attempts followed by a successful login.

Possible indicator of a brute-force attack.

---

## 🌐 Suspicious Network Activity

Shortly after the login event, the system initiated outbound connections.

Example network log:

```text
Timestamp           Source IP       Destination IP     Port
------------------------------------------------------------
2026-03-04 11:16:22 192.168.1.50    185.199.110.10     443
2026-03-04 11:16:30 192.168.1.50    185.199.110.10     443
```

Observation:

Repeated communication with unknown external server.

Possible command-and-control communication.

---

## ⚠ Indicators of Compromise (IOC)

Identified indicators:

* Suspicious external IP address
* Multiple failed login attempts
* Unusual outbound network traffic
* Possible compromised administrator account

---

## 🔎 Investigation Steps

SOC analysts performed the following actions:

1. Reviewed authentication logs
2. Investigated network traffic
3. Checked endpoint processes
4. Verified external IP reputation
5. Collected forensic evidence

---

## 🛠 Incident Response

Recommended actions:

* Isolate affected workstation
* Reset compromised account credentials
* Block malicious IP address
* Perform malware scan
* Monitor network for additional suspicious activity

---

## 🧠 MITRE ATT&CK Techniques

Possible techniques observed:

T1110 – Brute Force
T1071 – Application Layer Protocol

These techniques are commonly used in credential attacks and command-and-control communication.

---

## 🔐 Security Improvements

Recommended improvements:

* Enable Multi-Factor Authentication
* Implement SIEM alerting rules
* Monitor authentication logs
* Restrict external network connections

---

## 🎯 Skills Demonstrated

* Security incident investigation
* Log analysis
* Threat detection
* Incident response
* MITRE ATT&CK framework usage
* Cybersecurity documentation

