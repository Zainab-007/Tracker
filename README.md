# 🎯 Smart Internship Tracker

**A web-based internship management platform that helps students discover relevant opportunities, organize applications, and track their internship journey in one place.**

Smart Internship Tracker is a Flask-based web application built to simplify internship management. It combines skill-based recommendations with application tracking, deadline planning, resume management, and analytics to help students stay organized throughout their internship search.

## ✨ Features

### 🔐 User Authentication
- Register and log in using an email address or username.
- Secure password hashing.
- Personalized dashboard and profile management.

### 🤖 Skill-Based Internship Recommendations
- Matches student skills with internship descriptions using **TF-IDF vectorization and cosine similarity**.
- Calculates similarity scores for available internships.
- Prioritizes relevant opportunities on the dashboard.

### 📋 Application Tracking
- Track internship applications and their statuses.
- View application history and status timelines.
- Add application notes.
- Maintain a checklist for resume readiness, skill matching, deadlines, cover letters, and company research.

### 📄 Resume Management
- Upload resumes in PDF, DOC, and DOCX formats.
- Store resume files for internship applications.

### 📅 Internship Discovery and Planning
- Browse internship opportunities and view their details.
- Bookmark internships for later.
- Compare internship opportunities.
- View recently visited internships.
- Explore internship deadlines through a calendar.

### 📊 Skill Gap Analysis and Analytics
- Identify skills that may be missing for selected opportunities.
- Compare existing skills with internship requirements.
- View application statistics and status breakdowns.
- Analyze applications by month, company, and internship field.

### 🔔 Additional Features
- Notifications for shared internship opportunities.
- Share internship listings with other users.
- Rate and review internship opportunities.
- View and update profile information.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Web application framework |
| MySQL | Relational database |
| HTML | Page structure |
| CSS | Styling and layout |
| JavaScript | Client-side interactions |
| Scikit-learn | TF-IDF and cosine similarity |
| Werkzeug | Password hashing and secure filename handling |
| python-dotenv | Environment variable configuration |

## 🏗️ Project Structure

```text
Tracker/
├── app.py                 # Flask application and routes
├── templates/             # HTML templates
├── static/                # CSS, JavaScript, images and uploads
├── .env                   # Local environment configuration
├── .gitignore             # Files excluded from Git
└── README.md              # Project documentation
```

*The structure above describes the main application files. Keep local environment files and virtual environments out of the published repository.*

## ⚙️ Getting Started

### Prerequisites

Install the following before running the project:

- Python 3.10 or a compatible Python version
- MySQL Server
- Git
- A web browser

### 1. Clone the Repository

```bash
git clone https://github.com/Zainab-007/Tracker.git
cd Tracker
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install Flask Flask-MySQLdb scikit-learn python-dotenv
```

If a `requirements.txt` file is available, use it instead:

```bash
pip install -r requirements.txt
```

### 4. Configure MySQL

Start your MySQL server and create the database configured for the application.

```sql
CREATE DATABASE interntrack;
```

The application expects the database tables required for users, internships, applications, bookmarks, reviews, notifications, application history, checklists, and recently viewed internships.

**Important:** Creating the database alone is not enough. The required tables and their columns must also be created before the application can run. Use the project's database schema if available.

### 5. Configure Environment Variables

Create a `.env` file in the project root and configure your local database connection and Flask secret key.

```env
SECRET_KEY=replace_with_a_long_random_secret
MYSQL_HOST=localhost
MYSQL_USER=your_mysql_username
MYSQL_PASSWORD=your_mysql_password
MYSQL_DB=interntrack
```

Replace the example values with your local configuration. Never commit your real `.env` file or credentials to GitHub.

### 6. Run the Application

```bash
python app.py
```

Open the local address displayed in your terminal, typically:

```text
http://127.0.0.1:5000
```

Register a new account to explore the application.

## 🔄 Application Workflow

1. **Register:** Create an account and provide your profile information and skills.
2. **Discover:** Browse internship listings and receive skill-based recommendations.
3. **Evaluate:** Compare opportunities, review requirements, and identify skill gaps.
4. **Organize:** Bookmark opportunities, maintain checklists, and monitor deadlines.
5. **Track:** Record application progress and review application history.
6. **Analyze:** Use the dashboard and analytics to understand your internship search.

## 🔒 Security Notes

- Passwords are hashed before storage.
- Database queries use parameterized values in the application.
- Environment variables should be used for credentials and secret keys.
- Resume uploads should be validated and handled securely.
- Production deployments should use a strong secret key, secure session settings, and a production-ready WSGI server.

## 🚀 Future Improvements

- Automated deadline reminders through email or notifications.
- Resume parsing and more detailed skill extraction.
- Improved matching explanations and recommendation accuracy.
- Internship data import from verified sources.
- Advanced filtering by location, stipend, duration, and work mode.
- Improved accessibility and mobile responsiveness.
- Automated testing and continuous integration.
- Deployment to a cloud hosting platform.

## 🎯 Project Goal

The goal of Smart Internship Tracker is to help students manage internship opportunities more efficiently, make informed application decisions, and identify skills they can develop to improve their career prospects.

## 👩‍💻 Author

**Zainab Shaikh**

GitHub: [@Zainab-007](https://github.com/Zainab-007)

## 📌 Repository

[View Smart Internship Tracker on GitHub](https://github.com/Zainab-007/Tracker)

---

<p align="center">
  <b>Smart Internship Tracker — Organize your search. Track your progress. Move toward your goals. 🚀</b>
</p>
