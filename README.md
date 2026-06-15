# n8n Gmail Auto Labeler 📧🤖

An AI-powered Gmail automation workflow built with **n8n** that automatically classifies incoming emails and applies Gmail labels using **Google Gemini AI**.

## 🚀 Features

* Automatically listens for new Gmail messages.
* Uses **Google Gemini AI** to classify emails.
* Automatically applies Gmail labels based on email content.
* Categories supported:

  * 🎓 College
  * 💼 Internship
  * 📂 Others
* Runs locally using Docker.
* Can be deployed to cloud platforms like Railway.

---

## 🛠️ Tech Stack

* **n8n**
* **Docker**
* **Google Gemini API**
* **Gmail API**
* **GitHub**

---

## 📌 Workflow

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

Add your screenshot here:

```text
screenshots/workflow.png
```

### Docker Running

```text
screenshots/docker-running.png
```

### Successful Execution

```text
screenshots/execution.png
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
│   └── execution.png
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Riaz1407/n8n-gmail-auto-labeler.git
cd n8n-gmail-auto-labeler
```

---

### 2. Install Docker

Download and install Docker Desktop.

Verify installation:

```bash
docker --version
```

---

### 3. Run n8n with Docker

Create a volume:

```bash
docker volume create n8n_data
```

Run n8n:

```bash
docker run -d --restart unless-stopped \
--name n8n \
-p 5678:5678 \
-v n8n_data:/home/node/.n8n \
docker.n8n.io/n8nio/n8n
```

Open:

```text
http://localhost:5678
```

---

### 4. Import Workflow

* Open n8n.
* Click **Import from File**.
* Select:

```text
workflows/mail_auto_label.json
```

---

### 5. Configure Credentials

Add:

* Gmail OAuth Credentials
* Google Gemini API Key

---

### 6. Activate Workflow

Enable the workflow.

n8n will automatically monitor incoming emails and apply labels.

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

---

### 📂 Others

Any email that does not belong to College or Internship categories.

---

## 🐳 Docker Deployment

This project is deployed locally using Docker.

Benefits:

✅ Persistent workflow storage
✅ Automatic restart after PC reboot
✅ Background execution
✅ Easy backup and migration

---

## 🚀 Live Demo

This workflow is currently:

```text
Running locally on Docker
```

Local URL:

```text
http://localhost:5678
```

*Note: Since the workflow is self-hosted, there is no public demo URL available.*

---

## 🔮 Future Improvements

* Add Security email category.
* Add Promotions category.
* Add Telegram notifications.
* Deploy workflow to Railway for 24/7 uptime.
* Add email summarization using Gemini.
* Add support for multiple Gmail accounts.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.

Feel free to fork this repository and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Riaz Mohd**

GitHub: https://github.com/Riaz1407

Built with ❤️ using n8n, Docker, Gmail API and Google Gemini AI.
