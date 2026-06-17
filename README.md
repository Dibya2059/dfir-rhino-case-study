# 🕵️ DFIR Case Study – Rhino Image Investigation

## 📌 Overview
This project is a Digital Forensics and Incident Response (DFIR) investigation of a simulated case involving illegal distribution and hidden embedding of rhino images.

The investigation analyzed network traffic (TCP/HTTP), USB forensic images, and JPEG file structures to identify hidden or embedded image data.

Multiple forensic tools were used to reconstruct evidence and detect concealed data within image files.

---

## 🛠️ Tools Used
- Wireshark (TCP/HTTP Traffic Analysis)
- Autopsy (Disk Forensics)
- PhotoRec (File Recovery)
- Stegdetect (Steganography Detection)
- JPseek (JPEG Structure Analysis & File Carving)
- Binwalk (Embedded File Analysis)

---

## 🌐 Network Traffic Analysis (Wireshark)
- Analyzed packet capture using Wireshark
- Focused on TCP stream reconstruction and HTTP communication
- Identified file transfer activity over network traffic
- Extracted image-related data from TCP/HTTP streams

---

## 💾 USB Forensics (RHINOUSB.dd)
- Analyzed USB disk image using forensic tools
- Recovered deleted and existing image files
- Extracted multiple rhino-related artifacts
- Correlated USB evidence with network traffic activity

---

## 🔍 Steganography Analysis (Stegdetect)
- Ran Stegdetect on recovered JPEG images
- Most images returned negative results for steganography
- No confirmed hidden payloads detected by automated analysis tools

---

## 🧪 JPseek Analysis (Key Finding)
- Performed structural JPEG analysis using JPseek
- Detected embedded image data within a crocodile image file
- Successfully extracted a hidden rhino image from within the crocodile image

### 🧠 Interpretation
The crocodile image acted as a carrier file containing embedded image data. While Stegdetect failed to identify steganographic patterns, JPseek revealed hidden image structures through deep file analysis and carving techniques.

---

## 📊 Key Findings
- File transfer activity observed over TCP/HTTP streams
- Multiple rhino images recovered from network and USB evidence
- JPEG file anomalies detected in some images
- Crocodile image contained embedded rhino image data
- No traditional steganography confirmed, but embedded content was recovered through structural analysis

---

## 🔗 Evidence Correlation
A direct relationship was established between:
- USB forensic image data (RHINOUSB.dd)
- Network traffic (TCP/HTTP streams)
- Embedded image data extracted from JPEG files

This confirms multi-source data movement and concealed image embedding across different storage mediums.

---

## 🧠 Conclusion
The investigation successfully reconstructed a complex data concealment scenario involving network traffic, USB storage, and embedded image structures.

Although steganography detection tools did not confirm hidden payloads, JPseek analysis revealed embedded rhino image data within a crocodile image, proving that file carving and structural analysis are essential in DFIR investigations.

---

## 👨‍💻 Author
Cybersecurity Student – SOC / DFIR Analyst Path
