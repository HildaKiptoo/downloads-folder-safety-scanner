# Downloads Folder Safety Scanner

## 📝 Overview
The **Downloads Folder Safety Scanner** is a lightweight Python script designed for Windows users to triage and analyze files in their Downloads directory. This tool acts as a first line of defense by identifying potentially dangerous file types and common disguise techniques used by malware, such as "double extensions" (e.g., `invoice.pdf.exe`).

By automatically generating a SHA-256 hash for flagged files, users can easily verify their safety against dozens of antivirus engines using VirusTotal. Finally, it seamlessly integrates with Windows Defender to initiate a localized, deep scan of the target folder.

**Disclaimer:** This script is a triage helper, not an antivirus engine. It flags suspicious file extensions and naming patterns, but does not analyze file contents. Always use a dedicated antivirus solution (like the integrated Defender scan) for true malware detection.

## 🛠️ Key Features
* **Risky Extension Detection:** Flags over 25 commonly abused file extensions, including `.exe`, `.scr`, `.bat`, `.vbs`, and `.ps1`.
* **Double Extension Spoofing:** Detects disguise tactics where a dangerous extension is hidden behind a safe-looking one (e.g., `.pdf.exe`, `.jpg.vbs`).
* **SHA-256 Hashing:** Automatically computes the cryptographic hash of flagged files, ready to be pasted into [VirusTotal](https://www.virustotal.com).
* **Metadata Extraction:** Displays the precise file size and last modified date for quick review.
* **Windows Defender Integration:** Optionally triggers a custom `MpCmdRun.exe` Windows Defender scan specifically targeting the analyzed folder.

## 🚀 How to Use

### Prerequisites
* Python 3.8 or higher.
* A Windows operating system (for Defender integration).

### Running the Scanner
1. Download or clone this repository.
2. Open your command prompt or terminal.
3. Run the script using Python:

**To scan your default user Downloads folder:**
```bash
python scan_downloads.py