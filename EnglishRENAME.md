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
