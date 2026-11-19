# Lab-4
# Vulnerability Analysis (Lab 4) — Active Activity

## Student Information
* **Name:** Ainsya Batrisya Binti Abdullah[cite: 9]
* **Student ID:** 52215125921[cite: 9]
* **Target:** `https://vulnbank.org`[cite: 9]

---

## 1. Target Setup (Victims)
* **Target Application:** VulnBank (`https://vulnbank.org`)[cite: 9]
* **Target Scope:** Web application layer running on ports `80` (HTTP) and `443` (HTTPS)[cite: 9]
* **Environment Description:** An authorized online banking simulation web application used for web reconnaissance, asset discovery, and security assessment[cite: 9].

---

## 2. Own Hosts (Attacker)
* **Attacker:** Kali Linux[cite: 10]
* **Virtualization Platform:** UTM[cite: 10]
* **Network Mode:** Shared Network with verified outbound internet and target reachability (`ping -c 3 vulnbank.org` resolved to `104.21.5.243` with 0% packet loss)[cite: 9, 10]
* **Toolchain Used:**
  * **Network & Port Scanning:** `Nmap`[cite: 10]
  * **Directory Enumeration:** `Gobuster`[cite: 10]
  * **Browser & Session Analysis:** Firefox Developer Tools[cite: 10]

---

## 3. Reconnaissance & Enumeration

### 3.1 Port & Service Scanning
```bash
nmap -sV -p 80,443 vulnbank.org
