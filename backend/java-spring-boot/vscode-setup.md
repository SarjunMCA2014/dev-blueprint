# Spring Boot Setup for VS Code on Windows (2026 Edition)

This guide covers the essential steps to configure **Visual Studio Code** for the latest **Spring Boot 4.x** and **Java 21/25** development.

---

## 🛠 1. Essential VS Code Extensions

Open the Extensions view (`Ctrl+Shift+X`) and install the following:

- **Extension Pack for Java** (Microsoft): Provides language support, debugger, and build tool (Maven/Gradle) integration.
- **Spring Boot Extension Pack** (VMware): Provides the Spring Initializr, Spring Boot Dashboard, and smart code navigation.

---

## ☕ 2. Java Runtime Configuration

Ensure VS Code is using the correct JDK for your Spring projects.

1.  Press `Ctrl + Shift + P` to open the **Command Palette**.
2.  Type `Java: Configure Java Runtime` and select it.
3.  In the **Project JDKs** tab, verify it points to **Java 21** or **Java 25**.
4.  If not found, add the path to your JDK installation (e.g., `C:\Program Files\Eclipse Adoptium\jdk-25...`).

---

## 🚀 3. Creating a New Project

You can generate a Spring Boot project without leaving VS Code:

1.  Open the Command Palette (`Ctrl + Shift + P`).
2.  Type `Spring Initializr: Create a Maven Project` (or Gradle).
3.  **Spring Boot Version:** Select the latest stable (e.g., `4.0.4`).
4.  **Dependencies:** Add at least `Spring Web` and `Spring Boot DevTools`.
5.  Save and **Open** the project when prompted.

---

## 🖥️ 4. Running & Debugging

The **Spring Boot Dashboard** is the primary way to manage your apps.

- **Launch:** Click the **Spring Boot Icon** (Leaf logo) in the Activity Bar on the left.
- **Start/Debug:** Hover over your project name and click the **Play** or **Bug** icon.
- **Hot Reload:** If `Spring Boot DevTools` is in your dependencies, VS Code will automatically restart the server when you save changes.

---

## ⌨️ Useful Shortcuts for Windows

| Action                   | Shortcut           |
| :----------------------- | :----------------- |
| **Run Application**      | `Ctrl + F5`        |
| **Debug Application**    | `F5`               |
| **Command Palette**      | `Ctrl + Shift + P` |
| **Search Symbols/Beans** | `Ctrl + Shift + O` |
| **Format Code**          | `Shift + Alt + F`  |

---

## 📝 Verification Checklist

1. [ ] `java -version` in terminal shows Java 21+.
2. [ ] Project `pom.xml` or `build.gradle` loaded without errors.
3. [ ] Console shows `Tomcat started on port 8080`.
4. [ ] Browsing `http://localhost:8080` works.
