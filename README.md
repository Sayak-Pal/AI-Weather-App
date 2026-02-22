# 🌦️ AI Weather & Chat App
A simple, responsive **weather dashboard + AI chatbot** that answers questions using **live weather context**.

<p align="center">
  <a href="https://github.com/Sayak-Pal/AI-Weather-App">
    <img alt="GitHub Repo" src="https://img.shields.io/badge/GitHub-Repo-181717?logo=github&logoColor=white">
  </a>
  <img alt="HTML" src="https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white">
  <img alt="CSS" src="https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-ES6-F7DF1E?logo=javascript&logoColor=black">
  <img alt="OpenWeather" src="https://img.shields.io/badge/API-OpenWeather-FF6B00">
  <img alt="Gemini" src="https://img.shields.io/badge/AI-Google%20Gemini-4285F4?logo=google&logoColor=white">
  <img alt="Status" src="https://img.shields.io/badge/Status-Prototype-f59e0b">
</p>

---

## ✨ Features
- 🌍 **Live Weather Data**: up-to-date weather for any location  
- 🔎 **Search by City**: type any city and press Enter  
- 📍 **Current Location**: get weather using geolocation (browser permission required)  
- 🎨 **Animated Background**: smooth day→night gradient transitions  
- 💬 **Context-Aware AI Chat**: ask questions and get answers using the **current weather card** as context  
- 📱 **Fully Responsive**: works great on mobile + desktop  

---

## 🧠 How the AI Chat Works
The chatbot sends the **currently displayed weather** (city + conditions) as context to **Google Gemini**, then generates an answer tailored to what you’re seeing on screen.

Example questions:
- “Do I need an umbrella today?”
- “Is this weather good for a run?”
- “What should I wear in these conditions?”

---

## 🚀 Setup & Installation
You only need a modern browser — but the app requires **two API keys**.

### ✅ Required API Keys
1. **OpenWeatherMap API Key** (weather)
   - https://openweathermap.org/
2. **Google Gemini API Key** (AI chat)
   - https://aistudio.google.com/

---

## 🔑 Add Your Keys (Important)
This repository uses **`index.html`** as the main entry file.

1. Open `index.html` in a text editor  
2. Find the `<script>` section near the bottom where the API keys are declared  
3. Paste your keys:

```js
// Get your OpenWeatherMap key from https://openweathermap.org/
const OPENWEATHER_API_KEY = "PASTE_YOUR_OPENWEATHERMAP_KEY_HERE";

// Get your Gemini API key from https://aistudio.google.com/
const GEMINI_API_KEY = "PASTE_YOUR_GEMINI_API_KEY_HERE";
```

---

## ▶️ Run the App

### Option A: Open directly
Just open `index.html` in your browser.

### Option B: Run a local server (recommended)
Some browsers restrict certain features when running from `file://`.

```bash
python -m http.server 5173
```

Open: `http://localhost:5173`

---

## 🗂️ Project Structure
```text
.
├── index.html       # Main app (UI + logic)
├── README.md
└── key              # (Make sure this does NOT contain real secrets in public repos)
```

---

## 🧭 How to Use
- 🔎 **Search**: type a city name → press **Enter**
- 📍 **Use My Location**: click the location icon (bottom-right)
- 💬 **Chat with AI**: click the chat icon (bottom-left)
  - AI answers are based on the weather shown on the card

---

## 🧯 Troubleshooting

### “Invalid API key” / 401 errors
- Confirm your **OpenWeather** key is active (new keys may take a few minutes).
- Confirm your **Gemini** key is valid and not restricted.

### Geolocation not working
- Allow location permissions in the browser.
- Geolocation usually works best on `http://localhost` or `https://` (not always on `file://`).

### CORS / fetch errors
- Use the local server method (`python -m http.server`) instead of opening the file directly.

---

## 🔐 Security Note
Never commit real API keys to a public repo. Consider:
- using a backend proxy to keep keys private, or
- environment variables + a build step (if you migrate to a framework later).

---
