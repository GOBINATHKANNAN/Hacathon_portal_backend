# Hackathon Management Portal — Backend

Backend services for a college hackathon participation management platform developed for the Department of Computer Science and Business Systems, Thiagarajar College of Engineering.

## Overview

The system manages student hackathon submissions, verification workflows, participation tracking, notifications, and administrative reporting.

## Core Capabilities

- Student registration and authentication with institutional email validation
- Role-based access for students, proctors, and administrators
- Hackathon submission and certificate upload workflow
- Proctor review and approval/rejection of submissions
- Participation history and status tracking
- Email notifications for registration, submission, and review outcomes
- Administrative statistics and reporting
- CSV export support

## Technology Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB
- **ODM:** Mongoose
- **Authentication:** JWT
- **Security:** Bcrypt
- **Email:** Nodemailer
- **File Uploads:** Multer

## Architecture

```text
Client Applications
        |
        v
   Express REST API
        |
  +-----+-----+----------------+
  |           |                |
Auth      Hackathons       Users/Admin
  |           |                |
  +-----------+----------------+
              |
              v
           MongoDB
              |
              v
        Email / File Services
```

## Local Development

### Prerequisites

- Node.js 16+
- MongoDB (local or MongoDB Atlas)

### Setup

```bash
git clone https://github.com/GOBINATHKANNAN/Hacathon_portal_backend.git
cd Hacathon_portal_backend
npm install
```

Create a local `.env` file using your own development values:

```env
PORT=5000
MONGO_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-secret>
EMAIL_USER=<your-email>
EMAIL_PASS=<your-email-app-password>
```

Never commit `.env`, credentials, API keys, or other secrets to the repository.

### Run

```bash
npm start
```

## API Areas

- Authentication and authorization
- Hackathon submission and review
- Student participation history
- User and role management
- Administrative reporting

## Engineering Focus

This project demonstrates practical backend development using REST APIs, authentication, role-based authorization, database modeling, file handling, email integration, and CRUD workflows.

## Related Frontend

The frontend is maintained separately in the companion repository:

`GOBINATHKANNAN/hacathon_portal_frontend`

## Project Context

**Academic Project — Thiagarajar College of Engineering**  
Department of Computer Science and Business Systems
