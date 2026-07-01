# QR Verify

**Know Before You Open**

A premium, privacy-first QR code scanner and **offline security analyzer**. QR Verify scans a QR code — from your camera or an uploaded image — decodes it instantly, and runs a transparent, on-device risk analysis before you ever tap a link, scan a payment, or join a network.

100% **HTML, CSS, and vanilla JavaScript**. No frameworks, no backend, no servers, no accounts, no cookies, no analytics, no tracking, and no data collection of any kind. Everything happens inside your browser.

---

## ✨ Features

- **Live camera scanner** — rear/front camera, auto scan, continuous scan, pause/resume, flash toggle (where supported)
- **Image upload** — drag-and-drop or browse, supports PNG / JPG / JPEG / WEBP
- **Smart content detection** — Website URL, UPI Payment, WhatsApp, Telegram, Instagram, Facebook, YouTube, Email, SMS, Phone, WiFi, Location, vCard, Calendar, Crypto wallet, Plain text, and more
- **Smart analysis panel** — type, detected app, purpose, protocol, domain/subdomain/TLD, short-URL detection, parameter count, character count, encoding
- **Brand detection** — flags whether a domain or UPI handle matches a recognized official brand
- **Offline risk engine** — heuristic scoring (0–100) checking HTTP vs HTTPS, IP-based URLs, disguised `@` links, excessive length, shortener domains, suspicious keywords, brand impersonation, and more
- **Human-language explanation** — a plain-English summary of what the QR does and why it's safe or risky
- **Security report UI** — circular risk gauge, verdict chip, console-style decoded readout, and a flag list
- **Utilities** — copy result, open link, download a PDF report, share, clear, scan again
- **Dark & light themes**, glassmorphism UI, responsive down to small phones
- **Accessible** — keyboard navigation, ARIA labels, visible focus states, reduced-motion support

## 🔒 Privacy

> No information leaves your device. Everything is processed locally. No scan history is stored.

- All QR decoding and risk analysis runs in your browser using JavaScript.
- The only network requests this app makes are the **one-time CDN downloads** of the [html5-qrcode](https://github.com/mebjas/html5-qrcode) and [jsPDF](https://github.com/parallax/jsPDF) libraries declared in `index.html`, plus the Google Fonts stylesheet. After the first load, your browser caches them and the app works fully offline.
- The only thing stored locally is your **light/dark theme preference**, saved in `localStorage` on your own device. It is never transmitted anywhere. No scan content, history, or personal data is ever stored or sent.

## 📁 Project structure

```
qr-verify/
├── index.html      # App markup & structure
├── style.css        # Design system, theming, layout, animation
├── script.js        # Scanner logic, QR parser, risk engine, UI rendering
├── icons/            # Favicon & brand mark (SVG)
├── assets/           # Reserved for future static assets
└── README.md
```

## 🚀 Run it locally

No build step, no dependencies to install. Just open `index.html` in a modern browser.

> Camera access requires a **secure context** (HTTPS) or `localhost`. If you open the file directly via `file://`, the camera scanner will not be available in most browsers — use the image upload feature instead, or serve the folder locally:
>
> ```bash
> npx serve .
> # or
> python3 -m http.server 8080
> ```

## 🌐 Deploy to GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Source**, select your branch (e.g. `main`) and root folder (`/`).
4. Save. Your app will be live at `https://<username>.github.io/<repo>/` within a minute or two — fully working camera scanner included, since GitHub Pages is served over HTTPS.

## ⚠️ Disclaimer

QR Verify's risk engine uses transparent, offline **heuristics** — pattern checks for things like protocol, domain shape, known shortener services, and scam-associated keywords. It is a helpful second opinion, not a guarantee. It cannot detect every threat, and a "Low Risk" result does not mean a link, payment, or contact is automatically safe. Always use your own judgment, especially before making a payment or entering personal information.

---

### Credits

Created by **Imtiyaz Surjapuri**

- Follow on X — [@Imtiyazkth](https://x.com/Imtiyazkth)
- Follow on Facebook — Imtiyaz Surjapuri
- Follow on Instagram — Imtiyaz Surjapuri

Built with [html5-qrcode](https://github.com/mebjas/html5-qrcode) and [jsPDF](https://github.com/parallax/jsPDF) (MIT licensed open-source libraries, loaded client-side only).
