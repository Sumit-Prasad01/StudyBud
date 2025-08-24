# StudyBud 🎓💬

A lightweight, community-driven chat platform designed specifically for developers and students. StudyBud allows users to join or create topic-specific chat rooms focused on programming technologies and study topics, fostering collaborative learning and knowledge sharing.

## 🌟 Features

- **Topic-Based Chat Rooms**: Create or join rooms focused on specific programming languages and technologies
- **Real-time Messaging**: Instant communication with other developers and learners
- **User Authentication**: Secure user registration and login system
- **Room Management**: Create, edit, and delete study rooms
- **User Profiles**: Personalized user profiles with activity tracking
- **Search Functionality**: Find rooms and topics quickly
- **Mobile Responsive**: Works seamlessly across all devices
- **Activity Feed**: Stay updated with recent room activities and messages

## 🚀 Technologies Used

- **Backend**: Django (Python)
- **Frontend**: HTML5, CSS3, JavaScript
- **Database**: SQLite (default) / PostgreSQL (production)
- **Authentication**: Django's built-in authentication system
- **Styling**: Custom CSS with responsive design

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- pip (Python package installer)
- Git

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Sumit-Prasad01/StudyBud.git
   cd StudyBud
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv studybud_env
   
   # On Windows
   studybud_env\Scripts\activate
   
   # On macOS/Linux
   source studybud_env/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   Open your browser and navigate to `http://127.0.0.1:8000/`

## 📁 Project Structure

```
StudyBud/
│
├── studybud/                 # Main project directory
│   ├── __init__.py
│   ├── settings.py          # Django settings
│   ├── urls.py              # Main URL configuration
│   └── wsgi.py              # WSGI configuration
│
├── base/                    # Main app directory
│   ├── migrations/          # Database migrations
│   ├── templates/           # HTML templates
│   ├── __init__.py
│   ├── admin.py            # Admin configuration
│   ├── apps.py             # App configuration
│   ├── models.py           # Database models
│   ├── urls.py             # App URL patterns
│   └── views.py            # View functions
│
├── static/                  # Static files (CSS, JS, images)
├── media/                   # User uploaded files
├── templates/               # Global templates
├── requirements.txt         # Python dependencies
├── manage.py               # Django management script
└── README.md               # This file
```

## 🎯 Usage

### For Students/Developers:
1. **Sign up** for a new account or **log in** to existing account
2. **Browse rooms** to find topics you're interested in
3. **Join conversations** in existing rooms
4. **Create new rooms** for topics you want to discuss
5. **Participate** in real-time discussions with other learners

### For Room Hosts:
1. **Create rooms** with specific topics (Python, JavaScript, Django, etc.)
2. **Moderate discussions** in your rooms
3. **Edit or delete** rooms you've created
4. **Track activity** in your hosted rooms

## 🛡️ API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Home page with room listings |
| GET | `/login/` | User login page |
| POST | `/login/` | Process login |
| GET | `/register/` | User registration page |
| POST | `/register/` | Process registration |
| GET | `/room/<id>/` | Individual room view |
| GET | `/create-room/` | Create new room form |
| POST | `/create-room/` | Process room creation |
| GET | `/update-room/<id>/` | Edit room form |
| POST | `/update-room/<id>/` | Process room update |
| GET | `/delete-room/<id>/` | Delete room confirmation |
| POST | `/delete-room/<id>/` | Process room deletion |
| GET | `/profile/<id>/` | User profile page |

