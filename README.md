# SayCheese (Updated & Fixed)

This is an updated version of the original **SayCheese** tool by **thelinuxchoice**. Since the original repository became outdated and the author's account is no longer active, this version has been patched to work with modern tunneling services and includes improved templates.

![cheese](https://user-images.githubusercontent.com/34893261/56869077-e5714d80-69d1-11e9-8ce2-29a254021890.jpg)

## What's New in this Version?
- **Fixed Link Generation:** Patched the regex logic to support the new Serveo domain (`serveousercontent.com`) and modern Ngrok domains (`ngrok-free.app`).
- **Zoom Template:** Replaced the legacy template with a professional "Zoom - Waiting for Host" interface to increase the success rate of permission requests.
- **Improved Detection:** Added fallback logic to ensure links are captured even if tunneling services change their output format.

## How it works?
The tool generates a secure HTTPS page using **Serveo** or **Ngrok**. It utilizes the `MediaDevices.getUserMedia` API to request camera access. 

To encourage the user to grant permission, the page mimics a legitimate Zoom meeting waiting room. Once the user clicks "Join" and allows access, the tool captures frames at regular intervals and sends them back to your server.

[Read more about MediaDevices.getUserMedia()](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)

## Installation

### Kali Linux / Ubuntu / Termux:
```bash
# Clone your updated repository
git clone https://github.com/AndiXplorer/saycheese.git
cd saycheese
bash saycheese.sh
```

## Dependencies
- `php`
- `ssh`
- `wget`
- `unzip`

## Credits
- **Original Author:** thelinuxchoice
- **Template & Fixes:** Updated for 2026 compatibility.

---
**Disclaimer:** This tool is for educational purposes only. Unauthorized use of this tool for accessing cameras without consent is illegal and unethical.
