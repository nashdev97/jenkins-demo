# Jenkins Demo CI/CD Pipeline 🚀

This repository demonstrates a basic CI/CD pipeline using **Jenkins** to clone a GitHub repo, build, test, and (optionally) deploy an application. It uses a `Jenkinsfile` written in Declarative Pipeline syntax.

## 📂 Project Structure

```bash
.
├── Jenkinsfile    # Pipeline script for Jenkins
└── README.md      # You're here!
└── app.py
└── dockerfile

📋 Jenkins Pipeline Overview

This pipeline includes the following stages:

Checkout SCM – Clones the repo from GitHub.

Build – Runs a simple build script (adjust to your needs).

Test – Placeholder for unit or integration tests.

Deploy – Placeholder for deployment steps.


🧑‍💻 Setup Instructions

1. Clone the Repository
git clone https://github.com/nashdev97/jenkins-demo.git
cd jenkins-demo

2. Jenkins Setup

Make sure you have Jenkins installed (preferably LTS version).

Install required plugins:

Pipeline

Git

Blue Ocean (optional for UI)

3. Create a New Jenkins Pipeline Job

Open Jenkins.

Create a new item → Select Pipeline → Name it jenkins-demo.

In pipeline config:

Definition: Pipeline script from SCM

SCM: Git

Repository URL: https://github.com/nashdev97/jenkins-demo.git

Branch: main

✅ Important (Windows users):

If you're running Jenkins on Windows, update the sh steps to use bat in your Jenkinsfile:
bat 'echo Building the application...'


🛠 Troubleshooting
❌ Cannot run program "sh": CreateProcess error=2

You're likely running Jenkins on Windows and using Unix shell commands (sh). Fix it by replacing sh with bat or by installing Git Bash and configuring it as the default shell.

📦 Example Jenkinsfile
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'echo Building the application...'
            }
        }
        stage('Test') {
            steps {
                bat 'echo Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo Deploying application...'
            }
        }
    }
}



🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the issues page if you want to contribute.


📸 Screenshots
Here are some screenshots demonstrating the application and CI/CD pipeline:

 <br>
<img src='./Screenshots/image.png'>
<br>
<br>
<img src='./Screenshots/image-1.png'>
<br>
<br>
<img src='./Screenshots/image-2.png'>
<br>
<br>
<img src='./Screenshots/image-3.png'>
<br>
<br>
<img src='./Screenshots/image-4.png'>
<br>
<br>
<img src='./Screenshots/image-5.png'>
<br>
<br>
<img src='./Screenshots/image-6.png'>
<br>