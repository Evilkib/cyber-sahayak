# 🛡️ Cyber Sahayak — साइबर फ्रॉड AI हेल्पर

> Free AI assistant for cyber fraud victims in India. Get help with account freeze, lien removal, bank complaints, and cybercrime.gov.in filing.

![License](https://img.shields.io/badge/license-MIT-blue)
![Next.js](https://img.shields.io/badge/Next.js-14-black)
![Deployment](https://img.shields.io/badge/deploy-Vercel-000)

---

## ✨ Features

- 🤖 **AI-powered guidance** in Hindi, Hinglish & English
- 🔒 **Account Freeze & Lien Removal** — MHA SOP 2026 compliant
- 📝 **Auto-generate** bank letters, emails & FIR drafts
- 📸 **Screenshot/Document analysis** — upload bank notices
- 📞 **1930 Helpline** integration & cybercrime.gov.in links
- ⚖️ **Legal rights education** — IT Act, IPC, RBI guidelines
- ⭐ **Anonymous review** system with viral share
- 🌙 **Mobile-first** responsive design
- 🚀 **Demo mode** — works without API key (shows guidance)

---

## 🚀 Quick Deploy (Vercel — 3 minutes)

### Step 1: Fork & Clone
```bash
# Fork on GitHub, then:
git clone https://github.com/YOUR_USERNAME/cyber-sahayak.git
cd cyber-sahayak
npm install
```

### Step 2: Configure API Key
```bash
# Copy example file
cp .env.local.example .env.local

# Edit .env.local and add your key:
# XAI_API_KEY=xai_your_key_here   ← Grok (recommended)
# OR
# OPENAI_API_KEY=sk-your_key_here ← OpenAI fallback
```

### Step 3: Test Locally
```bash
npm run dev
# Open http://localhost:3000
```

### Step 4: Deploy to Vercel
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Add env variable on Vercel dashboard:
# Settings → Environment Variables → Add XAI_API_KEY
```

**Or deploy with one click:**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/cyber-sahayak)

---

## 🔑 API Keys

| Provider | Get Key | Model Used |
|----------|---------|------------|
| **xAI (Grok)** ← recommended | [console.x.ai](https://console.x.ai/) | grok-2-1212 |
| OpenAI (fallback) | [platform.openai.com](https://platform.openai.com/api-keys) | gpt-4o-mini |

> **No key?** App runs in Demo Mode with pre-written guidance. Still useful!

---

## 📁 Project Structure

```
cyber-sahayak/
├── app/
│   ├── globals.css          # Custom styles + Tailwind
│   ├── layout.tsx           # Root layout + SEO metadata
│   ├── page.tsx             # Main chat interface
│   └── api/chat/route.ts   # AI API backend (Edge Runtime)
├── lib/
│   └── prompt.ts           # System prompt + quick prompts
├── public/
│   └── manifest.json       # PWA manifest
├── .env.local.example      # Environment template
├── .gitignore
├── next.config.js
├── package.json
├── tailwind.config.js
└── tsconfig.json
```

---

## 🛠️ Customization

### Change AI Model
Edit `app/api/chat/route.ts`:
```typescript
model = xai('grok-2-1212');     // Default
model = xai('grok-beta');       // Latest Grok
model = openai('gpt-4o');       // OpenAI GPT-4o
```

### Update System Prompt
Edit `lib/prompt.ts` — the `CYBER_SAHAYAK_PROMPT` constant controls all AI behavior.

### Add Quick Prompts
Edit `QUICK_PROMPTS` array in `lib/prompt.ts`.

### Styling
- Colors: `tailwind.config.js` → `theme.extend.colors`
- Custom CSS: `app/globals.css`

---

## 📋 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `XAI_API_KEY` | Optional* | xAI/Grok API key |
| `OPENAI_API_KEY` | Optional* | OpenAI API key |

*At least one is needed for full AI functionality. Without either, app runs in Demo Mode.

---

## ⚖️ Legal Disclaimer

This app provides **general information only** and does not constitute legal advice. Users should:
- Call **1930** for immediate cyber fraud assistance
- Visit **cybercrime.gov.in** to file official complaints
- Consult a qualified lawyer for legal advice

The AI responses are based on publicly available MHA SOPs, RBI guidelines, and legal information as of March 2026.

---

## 🤝 Contributing

Pull requests welcome! Please:
1. Fork the repo
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit changes: `git commit -m 'Add my feature'`
4. Push: `git push origin feature/my-feature`
5. Open a PR

---

## 📄 License

MIT License — free to use, modify, and deploy.

---

**Made with 💙 for India's cyber fraud victims**

> Emergency: 📞 **1930** | File Complaint: 🌐 **cybercrime.gov.in**
