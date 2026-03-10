```markdown
# 🎯 AdSpy Gallery

Turn your Chrome bookmarks (or any product URLs) into a beautiful, visual gallery. Perfect for marketers, researchers, and anyone who collects winning ad product pages and wants to browse them like a shopping catalog.

[![PWA Ready](https://img.shields.io/badge/PWA-ready-blue.svg)](https://web.dev/progressive-web-apps/)
[![Made with DeepSeek](https://img.shields.io/badge/AI-DeepSeek%20via%20OpenRouter-green)](https://openrouter.ai/)

---

## ✨ Features

- **Password protected** – only you can access your gallery (password: `cakado-win`).
- **Import Chrome bookmarks** – pick an exported `bookmarks.html` file and select a folder.
- **Manual URL entry** – add product URLs one by one.
- **DeepSeek AI analysis** – each page is scanned to extract:
  - Product title
  - Main product image
  - Price (if available)
  - Short description
  - Category (fashion, beauty, tech, etc.)
  - Relevant emoji
- **Visual gallery** – products displayed as cards with image, title, price and category.
- **Filtering** – by category or “has price”.
- **Detailed bottom sheet** – tap any card to see full info and visit the original page.
- **Persistent database** – all products are stored locally in your browser (IndexedDB). They remain even after you close the app.
- **Add more bookmarks anytime** – new products are merged with existing ones.
- **PWA ready** – install on your home screen for a native‑like experience.

---

## 🚀 Getting Started

### Prerequisites

- A modern browser (Chrome, Safari, Edge, Firefox).
- An [OpenRouter](https://openrouter.ai/) API key (free tier available) – used to analyze product pages.

### Installation

1. Download the [`index.html`](https://github.com/yourusername/adspy-gallery/releases) file (or clone this repo).
2. Open the file in your browser. That’s it – no server required!

> **Note:** All data stays in your browser. No information is sent anywhere except to OpenRouter (with your key) and a public CORS proxy.

### Configuration (API Key)

To enable AI analysis, you need an OpenRouter API key:

1. Sign up / log in at [OpenRouter](https://openrouter.ai/).
2. Create a new API key (starts with `sk-or-...`).
3. In the app, click the **⚙️** icon in the top bar.
4. Paste your key and click **Save & Close**.

Your key is stored only in your browser’s local storage.

---

## 📖 Usage

### 1. Login
When you open the app, a login modal appears. Enter the password:  
**`cakado-win`**  
Click **Unlock**. Any previously saved products will load automatically.

### 2. Import Bookmarks from Chrome

#### Export bookmarks (desktop)
- Open Chrome, press `Ctrl+Shift+O` (Windows/Linux) or `Cmd+Shift+O` (Mac) to open the Bookmark Manager.
- Click the **⋮** menu (top‑right) and choose **Export bookmarks**.
- Save the `bookmarks_MM_DD_YY.html` file.
- Transfer this file to your phone (email, cloud, WhatsApp, etc.).

#### Import into AdSpy Gallery
- On the **Import** page, tap **Choose Bookmarks File**.
- Select the HTML file you transferred.
- The app will list all bookmark folders found.
- Tap the folder containing your product links.
- Click **Analyze Selected Folder**.

The analysis will begin – you’ll see a progress bar and logs. Once finished, your gallery appears.

### 3. Manual URL Entry
- In the **Import** page, enter a URL in the input field.
- Click **+** to add it to the list.
- Repeat for multiple URLs.
- Click **Analyze X URLs** to start analysis.

### 4. The Gallery
- Products are shown as cards with image, domain, title, and price (if found).
- Use the **filter chips** at the top to narrow down:
  - **All** – everything
  - **Has Price** – products with a price
  - **Fashion, Beauty, Tech, Home, Fitness, Other** – category filters
- The top bar shows the total product count.
- **➕ Add** returns to the import page to add more bookmarks.
- **🗑 Clear** deletes **all** products from the database (use with caution).

### 5. Product Details
Tap any card to open a **bottom sheet** with:
- Full-size product image (if available)
- Title
- Price tag (if available)
- Category and domain tags
- Description
- Full URL
- **Visit Product Page** button – opens the original link in a new tab.

Drag the sheet down or tap the overlay to close it.

---

## 💾 Database Persistence

All products are saved in your browser’s **IndexedDB**. This means:
- Your gallery persists across sessions.
- Adding new bookmarks merges with existing ones (duplicate URLs are updated).
- Clearing browser data will erase your gallery – be careful!

---

## 📲 Install as a PWA

You can add AdSpy Gallery to your home screen for an app‑like experience.

**Android (Chrome):**
- Open the app in Chrome.
- Tap the menu (three dots) and select **Add to Home screen**.

**iOS (Safari):**
- Open the app in Safari.
- Tap the **Share** button.
- Scroll down and tap **Add to Home Screen**.

Once installed, it launches in standalone mode (no browser UI). An install banner will also appear when the app detects it can be installed.

---

## ❓ Troubleshooting

| Issue | Solution |
|-------|----------|
| **Login fails** | Ensure you type `cakado-win` exactly (case‑sensitive). |
| **No folders after importing HTML** | The file may not contain `<h3>` folder tags. Export again from Chrome. |
| **Analysis stuck or errors** | Check your OpenRouter API key in settings. Some sites block the proxy – those URLs may fail. |
| **Images not loading** | The AI might not have found a suitable image. Visit the page manually via the bottom sheet. |
| **Gallery empty after login** | No bookmarks imported yet. Go to the import page and add some. |
| **Forgot password** | It's hardcoded in the HTML. If lost, you’ll need to edit the file. |

---

## 🔧 Technical Overview

- **Single HTML file** – no build step, no dependencies (except fonts and external APIs).
- **IndexedDB** for local storage.
- **CORS proxy** (`api.allorigins.win`) to fetch page HTML.
- **OpenRouter API** with DeepSeek model for AI extraction.
- **PWA manifest** and service worker (blob‑based) for offline support.
- **Responsive design** – works on phones and tablets.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).  
Feel free to modify and adapt for your own use.

## 🙏 Credits

- [OpenRouter](https://openrouter.ai/) for AI inference.
- [AllOrigins](https://allorigins.win/) for CORS proxy.
- [Clash Display](https://fonts.google.com/specimen/Clash+Display) & [Outfit](https://fonts.google.com/specimen/Outfit) fonts.

---

**Happy spying!** 🎯
```
