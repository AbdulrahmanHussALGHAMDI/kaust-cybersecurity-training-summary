# 🕵️‍♂️ Timeline Analysis – Digital Forensics Summary (Slides 59–74)

---

### 🔎 Understanding the Analysis Process

The digital forensic analysis process requires converting raw evidence into actionable insights. This is achieved through:

- Identifying relevant digital artefacts  
- Extracting timestamped data  
- Creating a coherent timeline to understand event sequences

---

### 🕒 What is Timeline Analysis?

**Timeline analysis** is the process of transforming numerous time-stamped artefacts into a **single, ordered chronology**.

These artefacts include:

- File MAC times (Modified, Accessed, Created)
- Logs
- Browser history
- Registry updates
- Emails, chats
- Cloud events

### ✅ Process Steps:
1. Collect time sources  
2. Normalize timestamps  
3. Merge and sort  
4. Tag and filter  
5. Interpret  

---

### 🧰 Tools for Timeline Analysis

### Common Tools:
| Tool              | Purpose                                  |
|-------------------|-------------------------------------------|
| Plaso / log2timeline | Creates a super timeline from multiple sources |
| Timesketch        | Visualizes timelines in a GUI interface  |
| Magnet AXIOM      | Commercial forensics suite               |
| EnCase Timeline   | Timeline generation via EnCase suite     |
| X-Ways Timeline   | Timeline from forensic image             |

---

## 📝 Slide 62 – Case Scenario: Leaked Spreadsheet

A confidential file `m57plan.xls` was leaked.

### Key Details:
- File: `m57plan.xls`  
- MD5: `e23a4eb7f2562f53e88c9dca8b26a153`  
- Modified: `2008-JUL-20 01:28:03 GMT`  
- Found on: Jean’s desktop (CFO)  
- Claimed emailed to Allison (President)

---

## 📁 Slide 63 – Artefacts of Interest

Two digital artefacts are of primary interest in this case:

- **Prefetch files**: Show program execution  
- **.lnk (Link) files**: Reveal file access history, even after deletion

---

## 📂 Slides 64–66 – Visual Timeline Elements

These slides visually emphasize that:

- **File access patterns** can reveal user behavior  
- **Sequence of actions** (open, modify, transfer) can be reconstructed from logs and artefacts  
- Correlation of artefacts provides stronger evidence  

---

## 🧠 Slide 67 – What is Plaso?

**Plaso** (Plaso Langar Að Safna Öllu) is the backend for the `log2timeline` tool.

- It collects timestamps from multiple sources  
- Generates a **super timeline** stored in a `.plaso` file

---

## ⚙️ Slide 68 – Tools Included in Plaso

| Tool        | Purpose                                          |
|-------------|--------------------------------------------------|
| `image_export` | Extract files from images or drives            |
| `log2timeline` | Main parser to create .plaso timeline database |
| `pinfo`        | View .plaso file metadata                      |
| `psort`        | Sort/filter/tag data within .plaso files       |
| `psteal`       | One-step timeline creation + sorting           |

---

## 📤 Slide 69 – image_export

`image_export` extracts file content from:

- Disk images  
- Media devices  
- Forensic captures  

✅ **Parameters available** to fine-tune export (e.g., file types, path filters)

---

## ⏳ Slide 70 – log2timeline

A command-line tool to **extract event data** and create `.plaso` timeline.

### Usage:
```bash
log2timeline -f filter_windows.txt export/jeanfilter.plaso image/jean.001

