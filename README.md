# <div align="center">AlMethaq System</div>

<div align="center">
  <p><strong>Modern educational management platform for dashboards, students, teachers, reports, and real-time workflows.</strong></p>

  <p>
    <img src="https://img.shields.io/badge/Django-6.0-0C4B33?style=for-the-badge&logo=django&logoColor=white" alt="Django 6.0" />
    <img src="https://img.shields.io/badge/Channels-4.3-FF6B6B?style=for-the-badge" alt="Channels" />
    <img src="https://img.shields.io/badge/PostgreSQL-Supported-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
    <img src="https://img.shields.io/badge/Cloudinary-Media-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white" alt="Cloudinary" />
    <img src="https://img.shields.io/badge/WeasyPrint-PDF-1F2937?style=for-the-badge" alt="WeasyPrint" />
  </p>
</div>

<p align="center">
  <img src="https://placehold.co/1200x420/0f172a/f8fafc?text=Project+Banner+%2F+Dashboard+Preview" alt="Project banner placeholder" />
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#highlights">Highlights</a> •
  <a href="#screenshots">Screenshots</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#project-structure">Project Structure</a>
</p>

---

## Overview

`AlMethaq System` is a Django-based platform built for managing educational operations across dashboards, authentication flows, student activity, reports, and media-rich learning experiences.

This README is intentionally designed as a polished base template, so you can replace the placeholders with your final branding, screenshots, links, and product details.

> Replace the project name, banner, links, and section content as needed.

---

## Highlights

- Centralized admin and dashboard management
- Authentication flows for platform users
- Student, teacher, course, and media management
- Annual and monthly reports with PDF export support
- Real-time features using Django Channels
- Cloud media support through Cloudinary
- API endpoints for student-facing experiences
- Static/media handling for local and deployment environments

---

## Screenshots

<table>
  <tr>
    <td align="center">
      <img alt="Screenshot from 2026-04-13 23-22-29" src="https://github.com/user-attachments/assets/8ce1b2ab-8893-4e49-8f53-a1652b839152" />
      <br />
      <sub>Dashboard overview</sub>
    </td>
    <td align="center">
      <img src="https://placehold.co/560x320/e2e8f0/0f172a?text=Reports+Page" alt="Reports screenshot placeholder" />
      <br />
      <sub>Reports and analytics</sub>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://placehold.co/560x320/e2e8f0/0f172a?text=Students+Management" alt="Students management screenshot placeholder" />
      <br />
      <sub>Student management</sub>
    </td>
    <td align="center">
      <img src="https://placehold.co/560x320/e2e8f0/0f172a?text=Mobile+or+Portal+View" alt="Portal screenshot placeholder" />
      <br />
      <sub>Portal or mobile experience</sub>
    </td>
  </tr>
</table>

### Image Setup

Replace remote placeholders with your own assets, for example:

```md
<img src="./docs/images/banner.png" alt="Project banner" />
<img src="./docs/images/dashboard-home.png" alt="Dashboard home" />
```

If you want cleaner repository organization, place images in:

```text
docs/
  images/
    banner.png
    dashboard-home.png
    reports.png
```

---

## Tech Stack

| Layer | Tools |
|---|---|
| Backend | Django 6, Python |
| Realtime | Django Channels |
| Database | SQLite / PostgreSQL |
| Media | Cloudinary, Pillow |
| PDF / Reports | WeasyPrint, html2canvas |
| Deployment | Gunicorn, WhiteNoise, Vercel-compatible settings |
| Integrations | Telethon, WhatsApp-related workflow support |

---

## Main Modules

| Module | Purpose |
|---|---|
| `dashboardApp/` | Core system logic for dashboards, students, teachers, reports, courses, and media |
| `authentacationsApp/` | Login and authentication views |
| `customizationApp/` | Custom pages and UI extensions |
| `system/` | Project settings, routing, middleware, and shared config |
| `templates/` | Dashboard, auth, reports, portal, certificate, and shared templates |
| `student_app/` | Companion Flutter application |

---

## Getting Started

### 1. Clone the project

```bash
git clone <your-repository-url>
cd system
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Create your environment file

```bash
cp .env.example .env
```

If you do not have an `.env.example` yet, create `.env` manually and add your project values.

### 5. Apply migrations

```bash
python manage.py migrate
```

### 6. Run the development server

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000/` in your browser.

---

## Environment Variables

Add the variables your setup needs inside `.env`.

```env
DEBUG=True
DJANGO_SECRET_KEY=your-secret-key
ALLOWED_HOSTS=127.0.0.1,localhost
CSRF_TRUSTED_ORIGINS=http://127.0.0.1:8000,http://localhost:8000

DATABASE_URL=
SQLITE_PATH=

CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

DAILY_API_KEY=
DAILY_DOMAIN=

WHATSAPP_PHONE_NUMBER_ID=
WHATSAPP_ACCESS_TOKEN=
WHATSAPP_AUTOSEND_ENABLED=True
AUTOMATION_WEBHOOK_TOKEN=
```

> Keep secrets out of the repository and rotate any exposed credentials before production use.

---

## Project Structure

```text
system/
├── authentacationsApp/
├── customizationApp/
├── dashboardApp/
├── docker/
├── media/
├── static/
├── staticfiles/
├── student_app/
├── system/
├── templates/
├── requirements.txt
├── runserver.sh
└── README.md
```

---

## Features You Can Describe Here

Use this section to add your final product story:

- Who the system is for
- What problem it solves
- Key workflows for admins, teachers, students, or guardians
- Why your implementation is different
- Deployment or hosting notes

Suggested paragraph:

> This platform helps educational teams manage day-to-day operations through a centralized dashboard, structured reporting, media delivery, and user-specific access flows. It is designed to support both internal administration and student-facing experiences in a single system.

---

## Deployment Notes

You can later expand this section with:

- Production server setup
- PostgreSQL configuration
- Static and media storage strategy
- Cloudinary configuration
- Gunicorn startup command
- Reverse proxy or domain setup
- Vercel or other hosting notes

Example run command:

```bash
gunicorn system.wsgi:application
```

---

## Roadmap

- Improve automated test coverage
- Expand API documentation
- Add production-ready environment examples
- Add architecture diagrams
- Add final screenshots and branded assets

---

## Contributing

If you plan to accept contributions, replace this text with your workflow:

```bash
git checkout -b feature/your-feature-name
git commit -m "Add your feature"
git push origin feature/your-feature-name
```

Then open a pull request with a clear description of the change.

---

## License

Choose the license you want to publish under.

```text
MIT License
```

Or replace this section with your preferred license text and file reference.

