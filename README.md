# Flask TODO List (In-Memory)

## Overview
A minimal Flask web app to manage a simple in-memory TODO list. It supports:
- Viewing all tasks at the root route (/)
- Adding tasks via POST to /add
- Deleting tasks via POST to /delete/<id>

Data is stored in memory (Python process), making it ideal for demos and small experiments.

## Setup
1. Requirements
   - Python 3.8+
   - Flask

2. Install dependencies
   - pip install Flask

3. Run the app
   - python index.html

4. Open in your browser
   - http://localhost:5000

## Usage
- View tasks: Navigate to http://localhost:5000 to see the list of tasks.
- Add a task: Use the input box at the top and click Add (sends POST to /add).
- Delete a task: Click Delete next to a task (sends POST to /delete/<id>).

Endpoints:
- GET / — Renders the HTML page listing tasks.
- POST /add — Adds a new task with form field task.
- POST /delete/<id> — Deletes a task by numeric id.

Notes:
- Tasks are stored only in memory and will reset when the server restarts.
- IDs are incrementing integers assigned at creation time.

## Improvements
- Persistence: Store tasks in a file or database (SQLite) so data survives restarts.
- CSRF protection: Integrate Flask-WTF or generate tokens for forms.
- Edit and complete: Add endpoints and UI to edit tasks and mark them as completed.
- API layer: Provide JSON endpoints for programmatic access and SPA usage.
- Validation: Add stricter validation and error messaging for edge cases (e.g., overly long inputs).
- Tests: Unit and integration tests for routes and template rendering.