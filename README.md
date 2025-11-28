<div align="center">

# 📘 University Exam Timetabling Dashboard

### An Intelligent Scheduling & Visualization Tool

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)

<p align="center">
  <img width="1524" height="777" alt="image" src="https://github.com/user-attachments/assets/be452730-9677-4845-9caf-04d23a88c29f" />
  <br>
  <em><img width="1514" height="843" alt="image" src="https://github.com/user-attachments/assets/c58c624c-7b60-47c8-991c-7b5dbceec62d" />


</p>

</div>

---

## 📖 Overview

The **University Exam Timetabling Dashboard** is a modern, interactive web application designed to solve the complex problem of scheduling university exams without conflicts.

Leveraging **Graph Coloring** principles, this tool simulates a university environment with **120 courses** and **1500 students**, builds a conflict graph based on student enrollments, and generates optimal schedules using two distinct algorithmic approaches.

## ⚙️ Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | ![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white) | Interactive dashboard and data visualization |
| **Backend** | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white) | Core logic and graph processing |
| **Optimization** | **Greedy + Tabu Search** | Hybrid algorithmic approach for schedule minimization |
| **Deployment** | **Cloudflared** | Secure tunneling for Google Colab deployment |

---

## 🚀 Key Features

### 1. Advanced Algorithmic Comparison 🧪
Visualize the difference between heuristic speed and meta-heuristic optimization:
* **Greedy Welsh–Powell:** A fast, sequential graph coloring method. It guarantees a valid schedule but often results in a longer exam period (more time slots).
* **Tabu Search Optimization:** A local search meta-heuristic that takes the Greedy output and "compacts" it. It aggressively reduces the number of time slots required while maintaining zero conflicts.

### 2. Interactive Visualization 📊
* **Dynamic Grid:** A responsive timetable view where exams are grouped by time slots.
* **Aesthetic UI:** Clean, modern interface with color-coded exam blocks based on density or department.
* **Real-time Stats:** Instantly view the "Total Slots Used" and "Conflict Count" for both algorithms.

### 3. Smart Search & Discovery 🔍
* **Instant Filtering:** Locate specific courses (e.g., `C005`) instantly.
* **Highlighting:** The searched course is visually highlighted within the dense timetable grid for easy tracking.

### 4. Robust Data Simulation 👥
* Generates a synthetic dataset of **120 Courses** and **1500 Students**.
* Automatically constructs an adjacency matrix (conflict graph) based on shared student enrollments.
* Guarantees **Zero-Conflict** schedules for both algorithms.

---

## 🧠 How It Works

The system operates in three stages:

1.  **Data Generation:** * Students are assigned random courses (2-6 per student). 
    * If a student takes both Course A and Course B, an "edge" is drawn between them, meaning they cannot be scheduled at the same time.
2.  **Greedy Phase (Initialization):**
    * Courses are sorted by "degree" (number of conflicts).
    * The algorithm assigns the first available color (time slot) to the most conflicted courses first.
3.  **Tabu Search Phase (Optimization):**
    * The system attempts to move exams to earlier slots.
    * It uses a "Tabu List" to prevent cycling back to previous bad states, allowing it to escape local optima and find a tighter schedule.

---

## 📦 Made By
Fatimaa Khan,
Fatimah Sajid,
Rania Imran
