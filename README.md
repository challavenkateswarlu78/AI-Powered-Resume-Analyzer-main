# 🤖 AI-Powered Resume Analyzer

An intelligent full-stack web application that helps users analyze resumes, manage their profiles, and explore relevant job opportunities through an integrated modern web interface.

The application combines a **React.js frontend** with a **Java Spring Boot backend**, authentication, resume processing, email-based verification, and job-search functionality.

---

## 📌 Overview

Finding suitable jobs can be difficult when a resume does not clearly match the skills and requirements expected by employers.

The **AI-Powered Resume Analyzer** is designed to help users understand their resume and improve their job-search process through an integrated platform.

### The application provides:

- 👤 User registration and login
- 🔐 Secure authentication using JWT
- 📧 Email OTP verification
- 🔑 Password reset using OTP
- 📄 Resume upload and analysis
- 📊 Resume analysis results
- 💼 Job-search functionality
- 🏢 Company and job information
- 🔎 Location and category-based job information
- 🌐 React-based responsive frontend
- ⚙️ Spring Boot REST backend

---

## ✨ Key Features

### 👤 User Authentication

- User registration
- User login
- JWT-based authentication
- Protected backend endpoints
- Authentication and authorization handling

### 📧 Email Verification

The application supports email-based verification using OTPs.

Users can:

1. Register an account
2. Receive an OTP
3. Verify their email
4. Continue using the application

---

### 🔑 Password Reset

Users can recover their account through an OTP-based password reset flow.

The process includes:

```text
Forgot Password
       ↓
Enter Email
       ↓
OTP Sent
       ↓
Verify OTP
       ↓
Create New Password
       ↓
Login
```

---

### 📄 Resume Analysis

Users can upload their resumes through the React frontend.

The application processes the uploaded resume and provides analysis results through the backend.

The frontend contains dedicated functionality for:

- Resume upload
- Resume analysis
- Analysis results
- User interaction with the analysis page

---

### 💼 Job Search

The backend contains models and services for working with job-search information, including:

- Jobs
- Companies
- Categories
- Locations
- Job-search responses

This allows the application to combine resume-related information with job-search functionality.

---

### 🌐 Frontend

The frontend is built using **React.js** and **Vite**.

The application contains pages/components for:

- Home
- Login
- Resume analysis
- Resume upload
- Password reset
- Google authentication
- Application context/state management

---

## 🏗️ System Architecture

```text
                    ┌───────────────────────┐
                    │       User            │
                    │     Web Browser       │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌───────────────────────┐
                    │     React.js + Vite   │
                    │       Frontend        │
                    └───────────┬───────────┘
                                │
                         HTTP / REST API
                                │
                                ▼
                    ┌───────────────────────┐
                    │     Spring Boot       │
                    │       Backend         │
                    ├───────────────────────┤
                    │ Controllers           │
                    │ Services              │
                    │ Security              │
                    │ JWT                    │
                    │ Resume Processing     │
                    │ Job Search            │
                    │ Email / OTP           │
                    └───────────┬───────────┘
                                │
              ┌─────────────────┼─────────────────┐
              ▼                 ▼                 ▼
        Authentication     Email Service      Job Data
```

---

## 🛠️ Technology Stack

### Frontend

| Technology | Purpose |
|---|---|
| React.js | User interface |
| Vite | Frontend development/build tool |
| JavaScript | Application logic |
| CSS | Styling |
| CSS Modules | Component-level styling |
| ESLint | Code quality |

### Backend

| Technology | Purpose |
|---|---|
| Java | Backend programming language |
| Spring Boot | Backend framework |
| Spring Security | Application security |
| JWT | Authentication |
| Maven | Dependency management |
| REST API | Frontend-backend communication |

### Development Tools

| Tool | Purpose |
|---|---|
| Git | Version control |
| GitHub | Source-code hosting |
| IntelliJ IDEA | Backend development |
| VS Code | Frontend development |
| Postman | API testing |
| Docker | Containerization |

---

## 📁 Project Structure

