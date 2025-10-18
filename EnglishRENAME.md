# Online QR Code Generator

> A lightweight online QR code generator built entirely on Cloudflare Workers, supporting instant generation of any text, URL, or Chinese content.

[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare-Workers-orange?logo=cloudflare)](https://workers.cloudflare.com/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)  
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/yourusername/qrcode-generator/pulls)

---

## Features

- **Lightning-fast deployment** – Deploy to Cloudflare Workers with global CDN acceleration  
- **Modern UI** – Responsive design, gradient backgrounds, smooth animations  
- **Multilingual support** – Perfectly supports Chinese, Japanese, Korean, and other Unicode characters  
- **Mobile-friendly** – Adaptable to mobile, tablet, and desktop screens  
- **No storage required** – All processing happens on the front-end, no user data is stored  
- **Zero dependencies** – All code is embedded, no external CDN or libraries needed  
- **Completely free** – Uses Cloudflare Workers’ free tier (100,000 requests per day)  

---

## Quick Start

### Deploy to Cloudflare Workers

1. Sign up and log in to the [Cloudflare Dashboard](https://dash.cloudflare.com/)  
2. Go to `Workers & Pages` > `Create Application` > `Create Worker`  
3. Delete the default code and paste the full `worker.js` code  
4. Click `Save and Deploy`  
5. Access the assigned URL to start using the QR code generator  

### Local Development

1. Copy the code  
2. Go to Cloudflare and create a Worker project  
3. Click "Start from Hello, World"  
4. Give your Worker project a name  
5. Click Next > Save & Deploy  
6. In the Worker main interface, click Edit code  
7. Delete the default code and paste `worker.js` content  
8. Save & Deploy  
9. Access the Worker via the default domain or bind a custom domain  
10. Use the website  

---

## Usage

1. Enter any text (URL, plain text, Chinese, emoji, etc.) in the input box  
2. Click the "Generate QR Code" button or press `Enter`  
3. The QR code will appear instantly below and can be right-clicked to save or screenshotted  

### Supported Content Types

- URL: `https://example.com`  
- Plain text: `Hello World`  
- Chinese text: `你好世界`  
- Phone number: `tel:+8613800138000`  
- Email address: `mailto:example@email.com`  
- WiFi configuration: `WIFI:S:NetworkName;T:WPA;P:password;;`  
- Any Unicode character  

---

## Tech Stack

- **Runtime:** Cloudflare Workers  
- **Frontend:** HTML5 + CSS3 + Vanilla JavaScript  
- **QR Code generation:** QRCode.js (embedded version)  
- **Styling:** Responsive design + CSS3 animations  

---

## Project Structure

qrcode-generator/
├── worker.js # Full Cloudflare Worker code
├── README.md # Project documentation
├── LICENSE # MIT License
└── .gitignore # Git ignore file

---

## Custom Configuration

### Change QR Code Size

In `worker.js`, modify the following code:

```javascript
new QRCode(qrcodeDiv, {
  text: text,
  width: 300,    // Change width
  height: 300,   // Change height
  colorDark: "#000000",
  colorLight: "#ffffff"
});
Contributing

Issues and Pull Requests are welcome!

1.Fork the repository

2.Create a feature branch: git checkout -b feature/AmazingFeature

3.Commit your changes: git commit -m 'Add some AmazingFeature'

4.Push to the branch: git push origin feature/AmazingFeature

5.Open a Pull Request

Roadmap

 1.Support custom QR code colors

 2.Add logo watermark feature

 3.Batch QR code generation

 4.Add QR code download functionality

 5.Support more QR code styles

 6.Add history feature (local storage)

 7.Dark mode support

FAQ

Q: What if QR code generation fails?
A: Please check if the input is too long; it is recommended not to exceed 2000 characters per generation.

Q: Does Cloudflare Workers have traffic limits?
A: The free plan allows 100,000 requests per day, sufficient for personal use.

Q: How to save the generated QR code?
A: Right-click the QR code and choose "Save image as," or use a screenshot tool.

License

This project is licensed under the MIT License.

Acknowledgements

QRCode.js
 – QR code generation library

Cloudflare Workers
 – Serverless platform

All contributors and users

Contact

For questions or suggestions, contact:

Submit an Issue

Start a Discussion

Email: shabishabia1976@gmail.com

<div align="center">

If this project helps you, please give it a ⭐ Star!

Made with ❤️ by Lipeiying032

</div> ```
