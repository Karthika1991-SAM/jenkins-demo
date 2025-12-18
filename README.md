# Jenkins CI Setup with GitHub & Email Notification

## 📌 Project Overview

This project demonstrates a **Continuous Integration (CI)** setup using **Jenkins**, **GitHub**, and **AWS EC2**. Whenever a commit is pushed to the GitHub repository, Jenkins automatically triggers a build and sends the build result to the configured email address.

This setup is commonly used in real-world DevOps workflows to ensure automation, faster feedback, and reliable builds.

---

## 🛠 Tech Stack Used

* **AWS EC2** – Hosting Jenkins server
* **Jenkins** – CI automation tool
* **GitHub** – Source code repository
* **Gmail SMTP** – Email notifications
* **Ubuntu 20.04** – Operating system

---

## 📂 Repository Structure

```
jenkins-demo/
│── build.sh
│── README.md
```

---

## ⚙️ Jenkins Workflow

1. Developer pushes code to GitHub
2. GitHub webhook notifies Jenkins
3. Jenkins pulls latest code
4. Jenkins executes `build.sh`
5. Build status is generated
6. Email notification is sent automatically

---

## 📜 build.sh Script (Summary)

The `build.sh` script performs:

* Workspace validation
* System environment checks
* Dependency simulation
* Code quality verification
* Unit test simulation
* Artifact generation
* Build logging

The script is designed to fail the build if any step fails.

---

## 🔔 Email Notification Setup

Email notifications are configured using:

* **SMTP Server:** smtp.gmail.com
* **Port:** 587
* **Authentication:** Gmail App Password
* **Protocol:** TLS

Emails are sent automatically after each build with:

* Build status
* Job name
* Build number
* Build URL
* Attached build logs (optional)

---

## 🚀 How to Run the Project

### 1️⃣ Clone Repository

```bash
git clone https://github.com/<your-username>/jenkins-demo.git
cd jenkins-demo
```

### 2️⃣ Make Script Executable

```bash
chmod +x build.sh
```

### 3️⃣ Configure Jenkins Job

* Create a **Freestyle Project**
* Connect GitHub repository
* Enable **GitHub hook trigger for SCM polling**
* Add **Execute shell** build step:

```bash
./build.sh
```

---

## 🧪 Testing CI Automation

Make a new commit:

```bash
echo "Trigger CI build" >> test.txt
git add .
git commit -m "Test Jenkins CI"
git push
```

✔ Jenkins build triggers automatically
✔ Email notification is sent

---

## ✅ Expected Outcome

* Automatic build on every GitHub commit
* Professional build logs
* Email notification on build completion
* CI pipeline successfully implemented

---

## 📌 Conclusion

This project demonstrates a complete CI workflow using Jenkins and GitHub. It showcases essential DevOps skills including automation, integration, and monitoring through email alerts.

---

## 👩‍💻 Author

**Karthika**
Aspiring DevOps Engineer

---

⭐ If you found this useful, feel free to fork or star the repository!
