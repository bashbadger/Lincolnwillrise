LawFinder

A prototype Node.js web app that lets you **search U.S. state and federal laws and their limitations**, using mock data for states and live data from the **GovInfo API** for federal statutes.

---

## 🚀 Features

- Browse sample **state laws** (California, New York, Texas)
- Retrieve **live federal law data** (U.S. Code Title 18) via GovInfo API
- Simple, responsive front-end built with HTML/CSS/JS
- Modular Express.js backend with routes for future expansion
- Ready to deploy to **Vercel**, **Netlify**, or any Node-compatible host

---

## 🧩 Project Structure

```
lawfinder/
│
├── server.js              # Express server entry
├── package.json           # Dependencies & scripts
├── .env                   # API keys (optional)
│
├── /routes/api.js         # REST API routes (state + federal)
├── /data/laws.json        # Mock data for states
│
└── /public/               # Front-end files
    ├── index.html
    ├── app.js
    └── styles.css
```

---

## ⚙️ Installation

```bash
# 1. Unzip and enter directory
unzip lawfinder.zip
cd lawfinder

# 2. Install dependencies
npm install

# 3. (Optional) Add your GovInfo API key
echo "GOVINFO_KEY=your_api_key_here" > .env

# 4. Start the server
npm start
```

Then open **http://localhost:3000**

---

## 🧠 How It Works

- The app serves static pages from `/public`
- `/api/laws/:state` returns state law data from `/data/laws.json`
- `/api/federal/:title` fetches data from the **GovInfo API**
  - Example: `/api/federal/18` fetches a live sample of the U.S. Code (Title 18)

---

## 🌐 Deployment

### **Vercel**
1. Import project from GitHub.
2. Set `Root Directory` to `/`.
3. Add environment variable `GOVINFO_KEY` (optional).
4. Deploy — your Express app will run as a serverless function.

### **Netlify**
Netlify can host the front-end only.
To host the backend too, use a service like **Render**, **Fly.io**, or **Railway**.

---

## 🔮 Next Steps / Future Expansion

| Feature | Description |
|----------|--------------|
| **Full API Integration** | Add automatic updates from all 50 state legislative APIs. |
| **Database Layer** | Store laws in PostgreSQL or MongoDB for faster queries. |
| **Full-Text Search** | Add ElasticSearch or Meilisearch for advanced filtering. |
| **AI Summaries** | Summarize each law’s key points and exceptions. |
| **Version Tracking** | Track amendments and repeals over time. |

---

## 🧑‍💻 Author Notes

Built as a starting framework for a **comprehensive legal data portal**.
You can expand it into a real-time, automatically updated, searchable law platform.

---

### 📄 License
MIT License — free to modify and distribute.

