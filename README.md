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
* Runs locally or can be deployed to cloud platforms like Railway.

---

## 🛠️ Tech Stack

* **n8n**
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

## 📁 Repository Structure

```text
n8n-gmail-auto-labeler
│
├── workflows
│   └── mail_auto_label.json
│
├── screenshots
│   └── workflow.png
│
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Riaz1407/n8n-gmail-auto-labeler.git
```

### 2. Import Workflow

* Open n8n.
* Click **Import from File**.
* Select:

```text
workflows/mail_auto_label.json
```

### 3. Configure Credentials

Add:

* Gmail OAuth Credentials
* Google Gemini API Key

### 4. Activate Workflow

Enable the workflow and n8n will start automatically labeling incoming emails.

---

## 🧠 Email Categories

### College

Emails related to:

* Exams
* Assignments
* Results
* Notices
* Academic events
* Placements

### Internship

Emails related to:

* Internships
* Training programs
* Workshops
* Recruiters
* Job opportunities
* Career guidance

### Others

Any email that does not belong to College or Internship categories.

---

## 🔮 Future Improvements

* Add Security email category.
* Add Promotions category.
* Add Telegram notifications.
* Deploy workflow to Railway for 24/7 uptime.
* Add email summarization using Gemini.

---

## 👨‍💻 Author

**Riaz Mohd**

GitHub: https://github.com/Riaz1407
