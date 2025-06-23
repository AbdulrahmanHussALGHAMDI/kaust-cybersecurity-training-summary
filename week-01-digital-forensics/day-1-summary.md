# 📘 Day 1 – Table of Contents
- 🔹 Introduction  
- ⚖️ Laws and Regulations  
- ✅ Rules of Evidence  
- 📌 When Does Digital Forensics Matter?  
- 👨‍💼 Why Organizations Hire Forensic Experts  
- 🧪 Mock Digital Forensics Drill  
- 🧰 Virtual Lab Setup  
- 🧷 Pre-Investigation Considerations  
- 💾 Data Acquisition  
- 🧱 Forensic Imaging  
- 🔒 Write Blocking  
- 🔗 Chain of Custody  
- 🧪 Tool Validation  

---
---

## 🔹 Introduction

In the digital realm, the “objects” are:
- 👤 People  
- 💻 Devices  
- 🌐 Networks  
- 📂 Data

Every action — even a brief one — pushes bits into memory or storage.  
This reflects **Locard’s Principle**:

> “Every contact between two objects leaves a trace.”  
> — *Dr. Edmond Locard, father of modern forensic science*

---

### 🧪 Real-World Scenario

**Case**: An employee copies `DesignSpec.pdf` to a personal USB at 10:15 a.m., deletes it, and removes the drive.

🔍 **Traces left behind**:
- `$MFT` (Master File Table)
- Jump List
- `USBSTOR\\...\SerialNumber` key
- Shellbags
- `$UsnJrnl` (Update Sequence Number Journal)

---

### 🛡️ When Incidents Happen

When a security incident occurs, the **CSIRT** (Computer Security Incident Response Team) must:
- Analyze digital evidence
- Use forensic tools and methods properly

✅ To ensure evidence is **admissible in court**, examiners must:
- Follow legal procedures
- Know digital forensics best practices

---

### 📚 What Is Digital Forensics?

> Digital forensics is the disciplined process of:
- Identifying
- Acquiring
- Preserving
- Examining
- Analyzing
- Reporting  
digital evidence.

🎯 Purpose: To **reconstruct incidents** and present findings that are:
- **Technically sound**
- **Legally defensible**
