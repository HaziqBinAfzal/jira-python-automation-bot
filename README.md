 🚀 Jira Python Automation Bot

A Python-based automation project that integrates with **Atlassian Jira REST API** to automate issue creation, management, and workflow tasks.

---

# 🧠 What this project does

* Connects Python to Jira API
* Authenticates using API token
* Fetches Jira projects
* Creates issues automatically
* Can be extended for full automation workflows

---

# 🛠 Tech Stack

* Python
* Jira REST API
* Requests library
* Ubuntu (Linux environment)

---

# ⚙️ STEP-BY-STEP SETUP (UBUNTU MATE)

---

## 🟢 Step 1: Create project folder

```bash
mkdir jira-automation-bot
cd jira-automation-bot
```

---

## 🟡 Step 2: Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 🔵 Step 3: Install dependencies

```bash
pip install requests python-dotenv
```

---

## 🟣 Step 4: Save dependencies

```bash
pip freeze > requirements.txt
```

---

## 🟠 Step 5: Create files

```bash
touch main.py .env
```

---

## 🔐 Step 6: Setup `.env`

```bash
nano .env
```

```env
JIRA_EMAIL=your-email@example.com
JIRA_API_TOKEN=your-api-token
JIRA_URL=https://your-domain.atlassian.net
JIRA_PROJECT_KEY=HR
```

---

## 🧪 Step 7: Test connection (GET projects)

```python
import os
import requests
from requests.auth import HTTPBasicAuth
from dotenv import load_dotenv

load_dotenv()

EMAIL = os.getenv("JIRA_EMAIL")
TOKEN = os.getenv("JIRA_API_TOKEN")
URL = os.getenv("JIRA_URL")

auth = HTTPBasicAuth(EMAIL, TOKEN)

r = requests.get(f"{URL}/rest/api/3/project", auth=auth)

print(r.status_code)
print(r.text)
```

---

## 🚀 Step 8: Run script

```bash
python3 main.py
```

Expected:

```
Status Code: 200
```

---

## 🔥 Step 9: Create Jira Issue (FINAL SCRIPT)

```python
import os
import requests
from requests.auth import HTTPBasicAuth
from dotenv import load_dotenv
import json

load_dotenv()

EMAIL = os.getenv("JIRA_EMAIL")
TOKEN = os.getenv("JIRA_API_TOKEN")
URL = os.getenv("JIRA_URL")
PROJECT_KEY = os.getenv("JIRA_PROJECT_KEY")

auth = HTTPBasicAuth(EMAIL, TOKEN)

headers = {
    "Accept": "application/json",
    "Content-Type": "application/json"
}

issue_data = {
    "fields": {
        "project": {
            "key": PROJECT_KEY
        },
        "summary": "🔥 Automated issue from Python bot",
        "issuetype": {
            "name": "Task"
        }
    }
}

response = requests.post(
    f"{URL}/rest/api/3/issue",
    headers=headers,
    auth=auth,
    data=json.dumps(issue_data)
)

print(response.status_code)
print(response.text)
```

---

# 🎯 Expected Output

```json
Status Code: 201
{"key": "HR-1"}
```

---

# 📤 GitHub Commands

```bash
git init
git add .
git commit -m "Initial commit - Jira automation bot"
git branch -M main
git remote add origin YOUR_REPO_URL
git push -u origin main
```

---

# 📁 Final Project Structure

```
jira-automation-bot/
│
├── main.py
├── requirements.txt
├── README.md
├── .env (DO NOT PUSH)
└── venv/
```

---

# 🚫 Important Rules

* Never upload `.env`
* Never expose API token
* Always use correct Jira project key (example: `HR`)

---

# 📚 What you learned

* REST API integration
* Authentication handling
* Automation using Python
* Working with Jira projects
* Linux development environment setup

---

# Done by

*Ruveeha Ashfaq and Haziq Afzal

---

# 💼 Outcome

You built a real-world automation system using Python and Jira API — the kind of backend integration used in real companies.

