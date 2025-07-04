readme_content = """
# 🏥 MedTrack - Cloud-Enabled Healthcare Management System

**MedTrack** is a cloud-based healthcare management system built with **Flask**, **AWS DynamoDB**, and **AWS SNS**. It enables **patients** to book appointments, manage profiles, and view history, while **doctors** can manage schedules and appointments efficiently.

---

## 📌 Key Features

- ✅ **User Registration** (Doctor / Patient)
- ✅ **Role-Based Secure Login**
- ✅ **Book & Manage Appointments**
- ✅ **Doctor Dashboard** to manage appointments
- ✅ **Appointment Search** (by name or date)
- ✅ **Email Notifications** via SMTP
- ✅ **AWS DynamoDB Integration**
- ✅ **Custom 404 Error Page**
- ✅ **Responsive UI with Bootstrap**
- ✅ **Dark Mode & Accessibility Support**

---

## 👤 User Roles

- **Patient** – Book appointments, view history, manage profile  
- **Doctor** – Manage appointments, update status  
- **Admin** – (Optional) Monitor and manage overall system behavior

---

## 🚀 Live Demo *(Optional)*

> [🌐 Add your live URL here if hosted]

---

## ⚙️ Tech Stack

| Tech               | Purpose                                 |
|--------------------|------------------------------------------|
| Python (Flask)     | Backend Web Application                  |
| AWS DynamoDB       | NoSQL Database for user & appointment data |
| AWS SNS            | (Optional) Notifications service         |
| Bootstrap 5        | Responsive UI                            |
| Jinja2             | HTML Templating                          |
| smtplib (SMTP)     | Email Notifications                      |
| python-dotenv      | Secure environment variable management   |
| Werkzeug           | Password hashing and security            |

---

## 📁 Project Structure

```

MedTrack/
├── app.py
├── requirements.txt
├── .env
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   ├── dashboard\_patient.html
│   ├── dashboard\_doctor.html
│   ├── book\_appointment.html
│   ├── view\_appointment\_patient.html
│   ├── view\_appointment\_doctor.html
│   ├── search\_results.html
│   ├── profile.html
│   └── 404.html
├── static/
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── scripts.js
└── README.md

````

---

## 🛠️ Environment Variables

Create a `.env` file with the following keys:

```env
SECRET_KEY=<your_secret_key_here>
EMAIL_USER=<your_email_address>
EMAIL_PASS=<your_email_password_or_app_password>
AWS_ACCESS_KEY_ID=<your_aws_access_key>
AWS_SECRET_ACCESS_KEY=<your_aws_secret_key>
AWS_REGION=<your_aws_region>
DYNAMODB_USERS_TABLE=Users
DYNAMODB_APPOINTMENTS_TABLE=Appointments
SNS_TOPIC_ARN=<your_topic_arn>  # Optional
````

---

## 🗃️ DynamoDB Tables

### `Users` Table

| Attribute | Type   | Description           |
| --------- | ------ | --------------------- |
| email     | HASH   | Unique user ID        |
| name      | String | Full name             |
| role      | String | `patient` or `doctor` |

### `Appointments` Table

| Attribute       | Type   | Description                         |
| --------------- | ------ | ----------------------------------- |
| appointment\_id | HASH   | Unique appointment ID               |
| patient         | String | Patient email                       |
| doctor          | String | Doctor email                        |
| date            | String | Format: `YYYY-MM-DD`                |
| time            | String | Format: `HH:MM`                     |
| status          | String | `pending`, `confirmed`, `completed` |

---

## 📧 Email Notifications

Email alerts are sent for:

* ✅ Appointment bookings
* ✅ Confirmation updates
* ✅ Cancellations
* ✅ (Optional) Admin alerts

Implemented using **Python's `smtplib`** and Gmail's SMTP.

---

## ✅ Functional Testing

| Feature                     | Status |
| --------------------------- | ------ |
| Home Page Navigation        | ✔️     |
| Doctor/Patient Registration | ✔️     |
| Secure Login                | ✔️     |
| Patient Dashboard           | ✔️     |
| Doctor Dashboard            | ✔️     |
| Book Appointment            | ✔️     |
| Appointment Search          | ✔️     |
| DynamoDB Integration        | ✔️     |
| Email Notifications         | ✔️     |
| Error Handling (404 Page)   | ✔️     |

---

## 🚀 Deployment Notes

> For production deployment:

* Use `gunicorn` or `uWSGI` with **Nginx** or **Apache**
* Or deploy on platforms like **AWS EC2**, **Heroku**, or **Render**

---

## 👨‍💻 Author

**Developed by:** [@dedeepya]
📧 **Contact:** dedeepyapotnuru.com
"""


