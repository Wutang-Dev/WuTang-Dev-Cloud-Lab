# Day 01 – Cloud Lab Setup (GitHub & Project Structure)

## 📌 Overview
This marks the beginning of my cloud journey, transitioning from on-prem infrastructure to Microsoft cloud environments.

The focus of this lab was setting up a clean GitHub repository structure to document all future cloud-based labs in a consistent and professional format.

---

## 🖥️ Environment

- Local Machine: Windows (Git Bash)
- GitHub Repository: WuTang-Dev-Cloud-Lab

---

## ⚙️ Key Steps

### 1. Repository Creation

Created a new public GitHub repository:

```
WuTang-Dev-Cloud-Lab
```

Configured:
- Visibility: Public
- README: Not initialised (handled locally)

---

### 2. Local Repository Setup

Initialised Git locally:

```bash
git init
```

Linked local repository to GitHub:

```bash
git remote add origin https://github.com/Wutang-Dev/WuTang-Dev-Cloud-Lab.git
```

---

### 3. Project Structure

Created initial folder structure:

```bash
mkdir Day-01-Cloud-Orientation
cd Day-01-Cloud-Orientation
touch README.md
```

---

### 4. Initial Commit

Added and committed files:

```bash
git add .
git commit -m "Day 01 - Cloud Lab Setup"
```

Set main branch:

```bash
git branch -M main
```

Pushed to GitHub:

```bash
git push -u origin main
```

---

## 🧠 Key Learning

- Importance of separating projects (on-prem vs cloud)
- Git workflow fundamentals:
  - init → add → commit → push
- Structuring repositories for scalability and clarity
- Building a consistent documentation habit from Day 1

---

## 🏁 Outcome

Successfully created and structured a new cloud lab repository, ready for ongoing Microsoft cloud labs.

This provides a clean foundation for documenting identity, device management, and cloud infrastructure moving forward.

---

## 🚀 Next Steps (Day 02)

- Explore Microsoft 365 Admin Center
- Navigate Entra ID (Identity & Access)
- Understand Intune (Device Management)
- Begin working with users and roles


Author Ravi Gordon 
