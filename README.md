# 🖥️ Automated Platform Surveillance System

## 📝 Project Overview
This project is a periodic system monitoring and logging automation tool written in Python. It acts as a background surveillance script that automatically captures the current state of the operating system and running processes at fixed intervals, saving the data into neatly organized, timestamped log files.

## 🚀 Key Features

### 📊 System Health Report
At every scheduled interval, the script logs core system statistics using the `psutil` module:
* **CPU Usage:** Current processing load.
* **RAM Usage:** Memory consumption metrics.
* **Disk Usage:** Storage statistics across all partitions.
* **Network Stats:** Data sent and received over the network.

### ⚙️ Process Monitoring Report
The script acts like an automated Task Manager, logging details for every active process:
* **Process ID (PID)**, **Name**, **Username**, and **Status**.
* **Process Start Time**.
* **Resource Consumption:** CPU % and Memory % utilized by each specific process.

### ⏱️ Automated Execution & Logging
* **Auto-Directory Generation:** Checks for and creates a target folder for logs if it does not already exist using the `os` module.
* **Timestamped Logs:** Creates a uniquely named log file for every scan using current epoch time formatting via the `time` module.
* **Infinite Scheduling:** Runs continuously at user-defined intervals (e.g., every 5 minutes) using the `schedule` module until manually terminated with `Ctrl + C`.

## 🛠️ Technology Stack & Modules Used
* **Language:** Python
* **`psutil`:** Fetches cross-platform system and process information.
* **`os`:** Handles file system operations (checking paths, creating directories).
* **`sys`:** Handles command-line arguments (e.g., passing directory names via `sys.argv`).
* **`time`:** Formats timestamps and manages process sleep states.
* **`schedule`:** Automates the execution of the logging function at regular intervals.

## ⚙️ How to Run
1. Ensure you have the required external libraries installed:
   ```bash
   pip install psutil schedule
