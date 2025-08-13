# 🐞 Bug Tracker Console Application

A simple **console-based bug tracking system** built in Java using Apache Maven.  
This application allows users to **report, view, and manage bugs** via a command-line interface, storing data in JSON files.

---

## 📂 Project Structure

The project follows the standard **Maven directory layout**:

bug-tracker-console/
│
├── .mvn/ # Maven wrapper files (optional)
├── src/
│ ├── main/
│ │ └── java/
│ │ └── com/
│ │ └── bugtracker/
│ │ ├── main/ # Application entry point
│ │ │ └── Main.java
│ │ ├── model/ # Data objects & enums
│ │ │ ├── Bug.java
│ │ │ ├── User.java
│ │ │ └── enums/
│ │ ├── service/ # Business logic & data handling
│ │ │ ├── BugReportingSystem.java
│ │ │ └── DataStore.java
│ └── test/ # Unit tests
│
├── target/ # Compiled code & packaged JAR (created by Maven)
├── pom.xml # Maven configuration file
├── bugs.json # Bug database (auto-created on first run)
└── users.json # User database (auto-created on first run)

yaml
Copy
Edit

**Key Files:**
- **`src/main/java`** → All Java source code.
- **`pom.xml`** → Maven configuration (dependencies, build settings).
- **`target/`** → Compiled `.class` files and packaged `.jar` output.
- **`bugs.json` / `users.json`** → Auto-generated JSON databases.

---

## 🛠 Requirements

Before running the project, ensure you have:

- **Java Development Kit (JDK)** — Version **11+**
- **Apache Maven** — Installed and configured in your PATH

---

## 🚀 How to Run

### 1️⃣ Open Terminal
Open **Command Prompt**, **PowerShell**, or **Terminal**.

### 2️⃣ Navigate to Project Directory
```bash
cd path/to/bug-tracker-console
3️⃣ Run the Application
Option A: Run Directly with Maven (Best for Development)
Compiles and runs the project without creating a .jar:

bash
Copy
Edit
mvn exec:java
Option B: Package into a Runnable JAR (Best for Distribution)
Build the project:

bash
Copy
Edit
mvn package
Run the generated .jar:

bash
Copy
Edit
java -jar target/bug-tracker-console-1.0-SNAPSHOT.jar
👤 Default User Credentials
Role	Username	Password
Reporter	reporter1	pass
Developer	dev1	pass
Developer	dev2	pass

📌 Notes
bugs.json and users.json will be created on the first run.

You can safely delete the target/ directory — Maven will recreate it.