```text
AI-Powered-Resume-Analyzer-main/
│
├── frontend src/
│   ├── src/
│   │   ├── analyse/
│   │   ├── home/
│   │   ├── login/
│   │   ├── resetpassword/
│   │   ├── upload/
│   │   │
│   │   ├── App.jsx
│   │   ├── appcontext.jsx
│   │   ├── googlebtn.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── package.json
│   ├── package-lock.json
│   ├── vite.config.js
│   └── index.html
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/ai/Resume/analyser/
│   │   │       ├── configuration/
│   │   │       ├── controller/
│   │   │       ├── jwt/
│   │   │       ├── mail/
│   │   │       ├── model/
│   │   │       ├── repository/
│   │   │       ├── service/
│   │   │       └── ResumeAnalyserApplication.java
│   │   │
│   │   └── resources/
│   │       ├── static/
│   │       ├── templates/
│   │       └── application.properties
│   │
│   └── test/
│
├── .gitignore
├── Dockerfile
├── pom.xml
├── mvnw
├── mvnw.cmd
├── render.yaml
└── README.md
```

---

# 🚀 Getting Started

## Prerequisites

Make sure the following are installed:

- Java JDK
- Maven
- Node.js
- npm
- Git
- A Java IDE such as IntelliJ IDEA
- VS Code for frontend development

---

## 1. Clone the Repository

```bash
git clone https://github.com/challavenkateswarlu78/AI-Powered-Resume-Analyzer-main.git
```

Move into the project:

```bash
cd AI-Powered-Resume-Analyzer-main
```

---

# ⚙️ Backend Setup

The backend is a Spring Boot application.

Navigate to the project root and run:

### Windows

```powershell
.\mvnw.cmd spring-boot:run
```

### Linux / macOS

```bash
./mvnw spring-boot:run
```

The backend will start using the Spring Boot configuration.

---

# 🌐 Frontend Setup

Open another terminal.

Navigate to the frontend:

```bash
cd "frontend src"
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Vite will provide the local development URL in the terminal.

---

# 🔐 Environment Configuration

**Never commit API keys, passwords, OAuth secrets, email credentials, JWT secrets, or other sensitive credentials to GitHub.**

Create your local configuration using environment variables.

For example:

```text
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
SENDINBLUE_API_KEY=your_email_api_key
```

Use environment variables from the application instead of hardcoding credentials in Java source code.

### Important

Do not upload:

```text
.env
application-local.properties
```

to GitHub.

These files should remain in `.gitignore`.

---

# 🔒 Security

The application includes security functionality based on:

- Spring Security
- JWT authentication
- Authentication filters
- Protected endpoints
- OTP-based verification
- Password-reset verification

The authentication flow can be represented as:

```text
             User
               │
               ▼
          Registration
               │
               ▼
         Email Verification
               │
               ▼
             Login
               │
               ▼
         JWT Token Issued
               │
               ▼
       Authenticated Requests
               │
               ▼
          Protected APIs
```

---

# 📄 Resume Analysis Flow

```text
User
 │
 ▼
Login / Register
 │
 ▼
Upload Resume
 │
 ▼
Frontend sends request
 │
 ▼
Spring Boot Backend
 │
 ▼
Resume Processing
 │
 ▼
Analysis
 │
 ▼
Results
 │
 ▼
React Analysis Page
```

---

# 💼 Job Search Flow

```text
User
 │
 ▼
Search / Resume Information
 │
 ▼
Spring Boot Backend
 │
 ▼
Job Search Service
 │
 ├── Job
 ├── Company
 ├── Category
 └── Location
 │
 ▼
Job Search Response
 │
 ▼
