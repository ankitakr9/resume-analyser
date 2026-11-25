# 📄 Resume Analyzer

[![Live App](https://img.shields.io/badge/Live-App-brightgreen)](https://resume-analyser-kp0f.onrender.com/)

## 🚀 Description

Resume Analyzer is a full-stack web application that uses Artificial Intelligence to analyze resumes and provide meaningful insights, including skill extraction, resume evaluation, and improvement suggestions.

The application integrates **Google Gemini AI** for intelligent resume analysis and provides secure authentication features such as email verification and password reset using **Brevo**. It also offers relevant job suggestions through the **Adzuna API**.

🌐 **Live Application:** https://resume-analyser-kp0f.onrender.com/

## 🛠️ Tech Stack

**Frontend**

- React.js
- HTML5
- CSS3
- JavaScript

**Backend**

- Java
- Spring Boot
- Spring Security
- JWT Authentication
- Maven

**Database**

- MySQL

**APIs & Integrations**

- Google Gemini AI
- Google OAuth2
- Brevo Email API
- Adzuna Job Search API

## 📸 Project Preview

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/df7bb0c1-1f10-478d-b8c9-c2b1bf2369f4" />
  <img width="30%" src="https://github.com/user-attachments/assets/1c65a0cc-c915-4103-a7fe-30a975639ab0" />
  <img width="30%" src="https://github.com/user-attachments/assets/b8ca21ad-7c2f-470d-ad5d-73119b8fd9f1" />
</p>

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/3f945bf1-84dd-4052-9c65-709f512ae0a4" />
  <img width="30%" src="https://github.com/user-attachments/assets/d04af8b7-4e12-4948-94c6-3b1f15340180" />
  <img width="30%" src="https://github.com/user-attachments/assets/a0c6f513-2108-41c8-98b5-91e86d27d398" />
</p>

## 🔗 Frontend & Backend Integration

- The frontend is developed using React.js.
- The React application is built and served by the Spring Boot backend.
- Production build files are placed inside the backend's `static` directory.
- Spring Boot serves the frontend when the application runs.

### Static & Template Files

- The `static` folder contains React production build files.
- The `templates` folder contains email templates.
- Email templates are used for email verification and password reset functionality.

## ⚙️ How to Run the Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/ankitakr9/resume-analyser.git
```

### 2. Open the Project in an IDE

Open the project using IntelliJ IDEA or Eclipse.

- Import the project as a Maven project.
- Open `pom.xml`.
- Allow Maven to download the required dependencies.

### 3. Configure Application Credentials

Update `src/main/resources/application.properties` with your own credentials.

**Database Configuration (MySQL)**

```properties
spring.datasource.url=your_DB_URL
spring.datasource.username=your_DB_USERNAME
spring.datasource.password=your_DB_PASSWORD
```

**Google OAuth2 Configuration**

```properties
spring.security.oauth2.client.registration.google.client-id=your_GCP_ID
spring.security.oauth2.client.registration.google.client-secret=your_GCP_SECRET
```

**Google Gemini AI Configuration**

```properties
genKey=your_GEMINI_API_KEY
```

**Brevo Email Configuration**

```properties
apiKey=your_BREVO_MAIL_API
```

**Adzuna Job Search Configuration**

```properties
application-id=your_ADZUNA_APP_ID
application-api-key=your_ADZUNA_API_KEY
```

**JWT Configuration**

```properties
jwt-key=your_OWN_SECRET_KEY
```

Generate a secure JWT secret and configure it in your environment.

⚠️ Never commit actual API keys, database passwords, OAuth secrets, or JWT secrets to GitHub.

### 4. Run the Backend

Run the main Spring Boot application:

```text
ResumeAnalyserApplication.java
```

### 5. Open the Application

Visit:

```text
http://localhost:8080/
```

## 📝 Important Notes

- This project is currently configured to use Google Gemini AI.
- To integrate another AI provider, update the AI-related implementation in `appService.java`.
- Email functionality is configured to work with the Brevo API.
- To use another email provider, update the mail service implementation.
- If the configured Gemini model becomes unavailable, update the model configuration accordingly.

## 🎨 Modifying the Frontend UI

Do not directly modify the production files inside the backend's `static` directory.

### 1. Run Frontend in Development Mode

```bash
cd "frontend src"
npm install
npm run dev
```

This starts the React development server.

### 2. Build Frontend for Backend Deployment

```bash
cd "frontend src"
npm run build
```

### 3. Copy Production Build Files

After building the frontend, copy the contents of the `dist` folder into the backend's `static` directory.

Expected structure:

```text
static/
├── assets/
│   ├── *.css
│   └── *.js
└── index.html
```

Remove outdated build assets before copying the new ones.

## ⚠️ Disclaimer

- This project is developed for learning and demonstration purposes.
- AI-generated resume analysis results may vary.
- The suggestions provided by this application should not be considered professional career advice.

---

**Developed and maintained by Ankita Kumari**

GitHub: [@ankitakr9](https://github.com/ankitakr9)
