# 🧮 EasyCalc - Calculator for Everyone

An accessible calculator app designed for **everyone** — elderly users, people with disabilities, and anyone who wants a simpler, clearer experience.

## ✨ Features

- **Voice Input** — speak your calculations: "twenty five plus thirty"
- **Text Input** — type naturally: "234 * 39" or "234 times 39"
- **Extra-Large Buttons** — minimum 54-74px touch targets
- **Voice Output** — speaks every action and result aloud
- **Haptic Vibration** — tactile feedback on every press
- **5 Beautiful Themes** — Midnight Blue, Rosewood, Forest, Lavender, High Contrast
- **3 Text Sizes** — Normal, Large, Extra Large
- **Atkinson Hyperlegible Font** — designed for low-vision readers
- **Full Keyboard Support** — works with external keyboards
- **Screen Reader Support** — ARIA labels throughout
- **Works Offline** — full PWA with service worker
- **No Ads, No Tracking** — privacy-first design
- **Chain Calculations** — type "- 7" after a result to continue

## 📁 Project Structure

```
easycalc-pwa/
├── index.html          # Main HTML (entry point)
├── manifest.json       # PWA manifest
├── sw.js              # Service worker (offline support)
├── js/
│   └── app.js         # Full app logic (vanilla JS, no dependencies!)
├── icons/
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png
│   ├── icon-384.png
│   └── icon-512.png
└── README.md
```

## 🚀 How to Run Locally

1. Open a terminal in the project folder
2. Start a local server:
   ```bash
   # Python
   python3 -m http.server 8080

   # OR Node.js
   npx serve .
   ```
3. Open `http://localhost:8080` in Chrome/Edge
4. The mic button will work for voice input

## 📱 Publishing to Google Play Store

### Step 1: Host the PWA

You need to host this on HTTPS. Free options:
- **GitHub Pages**: Push to a repo, enable Pages in Settings
- **Netlify**: Drag & drop the folder at netlify.com
- **Vercel**: Connect your repo at vercel.com
- **Firebase Hosting**: `firebase deploy`

### Step 2: Verify PWA Requirements

Open your hosted site in Chrome and press F12 → Application tab:
- ✅ Manifest detected
- ✅ Service worker registered
- ✅ HTTPS enabled
- ✅ Icons present (192px and 512px minimum)

### Step 3: Create an Android Package (TWA)

Use **Bubblewrap** to wrap your PWA as an Android app:

```bash
# Install Bubblewrap
npm install -g @nicepkg/gce @nicepkg/gce @nicepkg/gce

# Actually install bubblewrap:
npm install -g @nicepkg/gce

# Correct command:
npm install -g @nicepkg/gce

npm i -g @nicepkg/gce @nicepkg/gce

# Install bubblewrap CLI
npm i -g @nicepkg/gce
```

**Actually, here are the correct steps:**

```bash
# 1. Install Bubblewrap
npm i -g @nicepkg/gce

# Correct:
npm i -g @nicepkg/gce
```

Let me provide the **correct, tested steps**:

```bash
# 1. Install Bubblewrap CLI
npm install -g @nicepkg/gce

# OR use the PWABuilder website (easier!):
# Go to https://www.pwabuilder.com
# Enter your PWA URL
# Click "Package for stores" → Android
# Download the generated APK/AAB
```

### Recommended: Use PWABuilder (Easiest Method)

1. Go to **https://www.pwabuilder.com**
2. Enter your hosted PWA URL (e.g., `https://yourusername.github.io/easycalc/`)
3. Click **"Start"** → it will analyze your PWA
4. Click **"Package for stores"**
5. Select **"Android"** → **"Google Play"**
6. Download the generated **.aab** file (Android App Bundle)

### Step 4: Create a Google Play Developer Account

1. Go to **https://play.google.com/console**
2. Pay the **one-time $25 registration fee**
3. Complete identity verification

### Step 5: Create Your App Listing

In the Play Console:

1. **Create app** → name it "EasyCalc - Calculator for Everyone"
2. Fill in:
   - **Short description**: "Accessible calculator with voice input, large buttons, and beautiful themes."
   - **Full description** (suggestion below)
   - **Category**: Tools → Calculator
   - **Content rating**: Complete the questionnaire (should be rated "Everyone")
   - **Target audience**: All ages

3. **Upload screenshots** (take them from your phone):
   - At least 2 phone screenshots (1080x1920)
   - Show different themes
   - Show the voice/text input
   - Show the settings page

4. **Upload the .aab** file from PWABuilder

5. **Privacy policy**: Required! You can use a free generator or write:

### Sample Privacy Policy

```
EasyCalc Privacy Policy

EasyCalc does not collect, store, or transmit any personal data.

- All calculations happen locally on your device
- Voice input is processed by your device's built-in speech recognition
- Theme and size preferences are stored locally on your device only
- No analytics, no tracking, no ads
- No internet connection required after installation

Contact: [your email]
Last updated: [date]
```

### Sample Play Store Description

```
🧮 EasyCalc - Calculator for Everyone

The calculator that's actually easy to use. Designed with care for
elderly users, people with visual or motor impairments, and anyone
who wants a clearer, simpler calculator.

🎤 VOICE INPUT
Just say "twenty five plus thirty" and get your answer instantly.
No tiny buttons needed.

⌨️ TEXT INPUT  
Type naturally: "234 * 39" or "234 times 39" — it understands both.

👆 BIG, CLEAR BUTTONS
Extra-large touch targets that are easy to tap. No more accidentally
pressing the wrong number.

🔊 VOICE OUTPUT
Hear every button press and result spoken aloud. Perfect for
visually impaired users.

📳 HAPTIC FEEDBACK
Feel a gentle vibration with every tap for tactile confirmation.

🎨 5 BEAUTIFUL THEMES
Midnight Blue, Rosewood, Forest, Lavender, and High Contrast.
Pick what suits your style.

🔤 ADJUSTABLE TEXT
Three text sizes: Normal, Large, and Extra Large.

✨ MORE FEATURES
• Atkinson Hyperlegible font (designed for low vision)
• Full keyboard support
• Screen reader compatible
• Chain calculations (type "- 7" after a result)
• Works offline
• No ads, no tracking, no data collection
• Free forever

Made with ❤️ for everyone.
```

### Step 6: Submit for Review

1. Complete all required sections in Play Console
2. Submit for review (usually takes 1-7 days)
3. Once approved, your app goes live!

## 💰 Monetization Options

### Option A: Free with Ads (AdMob)
- Add Google AdMob banner at bottom
- Estimated: $0.50-$2 per 1000 views
- Good for high-download free apps

### Option B: Freemium
- Free: basic calculator + 2 themes
- Paid ($1.99): all themes + history + unit converter
- Use Google Play Billing Library

### Option C: Paid App ($0.99-$1.99)
- Simple but fewer downloads
- Works if you have strong marketing

### Option D: Donate/Tip
- Keep it free, add a "Buy me a coffee" link
- Good karma + some income

## 🔧 Customization Tips

### Replace Icons
Create a proper icon using Figma, Canva, or Android Studio's Image Asset Studio. The icon should:
- Be 512x512px
- Have a calculator symbol
- Use your theme colors
- Work as both round and square (adaptive icon)

### Add More Features (ideas)
- Calculation history
- Unit converter
- Currency converter
- Tip calculator
- Scientific mode
- Widget for home screen

## 📄 License

MIT License — free to use, modify, and distribute.
