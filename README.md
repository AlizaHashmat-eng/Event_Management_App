##Event Management System

Welcome to the **Event Management System**, a powerful web application built with **Cookiecutter Django** that simplifies the process of organizing and managing events. The system comes with essential features like user management, email verification, Celery for background task processing, and Docker support for easy deployment.

---

## 🚀 Key Features

- **User Management**: Includes normal user and superuser roles with email verification.
- **Celery Integration**: Supports background tasks and periodic scheduling.
- **Test Coverage**: Tools for testing and monitoring test coverage.
- **Docker Support**: Easy containerization and deployment with Docker.
- **Live Reload & Sass Compilation**: Streamlined development with automatic reload and Sass support.

---

## 🛠️ Setup and Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/event-management-system.git
cd event-management-system
```

### 2. Install Dependencies

Make sure you have Python and Docker installed. Then, install project dependencies:

```bash
pip install -r requirements/local.txt
```

### 3. Create Superuser

Run the following command to create an admin user:

```bash
python manage.py createsuperuser
```

### 4. Run the Application

To start the development server with live reloading and Sass compilation, use:

```bash
docker-compose -f docker-compose.local.yml up
```

Access the application at `http://localhost:8000`.

---

## ✅ Testing and Type Checks

### Run Tests

```bash
pytest
```

### Check Test Coverage

```bash
coverage run -m pytest
coverage html
open htmlcov/index.html
```

### Type Checks with `mypy`

```bash
mypy my_event_manager
```

---

## ⚙️ Celery Setup

To run a Celery worker:

```bash
celery -A config.celery_app worker -l info
```

For periodic tasks, start the Celery beat scheduler:

```bash
celery -A config.celery_app beat
```

---

## 🚢 Deployment

The app is Docker-ready! Follow these steps for deployment:

1. **Build and run with Docker**:

   ```bash
   docker-compose -f docker-compose.production.yml up --build
   ```

2. Check detailed Docker documentation for more deployment options.

---

## 📚 Documentation

For more detailed instructions and settings configuration, please refer to the `docs/` folder.

---

## License

This project is licensed under the **Apache 2.0 License**.

---

## 👨‍💻 Contributors

Special thanks to all contributors. Check out the `CONTRIBUTORS.txt` file for details.

---

### ⭐ If you found this project useful, please star the repository and feel free to contribute!
