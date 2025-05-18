ALX Travel App
A robust Django-based travel listing platform with a focus on scalable backend architecture, MySQL database integration, and comprehensive API documentation.
Project Overview
ALX Travel App is a professional travel listing platform built with Django and Django REST Framework. This project serves as a foundation for a scalable travel application with industry-standard best practices for project structure, database configuration, and API documentation.
Key Features

Modular Project Structure: Organized following Django's best practices for maintainability and scalability
MySQL Database Integration: Robust database configuration with proper connection handling
API Documentation: Automated API documentation using Swagger/OpenAPI (drf-yasg)
Background Task Processing: Integration with Celery and RabbitMQ for asynchronous task processing
Secure Configuration: Environment variable management with django-environ for enhanced security
CORS Support: Cross-Origin Resource Sharing configured for frontend integration

Technology Stack

Backend Framework: Django + Django REST Framework
Database: MySQL
API Documentation: drf-yasg (Swagger/OpenAPI)
Task Queue: Celery + RabbitMQ
Environment Management: django-environ
Cross-Origin Support: django-cors-headers

Installation & Setup
Prerequisites

Python 3.8+
MySQL
RabbitMQ (for Celery)

Step 1: Clone the Repository
bashgit clone https://github.com/yourusername/alx_travel_app.git
cd alx_travel_app
Step 2: Set Up Virtual Environment
bashpython -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Step 3: Install Dependencies
bashpip install -r requirements.txt
Step 4: Configure Environment Variables
Create a .env file in the root directory:
DEBUG=True
SECRET_KEY=your-secret-key-here
DB_NAME=alx_travel_app
DB_USER=yourdbuser
DB_PASSWORD=yourdbpassword
DB_HOST=localhost
DB_PORT=3306
Step 5: Create the Database
sqlCREATE DATABASE alx_travel_app CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
Step 6: Run Migrations
bashpython manage.py makemigrations
python manage.py migrate
Step 7: Start the Development Server
bashpython manage.py runserver
Project Structure
alx_travel_app/
├── alx_travel_app/          # Main project directory
│   ├── __init__.py          # Celery configuration
│   ├── celery.py            # Celery app setup
│   ├── settings.py          # Project settings
│   ├── urls.py              # Main URL routing
│   ├── wsgi.py              # WSGI configuration
│   └── asgi.py              # ASGI configuration
├── listings/                # Listings application
│   ├── migrations/          # Database migrations
│   ├── __init__.py
│   ├── admin.py             # Admin interface configuration
│   ├── apps.py              # App configuration
│   ├── models.py            # Data models
│   ├── tests.py             # Unit tests
│   ├── urls.py              # App-specific URLs
│   └── views.py             # View functions/classes
├── .env                     # Environment variables
├── .gitignore               # Git ignore file
├── manage.py                # Django management script
└── requirements.txt         # Project dependencies
API Documentation
The API documentation is available at:

Swagger UI: /swagger/
ReDoc: /redoc/

Background Tasks with Celery
Start the Celery worker:
bashcelery -A alx_travel_app worker -l info
Development Guidelines

Code Style: Follow PEP 8 guidelines
Documentation: Document all functions, classes, and complex logic
Testing: Write tests for all new features
Git Workflow: Use feature branches and pull requests

License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgements

Django project structure best practices
RESTful API design principles
Secure database configuration practices