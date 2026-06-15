# n8n Gmail Auto Labeler 📧🤖


![n8n](https://img.shields.io/badge/n8n-Workflow-orange?style=for-the-badge\&logo=n8n)
![Docker](https://img.shields.io/badge/Docker-Container-blue?style=for-the-badge\&logo=docker)
![Gemini](https://img.shields.io/badge/Google-Gemini-green?style=for-the-badge\&logo=google)
![Gmail](https://img.shields.io/badge/Gmail-API-red?style=for-the-badge\&logo=gmail)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

![GitHub stars](https://img.shields.io/github/stars/Riaz1407/n8n-gmail-auto-labeler?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/Riaz1407/n8n-gmail-auto-labeler?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/Riaz1407/n8n-gmail-auto-labeler?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/Riaz1407/n8n-gmail-auto-labeler?style=for-the-badge)

---

## 📌 Project Overview

An AI-powered Gmail automation workflow built with **n8n** that automatically classifies incoming emails and applies Gmail labels using **Google Gemini AI**.

The workflow continuously monitors Gmail inbox, analyzes incoming emails using Gemini AI, and automatically organizes them into predefined categories.

---

## 🚀 Features

✅ Automatically listens for new Gmail messages

✅ Uses **Google Gemini AI** to classify emails

✅ Automatically applies Gmail labels

✅ Categories supported:

* 🎓 College
* 💼 Internship
* 📂 Others

✅ Runs locally using Docker

✅ Persistent storage using Docker Volumes

✅ Automatic restart after PC reboot

✅ Background execution

---

## 🛠️ Tech Stack

| Technology        | Purpose                 |
| ----------------- | ----------------------- |
| n8n               | Workflow Automation     |
| Docker            | Containerization        |
| Google Gemini API | AI Email Classification |
| Gmail API         | Gmail Integration       |
| GitHub            | Version Control         |

---

## 📌 Workflow Architecture

```text
Gmail Trigger
      ↓
Text Classifier (Gemini AI)
      ↓
 ┌───────────┬────────────┬─────────┐
 │           │            │
College   Internship    Others
 │           │            │
Add Label  Add Label   Add Label
```

---

## 📸 Screenshots

### Workflow Canvas

Add screenshot here:

```text
screenshots/workflow.png
```

---

### Docker Running

Add screenshot here:

```text
screenshots/docker-running.png
```

---

### Successful Execution

Add screenshot here:

```text
screenshots/execution.png
```

---

### Gmail Labels

Add screenshot here:

```text
screenshots/gmail-labels.png
```

---

## 📁 Repository Structure

```text
n8n-gmail-auto-labeler
│
├── workflows
│   └── mail_auto_label.json
│
├── screenshots
│   ├── workflow.png
│   ├── docker-running.png
│   ├── execution.png
│   └── gmail-labels.png
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/Riaz1407/n8n-gmail-auto-labeler.git

cd n8n-gmail-auto-labeler
```

---

### 2. Install Docker Desktop

Verify installation:

```bash
docker --version
```

---

### 3. Create Docker Volume

```bash
docker volume create n8n_data
```

---

### 4. Run n8n Using Docker

```bash
docker run -d --restart unless-stopped --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

---

### 5. Open n8n

```text
http://localhost:5678
```

Create your n8n account.

---

### 6. Import Workflow

* Open n8n
* Click **Import from File**
* Select:

```text
workflows/mail_auto_label.json
```

---

### 7. Configure Credentials

Add:

* Gmail OAuth2 Credentials
* Google Gemini API Key

---

### 8. Activate Workflow

Enable the workflow.

The workflow will now:

* Monitor Gmail inbox
* Analyze emails using Gemini AI
* Automatically classify emails
* Apply Gmail labels

---

## 🧠 Email Categories

### 🎓 College

Emails related to:

* Exams
* Assignments
* Results
* Notices
* Academic events
* Placements
* University announcements

---

### 💼 Internship

Emails related to:

* Internships
* Training programs
* Workshops
* Recruiters
* Job opportunities
* Career guidance
* Career webinars

---

### 📂 Others

Any email that does not belong to College or Internship categories.

---

## 🐳 Docker Deployment

This project is deployed locally using Docker.

### Benefits

* Persistent workflow storage
* Automatic restart after PC reboot
* Background execution
* Easy backup and migration
* No need to keep VS Code open

---

## 🚀 Live Demo

Current Status:

```text
✅ Running locally using Docker
```

Local URL:

```text
http://localhost:5678
```

> Note: Since this project is self-hosted on Docker, there is no public demo URL.

---

## 📈 Future Improvements

* Add Security email category
* Add Promotions category
* Add Telegram notifications
* Add Email Summarizer using Gemini
* Deploy to Railway or VPS
* Support multiple Gmail accounts
* Add AI-generated email summaries

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome.

Feel free to:

* Fork the repository
* Create a new branch
* Submit a Pull Request

---

## ⭐ Support

If you found this project useful:

* Star ⭐ this repository
* Share it with others
* Follow me on GitHub

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

### Riaz Mohd

GitHub:

https://github.com/Riaz1407

Built with ❤️ using **n8n**, **Docker**, **Google Gemini AI**, and **Gmail API**.
