# Task Management API - CodeNova Task 2

A RESTful API built with Django REST Framework for managing tasks with priorities, status tracking, due dates, sorting, and filtering capabilities.

## Features
- Full CRUD operations for tasks
- Pagination for listing endpoints (5 items per page)
- Query parameter filtering by `status` and `priority`
- Sorting by `created_at` or `due_date`

## Database Seed
To load the sample test data into the SQLite database, run:
`python manage.py loaddata seed_data.json`

## API Endpoints & Query Parameters

**Base URL**: `http://127.0.0.1:8000/api/tasks/`

| Parameter | Type | Description |
|-----------|------|-------------|
| status | string | Filter by Todo, In Progress, or Done |
| priority | string | Filter by Low, Medium, or High |
| ordering | string | Sort by created_at, -created_at, due_date, or -due_date |
| page | int | Page number for pagination |

## Test cURL Commands

**1. Get all tasks (Paginated)**
```bash
curl -X GET [http://127.0.0.1:8000/api/tasks/](http://127.0.0.1:8000/api/tasks/)