# Recipe App API

A RESTful API for managing recipes, ingredients, tags, and user accounts, built with **Python, Django REST Framework, and PostgreSQL**.

## Features

- **User Management** — Custom user model with email-based authentication and token authentication.
- **Recipe Management** — Create, retrieve, update, and delete recipes.
- **Ingredients & Tags** — Associate ingredients and reusable tags with recipes.
- **Authentication & Permissions** — Protect endpoints and restrict access to user-owned resources.
- **Filtering** — Filter recipes and retrieve relevant recipe attributes.
- **Image Uploads** — Upload images for individual recipes.
- **API Documentation** — Generate an OpenAPI schema and interactive API documentation.
- **Automated Testing** — Test API endpoints, authentication, permissions, and application behavior.
- **Continuous Integration** — Run automated tests and code quality checks with GitHub Actions.

## 🛠️ Tech Stack

| Technology                | Purpose                      |
| ------------------------- | ---------------------------- |
| Python                    | Programming language         |
| Django                    | Web framework                |
| Django REST Framework     | REST API development         |
| PostgreSQL                | Relational database          |
| Docker & Docker Compose   | Containerized development    |
| drf-spectacular & OpenAPI | API schema and documentation |
| Django Test Framework     | Automated testing            |
| Ruff                      | Linting and code quality     |
| GitHub Actions            | Continuous integration       |

## 🚀 Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/soheilrabiee/recipe-app-api.git
cd recipe-app-api
```

**2. Build and start the application**

```bash
docker compose up --build
```

**3. Access the API**

Once the containers have started, access the application at:

- API root: http://localhost:8000/
- Swagger UI: http://localhost:8000/api/docs/
- OpenAPI schema: http://localhost:8000/api/schema/

The application runs locally using the Docker Compose development configuration.

## 🧪 Running Tests

Run the automated test suite:

```bash
docker compose run --rm app sh -c "python manage.py test"
```

Run Ruff checks:

```bash
docker compose run --rm app sh -c "ruff check ."
```

## 📂 Project Structure

```text
recipe-app-api/
├── .github/
│   └── workflows/           # GitHub Actions CI workflows
├── app/
│   ├── app/                 # Django project configuration
│   ├── core/                # Shared functionality and custom user model
│   ├── user/                # User management and authentication
│   ├── recipe/              # Recipe and related API endpoints
│   ├── manage.py
│   └── pyproject.toml       # Ruff configuration
├── proxy/                   # Nginx reverse proxy configuration
├── scripts/                 # Application startup and utility scripts
├── Dockerfile
├── compose.yml              # Development configuration
├── compose.production.yml   # Production-style configuration
├── .env.sample              # Sample environment variables
├── requirements.txt         # Project dependencies
└── requirements.dev.txt     # Development dependencies
```

## 💡 Key Concepts & Practices

- RESTful API design and Django conventions
- Database modeling, relationships, and migrations
- Serializers, validation, and nested data
- Authentication, permissions, and user-specific querysets
- Automated testing and test-driven development
- Docker-based development workflows
- Production-style configuration with uWSGI and Nginx
- Environment-based configuration
- Continuous integration and code quality checks

## Purpose

A hands-on project focused on building reliable REST APIs and developing practical Django backend engineering skills.
