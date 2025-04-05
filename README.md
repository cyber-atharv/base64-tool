# 🔤 Base64 & Multi-Encoding Tool

> A fast, flexible CLI tool to encode, decode, detect, and peel multi-layered text obfuscation used in cybersecurity analysis.

[![Author](https://img.shields.io/badge/Made%20by-cyber--atharv-00ffcc?style=flat-square&logo=github)](https://github.com/cyber-atharv)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

---

## 📌 What is this tool?

In cybersecurity, attackers and web developers constantly encode data — whether in URLs, authorization tokens, or obfuscated malware payloads. 

This tool is a command-line utility built by **cyber-atharv** that allows you to easily encode, decode, and analyze multiple data formats including:
- **Base64** and **Base64URL** (safe for web URLs)
- **Base32**
- **Hexadecimal (Hex)**
- **URL Encoding (%XX)**

One of its coolest features is **automatic format detection** and **recursive payload peeling** (which strips off multiple nested layers of encoding until the raw data is revealed).

---

## ✨ Key Features

- **Multi-Format Support:** Convert between Plaintext, Base64, Base32, Hex, and URL encoding instantly.
- **Auto-Detection:** Analyzes raw strings, checks character sets & padding, and tells you what encoding is used.
- **Recursive Peeling (`peel`):** Have you ever encountered a string encoded 5 times like `Base64 -> Hex -> URL -> Base64`? The `peel` command automatically detects and unravels every single layer.
- **Encoding Chaining (`chain`):** Chain multiple encoding methods together to test how Web Application Firewalls (WAFs) or filters handle obfuscated payloads.
- **Pipeline Friendly:** Pipe text directly through standard terminal streams (`stdin`/`stdout`).

---

## 🚀 Quick Start & Installation

### 1. Install Dependencies
```bash
# Clone the repository
cd base64-tool

# Install in editable mode
pip install -e .
```

### 2. Basic Usage Examples

#### 🔹 Encode a message
```bash
b64tool encode "admin:password123"
# Output: YWRtaW46cGFzc3dvcmQxMjM=

# Encode to Hex format
b64tool encode -f hex "cyber-atharv"
# Output: 63796265722d617468617276
```

#### 🔹 Decode a message
```bash
b64tool decode "YWRtaW46cGFzc3dvcmQxMjM="
# Output: admin:password123
```

#### 🔹 Auto-detect encoding
```bash
b64tool detect "48656c6c6f20576f726c64"
# Output: Format: Hex (Confidence: 95%)
```

#### 🔹 Peel nested obfuscation (Unraveling multi-layer encoding)
```bash
# Decode a multi-layered payload automatically in one go:
b64tool peel "SlVkUFZEUXlTVEZrV1ZkMWRFbFVTa1pMVjBkM1lXNVVZV3hoY25ZPQ=="
```

---

## 🧠 Why I Built This

When analyzing web traffic, CTF challenges, or suspicious scripts, manual decoding step-by-step is tedious. I built this tool to have a clean, transparent, and scriptable encoder/decoder that handles complex encoding chains smoothly and helps beginners understand how data representations work.

---

## 📜 License & Author

- **Author:** [cyber-atharv](https://github.com/cyber-atharv)
- **License:** Open source under the MIT / AGPL License.
