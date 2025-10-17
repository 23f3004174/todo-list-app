# Simple Flask TODO List

## Overview
This is a minimal Flask web app for managing a simple in-memory TODO list. It supports:
- Viewing tasks at the root route: GET /
- Adding a task via POST /add
- Deleting a task by ID via POST /delete/<id> (GET supported for convenience)

Tasks are stored in memory and will reset when the server restarts.

## Setup
1. Prerequisites:
   - Python 3.8+ installed
   - Pip available

2. Install dependencies:
   - pip install Flask

## Usage
1. Run the app:
   - python index.html

2. Open in your browser:
   - http://127.0.0.1:5000/

3. Add tasks:
   - Use the form at the top of the page, or via curl:
     - curl -X POST -F "task=Buy milk" http://127.0.0.1:5000/add

4. Delete tasks:
   - Click the Delete button next to a task, or via curl:
     - curl -X POST http://127.0.0.1:5000/delete/1

5. Notes:
   - Data is stored in-memory; restarting the server clears all tasks.
   - The app accepts GET /delete/<id> for convenience in a browser, but POST is recommended.