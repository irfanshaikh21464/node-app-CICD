# node-app-CICD
✨ Introduction
This repository provides a step-by-step guide to setting up a complete Continuous Integration/Continuous Deployment (CI/CD) pipeline for a simple Node.js application using GitHub, Jenkins, and AWS EC2.

🛠️ Step 1: AWS EC2 Instances Setup
You need two running EC2 instances: one for Jenkins and one for the Node.js application.

Launch Two EC2 Instances: Designate one as the Jenkins Server and the other as the Node App Server.

Verify Instances: Confirm both are running and check their Public IPs.

![AWS EC2 Instances Running](Screenshot%20(1).jpg)

💻 Step 2: GitHub Repository Preparation
Ensure your repository contains all necessary application files and the Jenkins pipeline script.

Repository Structure: Confirm the presence of app.js, package.json, and Jenkinsfile.

![GitHub Repository Files](Screenshot%20(2).jpg)

🔑 Step 3: Jenkins Configuration (The CI Engine)
Configure the Jenkins job to use your repository and define the pipeline execution.

Create Jenkins Job: Create a new Pipeline job (e.g., node-app-CICD).

Configure SCM: Set the Definition to Pipeline script from SCM and provide the Repository URL and Credentials.

![Jenkins Job Configuration](Screenshot%20(6).png)

🔗 Step 4: Connecting GitHub and Jenkins (Webhooks)
Set up the Webhook to trigger the Jenkins build automatically upon every code push.

Add Webhook: Go to Repository Settings > Webhooks.

Payload URL: Use your Jenkins URL (http://<YOUR_JENKINS_PUBLIC_IP>:8080/github-webhook/).

Trigger: Select Just the push event.

![GitHub Webhooks Settings](Screenshot%20(3).jpg)

✅ Step 5: Verifying Deployment
Verify the application is successfully deployed and running on the target server.

Access URL: http://<NODE_APP_SERVER_PUBLIC_IP>:5432

The output should confirm the latest application version.

![Deployed Application Output](Screenshot%20(8).png)
