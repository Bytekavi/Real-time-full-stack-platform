# Campus Connect - Real-Time Full Stack Platform

Campus Connect is a real-time campus collaboration platform built with React,
Node.js, Express, Socket.IO, PostgreSQL, JWT authentication, RBAC, Docker, and
GitHub Actions.

The project is structured as a GitHub-ready monorepo with a React/Vite client,
an Express REST API, authenticated Socket.IO events, database schema, local
Docker Compose environment, and CI workflow.

## Highlights

- React.js + Socket.IO frontend for live channels, presence, posts, and campus events
- Node.js/Express.js REST API with JWT authentication and role-based access control
- PostgreSQL schema with practical indexes for feed, user, and event queries
- Dockerized API, frontend, and database for reproducible local runs
- GitHub Actions CI for server tests and frontend build checks
- GCP-ready container images and environment-driven configuration

## Tech Stack

<p>
  <img src="https://img.shields.io/badge/React.js-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React.js">
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite">
  <img src="https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="Socket.IO">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js">
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT">
  <img src="https://img.shields.io/badge/RBAC-E75D38?style=for-the-badge" alt="RBAC">
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Google Cloud Platform">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions">
</p>

- Frontend: React.js, Vite, Socket.IO Client
- Backend: Node.js, Express.js, Socket.IO, JWT, bcrypt
- Database: PostgreSQL
- Infrastructure: Docker, Docker Compose, GitHub Actions, GCP-ready containers

## Quick Start

```bash
cp .env.example .env
docker compose up --build
```

Open the app at:

```text
http://localhost:8080
```

API health check:

```text
http://localhost:4000/health
```

## Local Development

Install dependencies:

```bash
pnpm install
```

The root scripts are also npm-compatible if you prefer `npm install`.

Run PostgreSQL:

```bash
docker compose up db
```

Run the API and web app:

```bash
pnpm run dev
```

Client:

```text
http://localhost:5173
```

Server:

```text
http://localhost:4000
```

## Environment

Copy `.env.example` to `.env` and update values as needed.

Important values:

- `DATABASE_URL`: PostgreSQL connection string
- `JWT_SECRET`: secret used to sign JWT tokens
- `CLIENT_ORIGIN`: allowed browser origin for API and Socket.IO
- `SEED_ADMIN_EMAIL` / `SEED_ADMIN_PASSWORD`: optional seeded admin account

## Demo Roles

Public signup creates a `student` account. Admin and moderator capabilities are
available through seeded or manually updated users.

Roles:

- `student`: create posts, RSVP to events, join realtime channels
- `moderator`: student permissions plus event creation and content moderation
- `admin`: moderator permissions plus platform metrics

## API Overview

Authentication:

- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/me`

Posts:

- `GET /api/posts`
- `POST /api/posts`
- `DELETE /api/posts/:id`

Events:

- `GET /api/events`
- `POST /api/events`
- `POST /api/events/:id/rsvp`

Admin:

- `GET /api/admin/metrics`

Socket.IO events:

- `channel:join`
- `message:send`
- `typing:start`
- `typing:stop`
- `post:created`
- `presence:update`
- `event:created`
- `event:rsvp`

## Resume Summary

Campus Connect - Real-Time Full Stack Platform - GitHub  
Tech Stack: React.js, Node.js, Express.js, Socket.io, PostgreSQL, JWT, Docker,
GCP, GitHub Actions

- Full stack application built in 36 hours with a React.js + Socket.io frontend
  and Node.js/Express.js REST API backend; designed for 500+ concurrent users
  and placed Top-10 among 200+ teams.
- Implemented JWT authentication, RBAC, database optimization, Docker
  containerization, and CI/CD deployment workflow under time constraints.

Date: February 2025
