# BOTNET
# Botnet Controller (Educational Project)

> ⚠️ **Disclaimer:** This project is intended **strictly for ethical hacking and cybersecurity education**. Use only in isolated lab environments or on systems you own or are authorized to test. Unauthorized use is illegal and unethical.

## 📌 Overview

This project demonstrates the foundations of post-exploitation techniques such as remote command execution, file transfers, keylogging, and botnet-style control over multiple clients. It aims to help students and security researchers understand real-world cyber threats from a defensive perspective.

## 📁 Components

### ✅ `server.py`
- Single-client reverse shell interface.
- Supports command execution, file transfer, keylogging, screenshot capture, and persistence.

### ✅ `keylogger.py`
- Lightweight Python keylogger.
- Stores logged keystrokes in a file within `%AppData%`.
- Used in combination with `server.py`.

### ✅ `commandandcontrol.py`
- Multi-client Command and Control (C2) botnet interface.
- Accepts multiple connections simultaneously using threading.
- Allows interactive shell sessions with any connected client.

---

## 💡 Features

| Feature             | `server.py` | `commandandcontrol.py` |
|---------------------|-------------|-------------------------|
| Remote Shell Access | ✅           | ✅ (multi-client)       |
| File Upload/Download| ✅           | ✅                      |
| Keylogger Control   | ✅           | ✅                      |
| Screenshot Capture  | ✅           | ✅                      |
| Session Switching   | ❌           | ✅                      |
| Kill Connections    | ❌           | ✅                      |
| Broadcast Commands  | ❌           | ✅ (`sendall`)          |
| Threaded Client Mgmt| ❌           | ✅                      |

---

## 🧪 Usage (In a Controlled Lab)

### 1. Start C2 Server
```bash
python commandandcontrol.py
