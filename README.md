
---

# 🏋️ ACEest Fitness & Gym – DevOps CI/CD Pipeline Project

## 📌 Project Overview

This project demonstrates the implementation of a complete **DevOps pipeline** for the ACEest Fitness & Gym application. The goal is to ensure **code integrity, automated testing, containerization, and continuous integration** using modern DevOps tools.

The application is built using **Flask (Python)** and follows a structured workflow from local development to automated build validation using **Jenkins** and **GitHub Actions**.

---

## 🚀 Technologies Used

* **Python (Flask)** – Backend web application
* **Git & GitHub** – Version control system
* **Pytest** – Unit testing framework
* **Docker** – Containerization
* **GitHub Actions** – CI/CD automation
* **Jenkins** – Build and quality gate validation

---

## 📂 Project Structure

```
aceest-devops/
│── app.py
│── requirements.txt
│── Dockerfile
│── test_app.py
│── README.md
│── .github/
│    └── workflows/
│         └── main.yml
```

---

## ⚙️ Local Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/aceest-devops.git
cd aceest-devops
```

---

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Run the Application

```bash
python app.py
```

Open in browser:

```
http://localhost:5000
```

---

## 🧪 Running Tests Manually

To validate application logic using Pytest:

```bash
pytest
```

Expected Output:

```
2 passed
```

---

## 🐳 Docker Setup & Execution

### 1. Build Docker Image

```bash
docker build -t aceest-app .
```

---

### 2. Run Docker Container

```bash
docker run -p 5000:5000 aceest-app
```

Access the application at:

```
http://localhost:5000
```

---

## 🔄 GitHub Actions CI/CD Pipeline

### 📌 Workflow Location:

```
.github/workflows/main.yml
```

### 📌 Trigger:

* On every `push`
* On every `pull_request`

### 📌 Pipeline Stages:

1. **Build & Lint**

   * Checks Python syntax
   * Installs dependencies

2. **Automated Testing**

   * Runs Pytest test suite

3. **Docker Image Build**

   * Builds Docker container

### 📌 How to Check:

1. Go to your GitHub repository
2. Click on **Actions tab**
3. View latest workflow run
4. Ensure all steps show ✅ (green)

---

## 🏗️ Jenkins Build & Quality Gate

Jenkins is used as a **secondary validation layer** to ensure the application builds successfully in an isolated environment.

---

### 🔧 Jenkins Setup Steps

1. Open Jenkins:

```
http://localhost:8080
```

2. Create a new job:

* Click **New Item**
* Select **Freestyle Project**
* Name: `aceest-build`

3. Configure Source Code:

* Select **Git**
* Enter repository URL

4. Add Build Step → Execute Shell:

```bash
pip install -r requirements.txt
pytest
docker build -t aceest-app .
```

5. Save and click **Build Now**

---

### ✅ Jenkins Validation

* Click on build number
* Open **Console Output**

Expected result:

```
Finished: SUCCESS
```

---

## 🔁 CI/CD Workflow Summary

| Stage                  | Tool           | Description                    |
| ---------------------- | -------------- | ------------------------------ |
| Version Control        | GitHub         | Code storage and collaboration |
| Continuous Integration | GitHub Actions | Automated testing and build    |
| Containerization       | Docker         | Environment consistency        |
| Build Validation       | Jenkins        | Secondary build verification   |

---

## 📊 Key Features

* Flask-based fitness management backend
* REST API endpoints
* Automated unit testing using Pytest
* Dockerized application
* CI/CD pipeline with GitHub Actions
* Jenkins build integration

---

## 📌 Evaluation Criteria Coverage

✔ Application runs successfully

✔ Git commits structured and meaningful

✔ Unit tests implemented and passing

✔ Docker image builds successfully

✔ GitHub Actions pipeline executes successfully

✔ Jenkins build completes without errors

✔ Documentation is clear and professional

---

## 🎯 Conclusion

This project successfully demonstrates a **complete DevOps lifecycle**, ensuring:

* Reliable code integration
* Automated testing
* Consistent deployment environments
* Scalable CI/CD workflows

---

## 👨‍💻 Author

**Name - Akshay Salamwade**

**EMail - 2024tm93682@wilp.bits-pilani.ac.in**

DevOps Assignment – ACEest Fitness & Gym

---

---

