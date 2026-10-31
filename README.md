# Employee Management System

A full-stack web application for managing employee information, departments, salaries, and organizational activities through a centralized dashboard.

## Features

- Employee dashboard with statistics
- Add, view, update, and delete employee records
- Employee search, filtering, and sorting
- Table and grid views
- Bulk employee deletion
- Department management
- Salary analytics and charts
- Employee details and performance information
- Activity logs
- MongoDB integration with in-memory demo data fallback

## Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React 19, Vite 8, CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| Icons and animations | Lucide React, Motion |
| Package manager | Bun or npm |

## Project Structure

```text
Employee_management_system/
├── server/
│   ├── db.js
│   └── routes.js
├── src/
│   ├── components/
│   ├── App.jsx
│   ├── api.js
│   ├── index.css
│   └── main.jsx
├── .env.example
├── .gitignore
├── bun.lock
├── index.html
├── metadata.json
├── package.json
├── server.js
├── tsconfig.json
└── vite.config.ts
```

## Installation

Prerequisites: Node.js and npm or Bun.

Clone the repository:

```bash
git clone https://github.com/srujana-Kotcherla-29/Employee_management_system.git
cd Employee_management_system
```

Install dependencies:

```bash
npm install
```

Alternatively:

```bash
bun install
```

## Environment Configuration

Create a local environment file:

```powershell
Copy-Item .env.example .env
```

Example configuration:

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/employee_db
APP_URL=http://localhost:3000
```

Configure MongoDB locally or use an appropriate MongoDB connection URI.

The application includes in-memory demo data when MongoDB is not connected. Changes made in memory are not persistent after restarting the server.

## Run the Application

Start the application:

```bash
npm run dev
```

The application runs at:

http://localhost:3000

The same server can also be started using:

```bash
npm start
```

## Production Build

Generate the frontend build:

```bash
npm run build
```

For production mode, set `NODE_ENV=production` before starting the server.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/health` | Check application and database status |
| GET | `/api/stats` | Retrieve dashboard statistics |
| GET | `/api/employees` | Retrieve and filter employees |
| GET | `/api/employees/:id` | Retrieve employee details |
| POST | `/api/employees` | Create an employee |
| PUT | `/api/employees/:id` | Update an employee |
| DELETE | `/api/employees/:id` | Delete an employee |
| POST | `/api/employees/batch-delete` | Delete multiple employees |
| GET | `/api/departments` | Retrieve departments |
| POST | `/api/departments` | Create a department |
| PUT | `/api/departments/:id` | Update a department |
| DELETE | `/api/departments/:id` | Delete a department |
| GET | `/api/activity` | Retrieve activity logs |
| POST | `/api/seed` | Reset demo database data |

## Security Note

The current project does not implement user authentication. The `/api/seed` endpoint resets application data and should be protected or disabled before public deployment.

## Team Credits

This repository is an individual submission copy of a collaborative academic team project.

Original source repository:

https://github.com/mahadevupratheep/Employee_management_system

The original project creator and all contributing team members are acknowledged for their work. This repository maintains an independent submission history for the team member `srujana-Kotcherla-29`.

## Future Enhancements

- User authentication and role-based access
- Employee attendance and leave management
- Payroll enhancements
- Additional reporting and security features
