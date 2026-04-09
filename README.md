# Task Manager - Full Stack Assignment

This project is a small full-stack Task Manager app built to satisfy the assignment requirements.

## Tech Stack

- Frontend: React + Vite
- Backend: Node.js + Express
- Storage: File-based JSON (`backend/tasks.json`)

## Features

- View all tasks
- Add a new task
- Mark task as completed
- Delete task
- Basic loading/error handling on frontend
- Basic request validation on backend

## Project Structure

- `frontend/` - React client
- `backend/` - Express API server

## Prerequisites

- Node.js 18+ (tested with newer Node as well)
- npm

## Setup

Install dependencies for both apps:

```bash
cd backend
npm install

cd ../frontend
npm install
```

## Run Locally

Start backend (Terminal 1):

```bash
cd backend
npm start
```

Backend runs on `http://localhost:5000`.

Start frontend (Terminal 2):

```bash
cd frontend
npm run dev
```

Frontend runs on Vite default URL (usually `http://localhost:5173`).

## API Endpoints

- `GET /tasks` - Return all tasks
- `POST /tasks` - Create task (expects `{ "title": "..." }`)
- `PATCH /tasks/:id` - Update task (supports `completed` and `title`)
- `DELETE /tasks/:id` - Delete task

## Validation Notes

- `title` must be a non-empty string
- `completed` must be a boolean when provided
- API returns JSON errors for invalid requests and server failures
