
# Secure V1 Framework 🔒

<p align="center"> <img src="https://github.com/chamidu200/HORIZON-FRAMEWORK-V1/blob/8bc33c98558c74133f9088c03c341a2aee17d77a/Capture.PNG" alt="chamidu200" /> </p>

<p align="center"> <img src="https://github.com/chamidu200/HORIZON-FRAMEWORK-V1/blob/8bc33c98558c74133f9088c03c341a2aee17d77a/cap2.PNG" alt="chamidu200" /> </p>

![Secure V1 Framework Banner](https://img.shields.io/badge/Secure%20V1%20Framework-v1.0-blueviolet?style=for-the-badge)

Welcome to the **Secure V1 Framework**! A powerful Python-based tool for penetration testing and security research. This framework allows you to manage remote sessions, reverse TCP handlers, HoaxShell engines, and file smuggling capabilities.

---

## 📑 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
  - [Cloning the Repository](#cloning-the-repository)
  - [Installing Dependencies](#installing-dependencies)
- [Usage](#usage)
  - [Running the Script](#running-the-script)
  - [Configuring LHOST](#configuring-lhost)
- [Payloads](#payloads)
- [Notes](#notes)
- [Author](#author)
- [License](#license)

---

## 🔍 Overview

The **Secure V1 Framework** is a versatile toolset for managing remote sessions, generating payloads, and smuggling files over HTTP. Built with Python 3, it’s optimized for security professionals.

### Features:

- **Team Server**: Manage multiple sibling servers with secure or insecure connections.
- **HoaxShell Engine**: HTTP/HTTPS-based shell for remote command execution.
- **Reverse TCP Handler**: Multi-session TCP listener for backdoor management.
- **File Smuggler**: Transfer files easily via HTTP.
- **Interactive CLI**: Tab auto-completion, customizable prompt.
- **Payload Generator**: Generate custom payloads for various platforms.
- **Session Management**: Manage sessions, monitor active connections.

---

## 🛠️ Installation

### Cloning the Repository

Clone the repository from GitHub:

```bash
git clone https://github.com/chamidu200/HORIZON-FRAMEWORK-V1.git
cd HORIZON-FRAMEWORK-V1
```

> **Note**: Replace the URL with your actual GitHub repository URL if needed.

### Installing Dependencies

Install the required Python packages:

```bash
pip install requests
```

**Note**: `requests` is a third-party library essential for HTTP operations. Other dependencies (like `os`, `sys`, `threading`) are part of Python's standard library.

---

## 🚀 Usage

### Running the Script

To start the framework, execute:

```bash
python3 Secure-Framework.py
```

This will launch the team server, HoaxShell, reverse TCP handler, and file smuggler with default settings.

### Configuring LHOST 🖥️

When using commands like `conptyshell`, you must specify an `LHOST` value (your machine’s IP address). **Do not use `eth0`**, instead use your **actual IP**.

You can dynamically retrieve your local IP address using this Python code:

```python
import socket

# Get local IP address dynamically
def get_lhost():
    s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
    s.connect(("8.8.8.8", 80))  # Connect to a public DNS to get local IP
    ip_address = s.getsockname()[0]
    s.close()
    return ip_address

lhost = get_lhost()
print(f"Your LHOST IP address is: {lhost}")
```

To manually find your IP address:
- **Linux**: `ip addr show` or `ifconfig`
- **Windows**: `ipconfig`
- **macOS**: `ifconfig`

Example:
```bash
conptyshell 192.168.1.1 4444 session_123
```

---

## 💻 Payloads

You can use **payload generators** for creating custom payloads for different platforms. The framework supports multiple payload types, including reverse TCP shells, bind shells, and others.

Example for reverse TCP payload:
```bash
python3 payload_generator.py reverse_tcp 192.168.1.1 4444
```

This will generate a reverse TCP payload for your specific IP and port.

---

## 📝 Notes

- **LHOST Configuration**: Always use your actual IP (e.g., `192.168.1.1`) instead of `eth0`.
- **Ethical Use**: This tool is for educational purposes and authorized security testing only. Unauthorized use is prohibited.

---

## 👤 Author

**SECURE_HORIZON**  
GitHub: [https://github.com/chamidu200](https://github.com/chamidu200)  
YouTube: [https://www.youtube.com/@chamidunimsara20052](https://www.youtube.com/@chamidunimsara20052)  
Contact: Reach out via GitHub Issues or YouTube comments!

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🚀 Instructions for Using This README

1. Save this content as `README.md` in your project’s root directory.
2. Update the GitHub URL (`https://github.com/chamidu200/Secure-V1-Framework`) to your actual repository.
3. If you have a specific YouTube video link, replace the YouTube URL with your own.
4. Push the file to your GitHub repository:

```bash
git add README.md
git commit -m "Add README.md"
git push origin main
```

---

This `README.md` is visually structured, including emojis and clear steps for installing, using, and configuring the framework. If you need any adjustments or have further requests, feel free to ask!

---

### Sinhala Translation for Local Use (සිංහල පරිවර්තනය):

---

## 🔍 දර්ශනය

**Secure V1 Framework** යනු, පරිගණක ආරක්ෂණ පර්යේෂකයන් සහ පැනට්‍රේෂන් පරීක්ෂකයන් සඳහා ගොඩනැගීමකි. Python භාෂාව භාවිතා කර ඇති මෙය ඔබට ප්‍රතිචාර TCP පද්ධතිය, HoaxShell යන්ත්‍රය සහ ගොනු පරිවර්තනයේ හැකියාවන් සපයයි.

---

## 🛠️ ස්ථාපනය

### ගිට්හුබ් ගොනුවට යන්න

```bash
git https://github.com/chamidu200/HORIZON-FRAMEWORK-V1.git
cd HORIZON-FRAMEWORK-V1
```

### අවශ්‍ය පොදු පොදු මෘදුකාංග

```bash
pip install requests
```

---

## 🚀 භාවිතය

### ස්ක්‍රිප්ට් එක ධාවනය කිරීම

```bash
python3 Secure-Framework.py
```

### LHOST සකස් කිරීම 🖥️

```python
import socket

# Dynamic IP Address ලබා ගැනීම
def get_lhost():
    s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
    s.connect(("8.8.8.8", 80))
    ip_address = s.getsockname()[0]
    s.close()
    return ip_address

lhost = get_lhost()
print(f"Your LHOST IP address is: {lhost}")
```

---

## 📝 සටහන්

- **LHOST සකස් කිරීම**: `eth0` භාවිතා නොකර සැබෑ IP එක භාවිතා කරන්න.

---

Hope this helps! Let me know if you need further tweaks. 😊
