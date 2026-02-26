# Proman – Project Management App

Proman is a full‑stack project management application inspired by Ed Roh’s “Build a Nextjs Project Management App & Deploy on AWS” tutorial.  
It provides an opinionated, production‑style stack with a modern dashboard UI, robust backend API, and AWS‑ready deployment setup.

## Features

- Kanban‑style **project boards** with drag‑and‑drop tasks
- Multiple **projects**, each with:
  - Board view
  - List / table view
  - Timeline / Gantt‑style view
- Global **dashboard** with:
  - Project KPIs
  - Charts and analytics
  - Cross‑project timeline
- **Users** and **teams** management, including:
  - Team filtering
  - Export of team data
- **Search** across tasks
- **Light / dark mode**
- Fully **responsive** layout (sidebar + navbar shell)

> Note: This repo is for learning and portfolio purposes.  
> It closely follows Ed Roh’s architecture and code structure, but the project name and configuration are adapted to “Proman”.

---

## Tech Stack

### Frontend

- **Next.js** (App Router)
- **TypeScript**
- **Tailwind CSS**
- **Redux Toolkit** for state management
- **Redux Toolkit Query** for data fetching & caching
- **Material UI Data Grid** for complex tables
- **Recharts** for charts and visualizations
- **React DnD** for drag‑and‑drop boards
- **gantt-task-react** for Gantt/timeline views

### Backend

- **Node.js** + **Express**
- **TypeScript**
- **PostgreSQL**
- **Prisma** ORM
- **PgAdmin** (optional) for DB management

### AWS / Infrastructure (optional but supported)

Proman is designed to be deployable on AWS using:

- **EC2** – backend server
- **RDS (PostgreSQL)** – production database
- **Amplify** – hosting for the Next.js frontend
- **S3** – asset and image storage
- **Cognito** – user authentication and confirmation emails
- **API Gateway** – routing traffic to the backend
- **VPC / networking** – secure isolation and access control

You can also run everything locally without AWS for development.

---

## Project Structure

A typical layout (simplified) looks like:

```text
proman/
  client/           # Next.js frontend
    src/
      app/
      components/
      features/
      redux/
    public/
    tailwind.config.ts
  server/           # Node/Express backend
    src/
      index.ts
      routes/
      controllers/
      prisma/
        schema.prisma
        seedData/
  .env
  README.md
