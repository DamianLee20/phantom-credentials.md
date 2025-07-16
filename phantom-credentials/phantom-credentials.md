# Phantom Credentials – Initial Access & Pivoting Drill

## 🏢 Industry
Professional Services

## 🎯 Attacker Objective
Credential Theft

## 🎓 Exercise Objectives
1. Test and validate incident response and escalation procedures  
2. Enhance team coordination and communication  
3. Identify and address gaps in security policies and procedures

## 💻 Environment
**Operating Systems:** Windows, Linux  
**Architecture:** Hybrid Cloud  
**Application Stack:**
- SIEM (e.g., Splunk)
- VPN
- Email Platform (Microsoft 365 / Outlook Web Access)
- Web Apps (Internal tools/HR system)
- Active Directory
- Remote Management Tools

---

## 🧠 Scenario Overview
A malicious actor gains access to a user's VPN credentials through a phishing campaign. After successfully logging in, the attacker moves laterally, accesses sensitive systems, and attempts privilege escalation via Active Directory.

---

## 📅 Timeline & Phases

### Phase 1: Initial Access  
- **Inject:** Phishing email sent to finance team with a fake Microsoft login page  
- **Expected Action:** Identify the email, report it, block sender domain  
- **Artifacts:** Suspicious login to VPN from unusual geolocation

### Phase 2: Credential Abuse  
- **Inject:** Logs show successful login to VPN by compromised user  
- **Expected Action:** Detect login anomaly in SIEM, isolate user account  
- **Artifacts:** Splunk alert, brute-force pattern (multiple failed logins before success)

### Phase 3: Lateral Movement  
- **Inject:** Attacker accesses mapped drives, begins scanning network  
- **Expected Action:** Monitor traffic, detect unusual AD queries  
- **Artifacts:** Powershell history, SMB traffic, AD enumeration logs

### Phase 4: Escalation & Containment  
- **Inject:** Attempted privilege escalation logged on Domain Controller  
- **Expected Action:** Revoke access, isolate endpoint, initiate IR plan  
- **Artifacts:** Windows Event Logs (4624, 4672), EDR detection alert

---

## 🧑‍🤝‍🧑 Team Roles

| Role | Responsibility |
|------|----------------|
| SOC Analyst | Log analysis, detection, alert triage |
| Sysadmin | Account management, system isolation |
| Incident Commander | Lead coordination, escalation, communication |
| Communications | Internal updates, legal/compliance handling |
| IT Director | Final decisions, regulatory notification (if applicable) |

---

## 📊 Key Questions for Debrief

1. How quickly were initial alerts identified and acted upon?
2. Were escalation paths and responsibilities clear to all?
3. What tools were most useful during response?
4. Were any policy or visibility gaps exposed?
5. How could this be prevented in the future?

---

## ✅ Outcomes

- Validated detection capabilities  
- Strengthened cross-team communication  
- Identified areas for policy improvement  
- Documented for audit and compliance

---

## 📎 Notes

*This tabletop was designed using guidance from the MITRE ATT&CK framework (Initial Access: T1078, Lateral Movement: T1021, Credential Access: T1003).*

