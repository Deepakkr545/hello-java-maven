
# Hello Java Maven – Jenkins Build Project

## 📌 Overview
This is a simple **Java Hello World application** built using **Apache Maven** and compiled via a **Jenkins Freestyle job**.  
It’s designed as a beginner-friendly project to understand **continuous integration** with Jenkins.

---

## 🛠 Tools Used
- **Java JDK 21** (installed locally)
- **Apache Maven** (installed through Jenkins)
- **Jenkins** (installed locally)
- **Git** (optional)

---

## 📂 Project Structure

hello-java-maven/
│
├── pom.xml

├── screenshots/

└── src/

└── main/

└── java/

└── HelloWorld.java

---


## 🔧 Running in Jenkins (Local Installation)

1. **Open Jenkins**

   * Start Jenkins service:

     sudo systemctl start jenkins   # On Linux

   * Open in browser: `http://localhost:8080`

2. **Configure Tools**

   * Go to: `Manage Jenkins → Global Tool Configuration`
   * Add **Maven** (e.g., Maven 3.8.6)

3. **Create a Freestyle Job**

   * Dashboard → **New Item** → Name: `hello-java-maven-job`
   * **Source Code Management**:

     * If Git: select Git and paste repo URL
     * If local: select **None** and copy project files manually into Jenkins workspace
   * **Build**: Add step → **Invoke top-level Maven targets**

     * Maven Version: your configured Maven
     * Goals: `clean package`

4. **Build the Job**

   * Click **Build Now**
   * Go to **Console Output** and check for:

     ```
     [INFO] BUILD SUCCESS
     ```

---

## 📷 Deliverables

* Screenshot of **Console Output** showing `BUILD SUCCESS`
* `pom.xml` + `HelloWorld.java` in repository

