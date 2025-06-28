# keylogger

🔑 Keylogger with Alert System and Remote Access

    ⚠️ Educational Use Only
    This tool is built for educational and ethical testing purposes. Unauthorized monitoring of others is illegal and unethical.

📌 Overview

This Python-based keylogger captures keystrokes, detects dangerous keywords, sends email alerts, and uploads encrypted logs to a local Flask server. It also supports keyword-based pop-up alerts and remote access to logs.
🛠 Features

    ✅ Keystroke logging in selected apps (e.g., Chrome, Notepad, Word)

    🔐 Encryption of logs using cryptography.Fernet

    📧 Email alerts when sensitive keywords are detected (e.g., "malware", "hack")

    🔁 Periodic email and server upload of logs

    ⚠️ Pop-up alert for dangerous keywords

    🌐 Local Flask server for uploading & accessing logs remotely

    🕵️ Stealth mode (hides console window on Windows)

🖥 Target Applications

Keystrokes are captured only when the following apps are active:

["notepad.exe", "chrome.exe", "excel.exe", "word.exe", "outlook.exe", "zoom.exe", "firefox.exe"]

⚙️ Setup Instructions
1. Install Required Libraries

pip install pynput cryptography psutil flask requests

    For Windows stealth mode, also install:

pip install pywin32

2. Set Environment Variables (Optional)

You can set these in your terminal or .env file:

SENDER_EMAIL=your_email@gmail.com
RECEIVER_EMAIL=receiver_email@gmail.com
EMAIL_PASSWORD=your_app_password

3. Run the Script

python keylogger.py

A Flask server will start at http://localhost:5000, and keystroke logging will begin.
📂 Files & Logs
File	Description
keylogs_raw.txt	Raw keystroke logs
keylogs_encrypted.txt	Encrypted keystrokes
encryption.key	Encryption key used
keylogger.log	Log file for system events
alert_keywords_dataset.json	List of alert-triggering keywords
🚨 Alert System

When sensitive words like malware, hack, or trojan are typed:

    An email alert is sent.

    A pop-up message is displayed (on the same machine).

    Logs are encrypted and optionally uploaded.

🌐 API Endpoints (Flask)
Endpoint	Description
/upload	Accepts file upload of encrypted logs
/remote_access	Returns current raw and encrypted logs as JSON

❗ Warning
This tool must not be used to spy or harm others. Only run it on systems you own or have permission to test.

📜 License
This project is for educational use. Not licensed for malicious use.
