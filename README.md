# 🎭 Social Engineering & Phishing Payloads

<a href="https://attack.mitre.org/techniques/T1566/">
  <img src="https://img.shields.io/badge/Red_Team-Social_Engineering-red?style=for-the-badge" alt="Red Team" />
</a>

## 📌 Executive Summary
This repository contains a curated collection of simulated phishing emails, credential harvesting landing pages, and pretexting scenarios. These payloads are designed to test an organization's human defenses (Security Awareness) and to bypass email filtering gateways.

## 📂 Payloads Included

### 1. `it-password-reset.md`
A highly realistic "Urgent IT Password Reset" email. This template leverages authority and urgency—two classic psychological triggers—to convince employees to click a malicious link.

### 2. `office365-login.html`
A clean, realistic HTML landing page that mimics a standard Microsoft Office 365 login portal. In a real engagement, the form action would redirect to a listener (like Gophish or Evilginx) to capture credentials and session tokens.

## 🎯 How Red Teams Use These
1. **Email Spoofing:** Using SMTP servers configured with weak SPF/DKIM to send the email.
2. **Evasion:** Encoding the links using URL shorteners or compromised legitimate domains to bypass Secure Email Gateways (SEGs).
3. **Harvesting:** Directing the user to the `office365-login.html` page to capture their username and password.

## 🛡️ Defensive Evasion & Mitigation
- **Human Defense:** Train employees to verify the sender's actual email address, hover over links before clicking, and report suspicious emails to IT.
- **Technical Defense:** Enforce MFA (Multi-Factor Authentication). Even if a password is harvested, MFA stops the attacker from logging in.

## ⚠️ Disclaimer
These templates are for authorized Red Team engagements and educational purposes only. Using them to target individuals or organizations without explicit written permission is illegal.
