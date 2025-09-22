# DevOps Portal – Maven & Tomcat Deployment Demo

This repository contains a simple yet structured **Java Web Module** designed to demonstrate a complete **build and deploy workflow** using **Maven**, **EC2 instances**, and **Tomcat**.  

While the project itself is minimal, the focus lies on showing how to integrate core DevOps practices such as **code organization**, **artifact building**, **deployment pipelines**, and **environment setup**.



## ✨ Project Overview
- **Backend Logic**: Java service class (`EmployeeService.java`) inside a proper package structure.  
- **Frontend Presentation**:  
  - `home.jsp` (main JSP page) containing HTML, CSS, and JS references.  
  - Segregated assets: `style.css` for styling and `main.js` for interactivity.  
- **Configuration Files**:  
  - `web.xml` and `kk-servlet.xml` for servlet configuration.  
- **Build Management**: `pom.xml` handled with **Maven**.  
- **Deployment Target**: Apache Tomcat server hosted on an **EC2 instance**.  



## 🚀 Deployment Workflow
1. **Maven Build Instance**  
   - Code is compiled and packaged into a `.war` file using **Maven Auto Build Tool**.  

2. **Artifact Transfer**  
   - `.war` file is securely copied (`scp`) first to the local machine, then moved to the **Tomcat instance**.  

3. **Tomcat Deployment**  
   - Deployed the `.war` file under the `webapps` directory.  
   - Application accessed on multiple ports (`8080` and `8010`) to demonstrate handling **port conflicts**.  

4. **Result**  
   - The application renders `home.jsp` which pulls in `style.css` and `main.js` for a clean, modular structure.  

---

## 🗂 Project Structure

```plaintext
src
└── main
    ├── java
    │   └── com
    │       └── kk
    │           └── services
    │               └── EmployeeService.java
    └── webapp
        ├── WEB-INF
        │   ├── kk-servlet.xml
        │   └── web.xml
        ├── css
        │   └── style.css
        ├── js
        │   └── main.js
        └── jsps
            └── home.jsp
pom.xml
.gitignore

```

---

## ⚡ Key Highlights
- **Separation of Concerns**: Even though `home.jsp` holds the primary UI code, styles and scripts are cleanly modularized.  
- **Practical Deployment**: Shows real-world flow from Maven build → artifact transfer → Tomcat deployment.  
- **EC2 Demonstration**: Uses two different EC2 instances to mimic a build-and-deploy architecture.  
- **Port Conflict Handling**: Dual deployment on `8080` and `8010` for demonstration.  



## 🔧 Tech Stack
- **Java (JSP/Servlets)**  
- **Maven** (build automation & dependency management)  
- **Apache Tomcat** (application server)  
- **AWS EC2** (infrastructure)  



## 🎯 Learning Outcomes
- Understanding how to **package Java projects with Maven**.  
- Gaining hands-on with **artifact transfer across environments**.  
- Practical exposure to **Tomcat deployments on EC2 via inbound rules**.  
- Awareness of **basic BruteForce Deployment patterns**.  



## 🙌 Closing Note
This project is intentionally kept lightweight in scope to demonstrate the **Maven and Tomcat Dynamic web Deployments**.  
As a DevOps Aspirant, the goal is to **showcase adaptability, curiosity, and a hands-on approach** without exaggeration.  

---





















