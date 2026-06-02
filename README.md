# CST8919 Lab 1 - Auth0 Flask Authentication

## Overview

This project demonstrates authentication and authorization in a Flask web application using Auth0.

The application allows users to:

* Login using Auth0 authentication
* Access a protected route only when authenticated
* Logout securely
* Redirect unauthorized users to the login page

---

# Features

* Flask web application
* Auth0 authentication integration
* Protected route implementation
* User session handling
* Secure environment variable configuration

---

# Technologies Used

* Python
* Flask
* Auth0
* Hypercorn
* HTML
* dotenv

---

# Project Structure

```text
auth0-flask-app/
│
├── app.py
├── auth.py
├── requirements.txt
├── .env
├── .gitignore
│
├── templates/
│   ├── index.html
│   ├── profile.html
│   └── protected.html
│
└── static/
    └── style.css
```

---

# Setup Instructions

## 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
cd auth0-flask-app
```

---

## 2. Create Virtual Environment

### Git Bash

```bash
python -m venv venv
source venv/Scripts/activate
```

### PowerShell

```powershell
python -m venv venv
venv\Scripts\activate
```

---

## 3. Install Dependencies

```bash
python -m pip install flask python-dotenv auth0-server-python hypercorn asgiref
```

---

# Configure Auth0

Create an application in Auth0 Dashboard:

Application Type:

* Regular Web Application

---

# Configure Allowed URLs

## Allowed Callback URLs

```text
http://localhost:5000/callback
```

## Allowed Logout URLs

```text
http://localhost:5000
```

## Allowed Web Origins

```text
http://localhost:5000
```

---

# Environment Variables

Create a `.env` file in the project root.


```env
AUTH0_CLIENT_ID=YOUR_CLIENT_ID
AUTH0_CLIENT_SECRET=YOUR_CLIENT_SECRET
AUTH0_DOMAIN=YOUR_AUTH0_DOMAIN
AUTH0_SECRET=YOUR_GENERATED_SECRET
```

Generate a secure secret:

```bash
openssl rand -hex 64
```

---

# Run the Application

Run the application using Hypercorn:

```bash
python app.py
```

Application URL:

```text
http://localhost:5000
```
<img width="3072" height="1824" alt="image" src="https://github.com/user-attachments/assets/442215f8-bafe-4e4b-97e0-b16934af6548" />

<img width="3072" height="1824" alt="image" src="https://github.com/user-attachments/assets/420d7085-1503-4b15-a182-aa6902c2a9e1" />

<img width="3072" height="1824" alt="image" src="https://github.com/user-attachments/assets/038e1f58-dfbe-49b2-bce5-216eb155f7b4" />



---

# Protected Route

The application includes a protected route:

```text
/protected
```

Only authenticated users can access this route.

If a user is not authenticated, they are redirected to the login page.

---

# Demo Video

YouTube Demo Link:

[![Watch the demo](https://img.youtube.com/vi/IWf0rDtQj9A/hqdefault.jpg)](https://www.youtube.com/watch?v=IWf0rDtQj9A)

---

# GitHub Repository

Repository Link:

```text
https://github.com/saraMir26/CST8919-Lab1
```

---

# Demo Functionality

The demo video includes:

* Running the Flask application
* User login using Auth0
* Accessing the protected page
* Logout functionality
* Redirect behavior for unauthorized users
* Brief walkthrough of the project code

---

# What I Learned

Through this lab I learned:

* How authentication works using Auth0
* How OAuth callback routes work
* How to create protected routes in Flask
* How to manage user authentication sessions
* How to configure environment variables securely
* How to integrate Auth0 with Python Flask applications

---

# Important Notes

* The `.env` file is excluded from GitHub using `.gitignore`
* Secrets and credentials should never be committed to version control
