# 🚀 Jira Python Automation Bot

A Python-based automation project that integrates with **Atlassian Jira REST API** to automatically create and manage issues (tasks).

This project demonstrates real-world backend/API automation using Python.

---

# 📌 Features

* Create Jira issues automatically using Python
* Bulk issue generation (automation loop)
* REST API integration with Jira
* Secure authentication using API token
* Git + GitHub workflow ready project

---

# 🛠 Tech Stack

* Python
* Jira REST API
* Requests library
* Python-dotenv (optional)
* Git & GitHub

---

# ⚙️ FULL PROJECT SETUP (STEP BY STEP WITH COMMANDS)

---

## 🚀 Step 1: Create project folder

```bash
mkdir jira-python-automation-bot
cd jira-python-automation-bot
```

---

## 🐍 Step 2: Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 📦 Step 3: Install dependencies

```bash
pip install requests python-dotenv
```

---

## 📄 Step 4: Save dependencies

```bash
pip freeze > requirements.txt
```

---

## 📁 Step 5: Create project files

```bash
touch main.py .env README.md .gitignore
```

---

## 🔐 Step 6: Setup environment variables

```bash
nano .env
```

Add:

```env
JIRA_EMAIL=your-email@example.com
JIRA_API_TOKEN=your-api-token
JIRA_URL=https://your-domain.atlassian.net
```

---

## 🧠 Step 7: Run your Python script

```bash
python3 main.py
```

---

# 🔍 DEBUGGING / TESTING COMMANDS USED

## Check logged-in user (API test)

```bash
python3 main.py
```

OR:

```bash
curl -u email:token https://your-domain.atlassian.net/rest/api/3/myself
```

---

## List all Jira projects (VERY IMPORTANT STEP)

```bash
python3 list_projects.py
```

OR API endpoint:

```
GET /rest/api/3/project/search
```

---

# 🚀 RUN PROJECT

```bash
python3 main.py
```

Expected output:

```text
Status Code: 201
{"key":"HR-1"}
```

---

# 📤 GIT & GITHUB SETUP

---

## Step 1: Initialize repo

```bash
git init
```

---

## Step 2: Add files

```bash
git add .
```

---

## Step 3: Commit project

```bash
git commit -m "Initial commit - Jira automation bot"
```

---

## Step 4: Set main branch

```bash
git branch -M main
```

---

## Step 5: Connect GitHub repo

```bash
git remote add origin https://github.com/your-username/your-repo-name.git
```

---

## Step 6: Push to GitHub

```bash
git push -u origin main
```

---

# 🧹 CLEAN PROJECT STRUCTURE

```
jira-python-automation-bot/
│
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
└── .env (NOT PUSHED TO GITHUB)
```

---

# 🔥 WHAT THIS PROJECT DOES

This script connects Python with Jira API and:

* Authenticates user
* Sends POST request
* Creates tasks inside a project
* Automates issue creation

---

# 🧠 WHAT WE LEARNED

* REST API integration
* Authentication using API tokens
* Working with JSON payloads
* Automation using Python
* Git & GitHub workflow
* Jira project structure

---

# 🚫 IMPORTANT NOTES

* Never upload `.env` to GitHub
* Never expose API tokens publicly
* Always use virtual environment
* Always verify Jira project key before API calls

---

# 👤 AUTHOR

Built as a learning project for API automation using Python and Jira.

---

# 💥 RESULT

You successfully built a real automation system that interacts with Jira like a backend engineer.

