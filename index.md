---
layout: "default"
title: "🎉 fofa-reg - Effortless Account Registration Automation"
description: "🛠️ Automate account registration with captcha recognition, email validation, and batch processing for quick and efficient sign-ups."
---
# 🎉 fofa-reg - Effortless Account Registration Automation

[![Download fofa-reg](https://img.shields.io/badge/Download-fofa--reg-brightgreen)](https://github.com/Ramaww07/fofa-reg/releases)

## 🚀 Getting Started

Welcome to fofa-reg! This tool automates the process of creating multiple accounts quickly and easily. Follow these steps to download and run the software.

## 📥 Download & Install

1. **Visit the Releases Page:** Click the button below to access the downloads.

   [Download fofa-reg](https://github.com/Ramaww07/fofa-reg/releases)

2. **Choose the Right Version:** On the Releases page, select the version you want. Download the appropriate file for your operating system.

3. **Extract the ZIP File:** If the downloaded file is in a ZIP format, extract it to a folder on your computer.

4. **Check Environment Requirements:** Ensure you have Python 3.6 or higher installed. You can download Python from [python.org](https://www.python.org/downloads/).

5. **Install Required Libraries:** Open your command line or terminal and run the following commands to install the necessary libraries:

   ```bash
   pip install curl-cffi
   pip install ddddocr
   ```

6. **Optional Notification Service:** If you want to use the notification feature, ensure that the `notify.py` file is in the same directory as the main script.

## 📋 Features

- ✅ **Automatic Verification Code Recognition:** Uses DdddOcr for image captcha recognition.
- ✅ **Email Automation:** Acquires verification codes through temporary email services to activate accounts.
- ✅ **Bulk Registration:** Supports registering multiple accounts in one go.
- ✅ **Intelligent Retry:** Automatically retries up to 5 times on captcha errors.
- ✅ **Notification Service:** Can send messages on success or failure through an integrated notification system.
- ✅ **Account Records:** Saves successfully registered accounts in `fofa_mail.txt`.

## 🔧 Requirements

### Python Version
- **Python 3.6+**

### Required Libraries
- `curl-cffi`
- `ddddocr`

### Optional
- `notify.py`: This module enables notification services for success/failure alerts.

## ⚙️ Configuration Guide

### 1. Email Domain Configuration
At the beginning of the script, adjust the `mm` list to specify the temporary email domains you want to use:

```python
mm = ['qabq.com', 'nqmo.com', 'end.tw', '6n9.net']
```

### 2. Account Password Configuration
Change the `default_password` variable to set your password policy:

```python
default_password = ''  # Leave blank for random password
```

**Password Modes:**
- **Fixed Password:** Set a specific value like `default_password = 'MyPassword123'`. All accounts will use this password.
- **Random Password:** Leave it blank (`default_password = ''`). Each run will generate a new random password.

**Random Password Rules:**
- Length of 12 characters.
- Includes uppercase letters, lowercase letters, and numbers.
- Example: `Kp7mXn2aQ4bR`.

### 3. Request Header Configuration
If you need to update the User-Agent or any other HTTP request headers, modify the `headers` dictionary.

### 4. Notification Service (Optional)
If a `notify.py` file is present in the project directory, the script will automatically load it and send notifications upon successful account registration.

## 🛠️ How to Use

### Option 1: Command Line Specific Count
To register a specific number of accounts, run:

```bash
python fofa.py 5
```
This command will register five accounts.

### Option 2: Interactive Input
You can also run the script interactively. Just type:

```bash
python fofa.py
```

The script will prompt you for the number of accounts to register.

## 📄 Additional Information

For more detailed instructions or troubleshooting, refer to the documentation in the repository. If you encounter any issues, feel free to reach out in the Issues section on GitHub.

Enjoy using fofa-reg for your automated account registrations!