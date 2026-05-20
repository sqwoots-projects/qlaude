# Claude — Private Chat App

Your personal Claude AI workspace. Runs entirely in the browser, calls the Anthropic API directly.

## Features
- 💬 Full chat with streaming responses
- 🔍 Web search toggle (uses Anthropic's built-in search tool)
- 📎 File uploads — PDFs, images, text files
- 🧠 Persistent memory — auto-summarised after each conversation, editable
- 📚 Conversation history saved in the browser
- 🔒 PIN protection + encrypted API key storage
- 🤖 Model selector — Haiku / Sonnet / Opus
- 📱 Installs to home screen on iOS and Android (PWA)

---

## GitHub Pages Setup (takes ~5 minutes)

### Step 1 — Create a GitHub account
Go to [github.com](https://github.com) and sign up if you don't have one.

### Step 2 — Create a new repository
1. Click the **+** icon top-right → **New repository**
2. Name it anything, e.g. `my-claude`
3. Set it to **Private** (recommended)
4. Click **Create repository**

### Step 3 — Upload the files
1. In your new repository, click **Add file** → **Upload files**
2. Upload all three files:
   - `index.html`
   - `manifest.json`
   - `icon.svg`
3. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to **Settings** (tab at the top of your repo)
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Set Branch to **main**, folder to **/ (root)**
5. Click **Save**

### Step 5 — Get your URL
After about 60 seconds, your app will be live at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```
GitHub will show you the exact URL in the Pages settings.

Share this URL with your partner. Bookmark it.

---

## First-time setup in the app

1. **Choose a PIN** — 4 digits, you'll enter this every time you open the app
2. **Enter your Anthropic API key** — get it from [console.anthropic.com](https://console.anthropic.com)
3. **Enter your name** — so Claude addresses you correctly
4. **Choose a default model** — Sonnet 4 is recommended for most use

### ⚠️ Set a spend cap
Before using the app, go to [console.anthropic.com](https://console.anthropic.com) → **Billing** → **Usage limits** and set a monthly spend cap (e.g. $20). This protects you if the API key is ever exposed.

---

## Installing to your home screen

### iPhone / iPad (Safari)
1. Open the app URL in Safari
2. Tap the **Share** button (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

### Android (Chrome)
1. Open the app URL in Chrome
2. Tap the **⋮** menu → **Add to Home screen**
3. Tap **Add**

---

## How memory works

After each conversation, the app automatically calls Claude (using the cheap Haiku model) to extract key facts and update your memory. This memory is silently injected into every new conversation so Claude always knows your context — name, job situation, preferences, ongoing projects, etc.

You can view and edit memory anytime: open the sidebar → **Memory** tab.

---

## Security notes

- Your API key is encrypted in the browser using your PIN as the key
- The key is never sent anywhere except directly to Anthropic's API
- Anyone with your URL and PIN could access the app — keep both private
- Your conversation history is stored only in the browser on that device
- To use on multiple devices, you'll need to set up the PIN and API key on each one

---

## Updating the app

If the app is updated, just re-upload `index.html` to your GitHub repo. Your conversations and memory are stored in the browser and won't be affected.
