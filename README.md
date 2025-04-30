# 🧠 LeetSync

Automatically sync your **LeetCode accepted submissions** to this GitHub repository using **GitHub Actions**.  
Supports multiple languages (e.g., C++, Python, Java, etc.) and organizes submissions by **difficulty** and **language**.

---

## 🚀 Features

- ✅ Auto-fetches all **accepted submissions**
- 🕒 Runs every **6 hours** using GitHub Actions
- 📁 Organizes files by `difficulty/language/ProblemName.ext`
- 🧼 Avoids duplicates using a `last_fetch.json` timestamp
- 🔐 Keeps your submissions private in forks (see below)

---

## 🛠 Setup Instructions

### 1. Fork this repository

> ⚠️ The `leetcode/` folder is excluded via `.gitignore` to protect your personal submissions.

---

### 2. Get your LeetCode session cookie

Even if you signed in with Google, follow these steps:

1. Go to [https://leetcode.com](https://leetcode.com) and log in.
2. Open Chrome DevTools (`F12` or `Ctrl+Shift+I`)
3. Go to the **Application** tab → Cookies → `https://leetcode.com`
4. Copy the value of the `LEETCODE_SESSION` cookie

---

### 3. Add a GitHub Secret

Go to your repository → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**:

- **Name**: `LEETCODE_SESSION`
- **Value**: Your cookie value from above

---

Alternatively, the script will generate it on first run if not found.

---

## 💻 Folder Structure
leetcode/
├── easy/
│   ├── cpp/
│   │   └── TwoSum.cpp
├── medium/
│   └── python/
│       └── AddTwoNumbers.py
...

Each problem is saved as a separate file, organized by difficulty and language.

---

## 📦 Excluded from Forks

This repo ignores personal data and files via `.gitignore`:

- `leetcode/` → All submissions (so forks are clean)
- `last_fetch.json` → Your last fetched timestamp

> This keeps your personal solutions private when someone forks the repo.

---

## 🤖 Workflow Trigger

The GitHub Action:

- ⏰ Runs automatically every **6 hours**
- 🖱 Can also be manually triggered from the **Actions** tab

---

## 🙋 FAQ

### 📌 What languages are supported?

Any language you submit in on LeetCode — C++, Python, Java, JavaScript, etc.

### 🔒 Will my solutions be exposed?

No. They're excluded from version control by default using `.gitignore`.

### 🧪 Can I test it manually?

Yes! Trigger the workflow manually from the **Actions** tab and watch the log.

---

## 🧼 Credits

This project uses a hybrid method:

- LeetCode’s internal **GraphQL API**
- Your **session cookie** for authentication
- GitHub Actions for automation

---

## 📥 Contributing

Pull requests are welcome! You can improve documentation, formatting, or functionality (like stats, charts, etc.).
