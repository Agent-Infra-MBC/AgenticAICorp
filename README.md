# Agentic AI Corporate Framework

This project contains a fully AI-staffed corporate structure. Each department is an autonomous AI agent. Follow these steps to set up and run the project.

## 📦 Project Structure

```
agentic-ai-corp/
├── agents/
│   ├── ceo.js
│   ├── legal.js
│   ├── finance.js
│   ├── devops.js
│   ├── marketing.js
│   ├── hr.js
│   ├── sales.js
│   ├── rnd.js
│   ├── analyst.js
│   └── scraper.js
├── lib/
│   └── db.js
├── api/
│   └── server.js
├── ui/
│   └── index.html
├── .gitignore
├── .env.example
├── package.json
├── vercel.json
└── README.md
```

## 🧑‍💻 Requirements

1. **Node.js** (version 14 or above)
2. **MongoDB Atlas** account (or any MongoDB connection URI)
3. **Vercel** account for deployment
4. A computer with internet access

## 🚀 Setup Instructions

1. **Install Node.js**

   - Go to https://nodejs.org
   - Download the **LTS** version for your operating system
   - Follow the installer instructions

2. **Unzip the Project**

   - Locate the downloaded `agentic-ai-corp.zip` file
   - Right-click and choose **Extract All...** (Windows) or **Open With > Archive Utility** (Mac)
   - This creates a folder named `agentic-ai-corp`

3. **Install Dependencies**

   - Open a terminal (Command Prompt, PowerShell, or Terminal)
   - Navigate to the project folder:
     ```bash
     cd path/to/agentic-ai-corp
     ```
   - Install Node.js packages:
     ```bash
     npm install
     ```

4. **Configure Environment Variables**

   - In the project folder, copy the example file:
     ```bash
     cp .env.example .env
     ```
   - Open `.env` in a text editor (Notepad, VSCode, etc.)
   - Replace `<username>`, `<password>`, and other placeholders with your MongoDB connection string.
   - Save the file.

5. **Run Locally**

   - In the terminal:
     ```bash
     npm run dev
     ```
   - You should see:
     ```
     Connected to MongoDB
     Server listening on port 3000
     ```
   - Open a web browser and go to `http://localhost:3000`
   - You’ll see a message: **Agentic AI Running**

6. **Deploy to Vercel**

   - Log in to your Vercel account (https://vercel.com)
   - Click **New Project** → **Import Git Repository**
   - Select your GitHub repository (push this folder to GitHub first)
   - In Vercel project settings, set environment variable `MONGODB_URI` (same as in `.env`)
   - Click **Deploy**
   - After deployment, Vercel provides a URL. Open it to see **Agentic AI Running**

## 📁 File Details

### `lib/db.js`
- Connects to MongoDB using Mongoose.
- Reads `MONGODB_URI` from `.env`.

### `api/server.js`
- Sets up an Express server.
- Imports each AI agent (currently placeholders).
- Connects to MongoDB and starts listening on port 3000.

### `agents/*.js`
- Each file exports a class stub for the AI agent.
- Example: `agents/ceo.js` defines class `Helix`, with a `start()` method that logs to console.

### `ui/index.html`
- A simple webpage to show that the project is running.

## ✏️ Next Steps

- **Fill in Agent Logic**: Each file in `agents/` is a starting point. Add your AI logic here.
- **Enhance Dashboard**: Replace `ui/index.html` with a React or Next.js dashboard.
- **Advanced Crawling**: Build out `agents/scraper.js` to gather real-time data.

---

**That’s it!** You now have a basic, fully AI-staffed corporate framework that you can expand. If you need help, just re-open this guide and follow each step carefully.
