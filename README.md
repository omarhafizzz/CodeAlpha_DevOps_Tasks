# 🚀 CodeAlpha DevOps Internship Tasks

This repository contains the implementation of my DevOps tasks for the CodeAlpha internship, including Jenkins Remoting, CI/CD pipelines, and Docker containerization.

---

## ✅ TASK 2: Jenkins Remoting Project (Completed)

**Objective:** Set up Jenkins Remoting to connect remote Jenkins nodes, distribute build loads securely, and improve security using node isolation.

### 🛠️ Implementation Details:
- **Master Node (Controller):** Ubuntu Machine running Jenkins.
- **Agent Node:** Kali Linux Machine.
- **Connection Method:** SSH with dedicated credentials to ensure secure distribution of workloads.
- **Security & Least Privilege:** Created a dedicated `jenkins` user on the Agent node with limited permissions to prevent root access vulnerabilities.

### 🔒 Node Isolation & Architecture:
To ensure jobs run only on specific architectures and to improve security, **Node Isolation** was implemented using Jenkins Labels.
- The Kali agent was assigned the label: `linux-agent`.
- Build loads can now be distributed to run specifically on this remote Linux architecture.

### 📸 Proof of Completion:
I have successfully connected the agent. Please check the uploaded screenshots in this repository demonstrating:
1. The remote node successfully connected and online.
2. The specific Node Isolation label configuration.
3. The connection logs confirming SSH authentication.

## ✅ TASK 3: Java Application using Gradle (Completed)

**Objective:** Automate Java project builds using Gradle, manage dependencies, and integrate CI/CD pipelines for continuous delivery.

### 🛠️ Implementation Details:
- **Application:** Created a custom Java application.
- **Build Tool:** Configured **Gradle** (`build.gradle`) to manage dependencies (JUnit) and automate the build process.
- **CI/CD Pipeline:** Developed a declarative `Jenkinsfile` to orchestrate the entire workflow.
- **Integration with Task 2:** Successfully linked the pipeline to execute exclusively on the remote Kali agent using the `label 'linux-agent'` directive.

### 🔄 Pipeline Stages Executed:
1. **Checkout Code:** SCM pulled the source code from this GitHub repository.
2. **Provisioning:** Automated the download and setup of the Gradle tool directly within the workspace.
3. **Build:** Compiled the Java code using `gradle build`.
4. **Test & Run:** Executed tests and ran the compiled application, successfully outputting the application logs to the Jenkins console.

### 📸 Proof of Completion:
The complete source code is available in the `Task3_Java_Gradle` directory of this repository. Please check the uploaded screenshots demonstrating the successful Jenkins pipeline execution and console output.

## ✅ TASK 4: Web Server using Docker (Completed)

**Objective:** Learn Docker containerization basics, deploy and manage a web server inside Docker containers, and understand container lifecycle commands.

### 🛠️ Implementation Details:
- **Containerization:** Created a custom `Dockerfile` using `nginx:alpine` as the base image for a lightweight, secure web server.
- **Deployment:** Deployed a custom HTML page into the Nginx default hosting directory.
- **Lifecycle Commands:** 
  - Used `docker build -t` to create the custom image.
  - Used `docker run -d -p 9090:80` to start the container in detached mode and map the host port to the container port.
- **Monitoring & Troubleshooting:** Utilized `docker ps` and `docker stats` to monitor container health, verify uptime, and ensure optimal resource usage.

### 📸 Proof of Completion:
The `Dockerfile` and `index.html` source code are located in the `Task4_Docker` directory of this repository. Uploaded screenshots demonstrate the running container (`docker ps` output) and the successfully accessed web page via the browser on port 9090.
