# 🕵️ DFIR Rhino Case Study – Digital Forensics Investigation

## 📌 Overview
This project is a Digital Forensics and Incident Response (DFIR) case study involving multi-source evidence analysis, including network traffic logs, USB forensic images, encrypted archives, and steganographic image analysis.

The objective was to recover hidden rhino images, analyze data exfiltration techniques, and correlate evidence across multiple sources.

---

## 🛠️ Tools Used
- Wireshark (Network Traffic Analysis)
- Autopsy (Disk Forensics)
- fcrackzip (Archive Password Cracking)
- Stegdetect (Steganography Detection)
- Stegbreak (Brute-force Steganography Analysis)
- JPseek (JPEG Structure & Hidden Data Extraction)
- File extraction via TCP stream reconstruction

---

## 📁 Evidence Sources
- rhino.log
- rhino2.log
- rhino3.log
- RHINOUSB.dd
- contraband.zip (recovered from network traffic)

---

## 🌐 Network Forensics (Wireshark Analysis)
- TCP traffic was analyzed to identify file transfer activity
- Stream 69 contained exposed credentials (username and password)
- Files were reconstructed from TCP streams using export object features

### Recovered Files:
- rhino1.jpg
- rhino2.jpg
- rhino3.jpg
- contraband.zip

---

## 📦 Encrypted Archive Analysis
The file `contraband.zip` was extracted from network traffic and cracked using `fcrackzip`.

### Result:
- One additional image file was successfully recovered

This confirmed the presence of encrypted hidden evidence within the dataset.

---

## 💾 USB Forensics (Autopsy Analysis)
The USB disk image (RHINOUSB.dd) was analyzed using Autopsy.

### Findings:
- Total images recovered: 9+
  - 5 rhino images
  - 4 crocodile images
- 1 text file containing investigative narrative and system information

---

## 🔍 Steganography Analysis

### Stegdetect Analysis:
Bulk analysis was performed using:
