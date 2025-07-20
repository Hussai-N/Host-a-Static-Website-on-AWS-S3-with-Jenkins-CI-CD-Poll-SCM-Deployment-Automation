# Host-a-Static-Website-on-AWS-S3-with-Jenkins-CI-CD-Poll-SCM-Deployment-Automation

This project demonstrates how to automate the deployment of a static HTML website using **Jenkins** integrated with **GitHub**. The Jenkins server watches for changes in the GitHub repository and automatically deploys the updated website whenever a new push is made to the `main` branch.

---

## 📂 Project Structure

cloud_diaries/
├── index.html # Static HTML homepage
├── Jenkinsfile # Jenkins pipeline script (optional for scripted pipeline)
└── other files... # Any additional static assets

yaml
Copy
Edit

---

## 🛠️ Tools & Technologies Used

- **Jenkins** – Automation server for building and deploying
- **GitHub** – Source code hosting and version control
- **Poll SCM** – For detecting changes in the GitHub repository
- **HTML/CSS** – Static website content

---

## 🔁 Workflow Overview

1. GitHub repository is configured and contains your static website.
2. Jenkins is set up on your machine/server.
3. Jenkins job is created with **Poll SCM** configured (e.g., `* * * * *` for every minute).
4. When changes are pushed to the `main` branch, Jenkins automatically pulls and deploys the site.
5. Site is hosted locally or on a web server.

---

## 🧪 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Hussai-N/sample.git
Install Jenkins and set up a new freestyle project.

Configure the GitHub repo in Jenkins under Source Code Management.

Under Build Triggers, enable Poll SCM and set the schedule.

Add build steps to:

Pull the latest code

Copy files to your desired deployment directory (e.g., /var/www/html/)
