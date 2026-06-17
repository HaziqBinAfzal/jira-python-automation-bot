# 🚀 Jira Python Automation Bot

A Python-based automation project that integrates with Jira REST API to create and manage tasks automatically.

---

## 🔥 Features

* Create Jira issues using Python
* Bulk task generation
* Automated project management
* REST API integration with Jira

---

## 🛠 Tech Stack

* Python
* Jira REST API
* Requests library
* python-dotenv

---

# ⚙️ Setup & Installation (FULL COMMANDS)

## 1. Create project folder

```bash
mkdir jira-python-automation-bot
cd jira-python-automation-bot
```

---

## 2. Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Install dependencies

```bash
pip install requests python-dotenv
```

---

## 4. Save dependencies

```bash
pip freeze > requirements.txt
```

---

## 5. Create files

```bash
touch main.py .env README.md
```

---

## 6. Edit .env file

```bash
nano .env
```

Example:

```env
JIRA_EMAIL=your-email@example.com
JIRA_API_TOKEN=your-api-token
JIRA_URL=https://your-domain.atlassian.net
```

---

## 7. Run the project

```bash
python3 main.py
```

---

# 🚀 Example Output

```
Status Code: 201
{"key": "HR-1"}
```

---

# 📌 What this project does

This project connects Python to Atlassian Jira and automates issue creation using REST API.

---

# 🧠 Key Learnings

* REST API integration
* Authentication using API tokens
* Automation workflows
* Real-world project structuring

---

# 👥 Author

Built as a learning project for API automation and backend development practice.

---

