# Recipe App API

This project is a RESTful API for managing recipes, built with Django and Django REST Framework. It supports creating, updating, and deleting recipes, along with managing ingredients and tags. It follows test-driven development practices and includes image upload and API documentation.

## Features

* Token-based user authentication
* Recipe management (CRUD)
* Tag and ingredient management
* Recipe image uploads
* **Django admin interface**
* **Auto-generated API documentation with Swagger (via drf-spectacular)**
* **PostgreSQL as the database backend**
* Dockerized for local development
* GitHub Actions for continuous integration
* Pytest-based test suite

## Tech Stack

* **Backend:** Python, Django, Django REST Framework
* **Database:** PostgreSQL
* **Containerization:** Docker, Docker Compose
* **CI/CD:** GitHub Actions
* **Testing:** Pytest

## Getting Started

### Prerequisites

* Docker
* Docker Compose

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/d3meter/recipe-app-api.git
   cd recipe-app-api
   ```

2. Build and start the containers:
   ```bash
   docker compose build
   ```

   ```bash
   docker compose up
   ```

4. Apply migrations and create a superuser:

   ```bash
   docker compose run --rm app sh -c "python manage.py migrate && python manage.py createsuperuser"
   ```

5. Access the API at:
   `http://localhost:8000/api/`

## API Documentation

Explore the API in two ways:

* **Swagger UI**: [http://localhost:8000/api/docs/](http://localhost:8000/api/docs/)
* **Browsable API (DRF)**: Navigate directly to any endpoint

## Django Admin

To access the Django admin panel:

1. Create a superuser (if not done yet):

   ```bash
   docker compose run --rm app sh -c "python manage.py createsuperuser"
   ```

2. Visit: [http://localhost:8000/admin/](http://localhost:8000/admin/)

## Running Tests

Run the test suite with:

```bash
docker compose run --rm app sh -c "pytest"
```