React Frontend
```

---

# 🧪 Testing

The project includes Spring Boot test infrastructure.

Run backend tests using:

```powershell
.\mvnw.cmd test
```

You can also test REST APIs using tools such as **Postman**.

---

# 🐳 Docker

The project includes a `Dockerfile`, allowing the application to be containerized.

Build the Docker image:

```bash
docker build -t ai-resume-analyzer .
```

Run the container:

```bash
docker run -p 8080:8080 ai-resume-analyzer
```

> Make sure required environment variables and external services are configured before running the application in Docker.

---

# 📱 Application Pages

The frontend currently contains functionality for pages/components including:

| Page | Purpose |
|---|---|
| 🏠 Home | Main application interface |
| 🔐 Login | User authentication |
| 📝 Registration | Create a user account |
| 📤 Upload Resume | Upload a resume |
| 🤖 Analyze Resume | Process and analyze resume |
| 📊 Analysis | Display analysis results |
| 🔑 Reset Password | Password recovery |
| 📧 OTP Verification | Verify user identity |
| 🔵 Google Authentication | Google-based authentication |

---

# 🔮 Future Improvements

Potential improvements for future versions include:

- 📊 Advanced resume scoring
- 🎯 Job recommendation based on resume skills
- 🧠 Improved AI-based resume analysis
- 📈 Resume improvement recommendations
- 📝 Automatic resume suggestions
- 🔍 Advanced job filtering
- 📊 Skill-gap analysis
- 💼 Personalized job recommendations
- 📱 Improved mobile responsiveness
- ☁️ Production cloud deployment
- 🧪 Expanded automated testing
- 🔄 CI/CD pipeline
- 📊 Analytics dashboard

---

# 🎯 Project Goals

The main goals of this project are to:

1. Build a practical full-stack application.
2. Understand React and Spring Boot integration.
3. Implement secure user authentication.
4. Build RESTful backend services.
5. Process and analyze resume information.
6. Integrate job-search functionality.
7. Practice modern software development and deployment workflows.

---

# 👨‍💻 Author

**Venkateswarlu Challa**

GitHub:  
https://github.com/challavenkateswarlu78

---

# 📄 License

This project is intended for educational and development purposes.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Contributions, suggestions, and improvements are welcome.

## 🔐 Environment Variables

Before running the backend, configure the required environment variables in PowerShell.

```powershell
$env:SPRING_DATASOURCE_URL="jdbc:postgresql://localhost:5432/resume_analyser"
$env:SPRING_DATASOURCE_USERNAME="postgres"
$env:SPRING_DATASOURCE_PASSWORD="YOUR_POSTGRES_PASSWORD"

$env:JWT_SECRET="YOUR_JWT_SECRET"

$env:GEMINI_API_KEY="YOUR_GEMINI_API_KEY"

$env:BREVO_API_KEY="YOUR_BREVO_API_KEY"

$env:GOOGLE_CLIENT_ID="YOUR_GOOGLE_CLIENT_ID"
$env:GOOGLE_CLIENT_SECRET="YOUR_GOOGLE_CLIENT_SECRET"

$env:ADZUNA_APP_ID="YOUR_ADZUNA_APP_ID"
$env:ADZUNA_API_KEY="YOUR_ADZUNA_API_KEY"

Verify the keys
Write-Host "DB URL set:" ([bool]$env:SPRING_DATASOURCE_URL)
Write-Host "DB username set:" ([bool]$env:SPRING_DATASOURCE_USERNAME)
Write-Host "DB password set:" ([bool]$env:SPRING_DATASOURCE_PASSWORD)
Write-Host "JWT secret set:" ([bool]$env:JWT_SECRET)
Write-Host "Gemini key set:" ([bool]$env:GEMINI_API_KEY)
Write-Host "Brevo key set:" ([bool]$env:BREVO_API_KEY)
Write-Host "Google Client ID set:" ([bool]$env:GOOGLE_CLIENT_ID)
Write-Host "Google Client Secret set:" ([bool]$env:GOOGLE_CLIENT_SECRET)
Write-Host "Adzuna App ID set:" ([bool]$env:ADZUNA_APP_ID)
Write-Host "Adzuna API key set:" ([bool]$env:ADZUNA_API_KEY)

Run the backend
.\mvnw.cmd -version
.\mvnw.cmd spring-boot:run

Important: Replace the YOUR_... values with your own credentials locally. Never commit real API keys, passwords, JWT secrets, or OAuth secrets to GitHub.
