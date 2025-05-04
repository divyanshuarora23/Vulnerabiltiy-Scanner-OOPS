# Web Vulnerability Scanner – JScanSec Project

This module is part of the collective Java-based security tool “JScanSec”, built by a team of three members. The Web Vulnerability Scanner is responsible for scanning a target website for basic web security issues, such as exposed sensitive files, risky HTTP headers, and unsafe HTTP methods. This module is meant to be lightweight, beginner-friendly, and ready to integrate into a larger security analysis tool.

## 📌 Module Overview

- Language: Java
- Dependencies: None (standard Java SE libraries only)
- Purpose: Quickly check a website (including localhost) for common security misconfigurations.

## 🔍 Features

The module performs the following checks:

1. Exposed Files & Directories:
   - Looks for common sensitive files like .env, config.php, wp-config.php, admin/, backup/, etc.
   - Detects and explains whether these are publicly accessible.

2. HTTP Headers Check:
   - Detects information leakage from headers like Server and X-Powered-By.
   - Identifies open CORS policies (Access-Control-Allow-Origin: *).

3. HTTP Methods Enumeration:
   - Sends an HTTP OPTIONS request to detect allowed HTTP methods (GET, POST, PUT, DELETE, etc.).
   - Flags dangerous methods like PUT, DELETE, TRACE, CONNECT.

4. Friendly Output:
   - Displays alerts in an easy-to-read format with icons and explanations.
   - Helps non-cybersecurity users understand why a finding might be risky.

## ▶️ How to Run

1. Compile the Java file:

```bash
javac WebVulnerabilityScanner.java
