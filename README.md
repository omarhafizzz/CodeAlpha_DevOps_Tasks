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
