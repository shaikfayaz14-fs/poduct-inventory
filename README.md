# Poduct Inventory

A simple product inventory application with a React frontend and a Python-based data layer using SQLAlchemy and SQLite.

## Overview

This repository contains a small inventory management project for tracking products, including:

- product name
- description
- price
- quantity

The app is split into two main parts:

- `frontend/` — React + JavaScript UI
- root Python files — database models and product schema definitions

## Project Structure

```text
poduct-inventory/
├── README.md
├── database_models.py
├── models.py
├── products.db
├── frontend/
│   ├── package.json
│   ├── package-lock.json
│   ├── public/
│   └── src/
│       ├── App.js
│       ├── App.css
│       ├── index.js
│       ├── index.css
│       ├── TaglineSection.js
│       └── TaglineSection.css
└── __pycache__/
```

## Tech Stack

- Frontend: React, JavaScript, CSS
- Backend/data layer: Python, SQLAlchemy, Pydantic
- Database: SQLite (`products.db`)

## Features

- Add and manage products
- Store product details in SQLite
- Display product inventory in a web interface
- React-based frontend served locally with a proxy to the backend API

## Prerequisites

Before running the project, make sure you have installed:

- Python 3.9+
- Node.js and npm
- A virtual environment tool such as `venv`

## Setup

### 1. Create a Python virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 2. Install Python dependencies

```bash
pip install fastapi uvicorn sqlalchemy pydantic
```

### 3. Install frontend dependencies

```bash
cd frontend
npm install
```

## Running the Application

### Start the frontend

```bash
cd frontend
npm start
```

### Start the backend API

If your Python API entry point is a file such as `main.py`, run:

```bash
uvicorn main:app --reload
```

If your app exposes the API in a different module, adjust the command accordingly.

## Notes

- The frontend is configured with a proxy to `http://localhost:8000` in `frontend/package.json`.
- The repo currently includes a SQLite database file named `products.db`.
- The SQLAlchemy model defines a `Product` table with fields for `id`, `name`, `description`, `price`, and `quantity`.

## License

This project does not currently include a license file. If you plan to publish or distribute it publicly, consider adding an appropriate open-source license.

## Contributing

Contributions are welcome. If you want to improve the app, consider:

- improving the UI/UX
- adding validation and error handling
- extending inventory features like search, filtering, and editing
- adding tests for backend and frontend behavior
