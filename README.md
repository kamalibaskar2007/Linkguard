# 🛡️ LinkGuard – Smart Phishing URL Detector
> **Tagline:** Think Before You Click. Stay Safe Online.

LinkGuard is a cybersecurity web application built with **React.js + Tailwind CSS + Lucide Icons** that empowers internet users to analyze suspicious links and protect themselves against phishing attacks, brand impersonation, deceptive subdomains, and malicious traps **100% locally in the browser with zero server data leakage**.

---

## 🚀 Key Highlights & Features

1. **⚡ Heuristic URL Scanner**:
   - 9-Vector client-side heuristic inspection engine.
   - Calculates a risk score from **0 to 100** with risk classification (*Safe*, *Suspicious*, *High Risk Phishing*).
   - Animated SVG circular gauge with glowing color tiers.

2. **✨ Domain Highlighting & Structural Deconstruction**:
   - Isolates Protocol, Subdomains, the **TRUE Registrable Domain**, Path, and Query parameters.
   - Visually reveals deceptive subdomains (e.g. `accounts.google.com.attacker.com` vs real `google.com`).

3. **🎮 Interactive Phishing Simulator (Quiz)**:
   - Gamified cybersecurity quiz to test user instincts on real-world phishing vectors.
   - Live score tracker, streak multiplier, instant feedback, and bilingual explanations.

4. **🌐 Bilingual Support (English & தமிழ்)**:
   - Complete Tamil & English interface toggle.
   - Built-in **Tamil Cybersecurity Assistant** explaining threats and safety tips in clear, natural Tamil.

5. **📜 Local Scan History**:
   - Persisted in browser `localStorage`.
   - Export scan history to JSON or inspect past scans with one click.

6. **📚 Cybersecurity Awareness Hub**:
   - What is phishing, red flag checklists, common scams (banking, crypto airdrops, fake stores), and 4 golden rules of URL safety.

7. **🌙 Dark & Light Mode Support**:
   - Modern cybersecurity dashboard theme with cyber grid, neon accents, and responsive layout for mobile & desktop.

---

## 🛠️ How to Run Locally

### Prerequisites
- Node.js (v18+) & npm

### Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build
```bash
npm run build
npm run preview
```

---

## 🔬 Detection Techniques Implemented

1. **HTTPS & Protocol Verification**: Detects insecure plain HTTP connections.
2. **IP Hostname Detection**: Flags raw IPv4/IPv6 hosts commonly used by phishing infrastructure.
3. **Brand Impersonation & Typosquatting**: Detects lookalikes (*paypa1*, *g00gle*, *arnazon*, *micros0ft*) via regex patterns & Levenshtein distance.
4. **Deceptive Subdomain Spoofing**: Identifies when a trusted brand name is planted in the subdomain while the true destination domain belongs to an attacker.
5. **High-Risk Phishing Keywords**: Scans for social engineering lures (*verify-account*, *urgent-login*, *claim-prize*, *password-reset*, etc.).
6. **URL Shortener Concealment**: Warns when links use shorteners (*bit.ly*, *tinyurl.com*, *t.co*, etc.) to conceal destinations.
7. **Obfuscation & Structural Anomalies**: Flags deceptive `@` tricks, punycode (`xn--`), excessive dots (>3), and excessive hyphens in domains.
8. **High-Abuse Top-Level Domains (TLDs)**: Flags disposable TLDs (*.xyz*, *.top*, *.tk*, *.buzz*, *.work*).
9. **URL Length & Parameter Bloat**: Identifies bloated URLs designed to push the true domain off mobile screens.

---

## 👨‍💻 Developer & Author
- **Developer:** Kamali Baskar
- **GitHub:** [https://github.com/kamalibaskar2007](https://github.com/kamalibaskar2007)

---

## 🏆 Built for Cybersecurity Innovation Hackathons
- **Problem Statement:** Everyday internet users struggle to spot subtle URL tricks like deceptive subdomains and typosquatting.
- **Proposed Solution:** LinkGuard provides an explainable, privacy-first, client-side link analyzer with Tamil & English guidance.
- **Unique Selling Point (USP):** Zero data leaks (runs 100% in browser), domain anatomical highlighting, and bilingual accessibility.
