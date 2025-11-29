# Jarvis-
This is my first repo in github




   # Java Jarvis — Professional README

A lightweight, text-command–based personal assistant built using **Java**. The project aims to simulate a simple JARVIS-like assistant with modular commands, utilities, and an extensible structure. **Voice command functionality is currently non-functional**, and this README documents the system thoroughly while clearly noting that the voice subsystem needs debugging.

---

## 🔥 Project Overview

This project demonstrates how to build a modular assistant in Java capable of executing basic system-level tasks such as opening applications, performing web searches, telling time, and responding to predefined commands. The architecture has been intentionally designed to be simple, readable, and easy to expand.

**Important:**
The voice recognition system is not functioning at the moment. The core logic, command parser, and action executor work correctly, but the speech-to-text pipeline fails to capture or process microphone input.

---

## 📌 Features

* Text-based command input (fully functional)
* Modular command parser
* System actions (open browser, perform Google search, get system time, etc.)
* Clean and extensible code structure
* Placeholder voice recognition module (non-functional for now)

---

---

## 🛠️ Requirements

* **Java 11 or higher**
* **Maven / Gradle** (if you use a build tool)
* Microphone + audio drivers (only if you attempt voice debugging)
* Optional libraries for voice:

  * CMU Sphinx
  * Vosk
  * Google Speech-to-Text

---

## 🚀 Installation & Execution

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd java-jarvis
```

### 2. Build & Run (Maven)

```bash
mvn clean package
java -jar target/java-jarvis.jar
```

### 3. Build & Run (Gradle)

```bash
gradle build
gradle run
```

### 4. Direct Execution (IDE)

Open the project in IntelliJ / Eclipse and run **Main.java**.

---

## 🧠 Usage — Available Commands

Examples:

* `open browser` → Opens default web browser
* `search google <query>` → Performs a Google search
* `time` → Displays system time
* `help` → Shows available commands

> **Note:** Voice commands do not work yet. Use only text commands.

---

## ❌ Voice Command — Current Status

The voice module **does not work**, and the main issues are likely one of the following:

### 1. Microphone Permissions

* OS-level microphone access not granted
* Wrong audio device selected

### 2. Incorrect AudioFormat

Most voice libraries require very specific settings like:

* 16000 Hz sample rate
* Mono channel
* 16-bit little-endian samples

### 3. Missing or misconfigured speech model files

* Sphinx/Vosk model folder not found
* Wrong file path in code

### 4. Threading issues

* Listening thread not starting or getting blocked
* Buffer not receiving audio data

### 5. Unhandled Exceptions

If the module throws errors, fix them before testing recognition.

---

## 🔍 Voice Debugging Checklist (Follow in order)

1. Print logs: `Microphone opened`, `Reading bytes…`, etc.
2. Confirm microphone permissions in OS settings.
3. Verify `AudioFormat` matches your speech library requirements.
4. Check that model files exist and paths are correct.
5. Test microphone capture separately using a simple Java audio recorder.
6. If using cloud APIs, verify API keys and internet connection.

---

## 📘 Extending the Project

If you want to add more features, this structure supports:

* New commands (add cases in `CommandParser`)
* System utilities (add methods in `ActionHandler`)
* Custom APIs (weather, news, etc.)
* GUI version (JavaFX/Swing)

---

## 🤝 Contributing

Pull requests are welcome. When reporting issues, include:

* Full error logs
* Java version
* OS information
* Steps to reproduce


---

## 🛑
2. Console logs when running the module
3. Your OS + Java versio


