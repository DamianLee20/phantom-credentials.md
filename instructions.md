# Facilitator Guide – Phantom Credentials Tabletop Exercise

This document provides instructions and timing guidance for running the “Phantom Credentials – Initial Access & Pivoting Drill” tabletop cybersecurity exercise.

## 🎬 Before the Exercise

- Review all scenario materials in `phantom-credentials.md`
- Assign participant roles: SOC analyst, Sysadmin, IT Director, etc.
- Prepare artifacts:
  - `phishing_email.txt`: Present to finance team role
  - `vpn_log_sample.txt`: Provide during initial response
  - `ad_alert_event.txt`: Present when attacker escalates

## 🧩 Exercise Flow

### Phase 1: Initial Access
**Inject**: Share `phishing_email.txt`  
**Discussion**: Ask participants how they'd identify, report, and block the phishing attempt.

### Phase 2: Credential Abuse
**Inject**: Share `vpn_log_sample.txt`  
**Discussion**: Participants should detect geo-anomalous login and begin incident response.

### Phase 3: Lateral Movement
**Narration**: Inform team that attacker is accessing internal shares and probing the network.  
**Discussion**: What monitoring tools are used? Any alerts triggered?

### Phase 4: Escalation
**Inject**: Share `ad_alert_event.txt`  
**Discussion**: Ask what immediate actions should be taken and how escalation occurs.

## ⏱️ Suggested Timing

| Phase | Duration |
|-------|----------|
| Setup / Briefing | 10 minutes |
| Phase 1 – Phishing | 15 minutes |
| Phase 2 – VPN Logs | 15 minutes |
| Phase 3 – Lateral Movement | 10 minutes |
| Phase 4 – Escalation | 10 minutes |
| Debrief | 15 minutes |

## 🧠 Debrief Questions

- What went well during this scenario?
- Were any gaps identified in detection, tools, or processes?
- Did communication flow effectively?
- What changes would you recommend?

---

Facilitated by: Damian Lee  
Date: [Insert Date]

