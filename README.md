# Downloads Folder Safety Scanner

## 📌 Executive Summary
**The Problem:** The downloads folder is a primary entry point for malware. Manually inspecting file extensions and running individual antivirus scans on newly downloaded files is time-consuming and prone to human error, leaving systems vulnerable to disguised executables and malicious payloads.

**The Solution:** An automated Python security triage script designed for routine digital forensics. The tool scans a target directory, calculates cryptographic hashes for file integrity verification, detects potentially spoofed file extensions, and programmatically triggers Windows Defender.

**Business Impact:** Demonstrates the ability to bridge data engineering with cybersecurity. By automating routine security checks, this tool reduces the risk of initial compromise and streamlines incident response triage, principles critical to enterprise security operations.

---

## 🛠️ Tools & Technologies Used
* **Programming:** Python (`os`, `hashlib`, `subprocess`)
* **Security & Forensics:** Cryptographic Hashing (SHA-256), File Signature/Extension Validation
* **System Integration:** Windows Defender Command Line Interface (CLI)

---

## 🛡️ Key Features & Forensic Capabilities

1. **SHA-256 Hash Generation:** Automatically calculates the SHA-256 hash of downloaded files, allowing for easy cross-referencing against threat intelligence databases like VirusTotal.
2. **Risky Extension Detection:** Scans for and flags high-risk file types (e.g., `.exe`, `.bat`, `.scr`, `.vbs`) that often masquerade as harmless documents.
3. **Automated Malware Scanning:** Uses Python's `subprocess` module to integrate directly with Windows Defender (MpCmdRun.exe), forcing an immediate, targeted scan of the downloads directory without manual GUI navigation.

---

## 💻 How to Run This Project

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/HildaKiptoo/downloads-folder-safety-scanner.git](https://github.com/HildaKiptoo/downloads-folder-safety-scanner.git)
