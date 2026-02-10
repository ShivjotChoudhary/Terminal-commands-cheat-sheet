# 🖥️ Terminal Commands Cheat Sheet (Beginner → Advanced)

A simple, practical guide to terminal / command-line usage.  
Made for **daily practice, real work, and quick revision**.

---

## 📍 Navigation & Location

### `pwd` — Print Working Directory
Shows where you are right now.
```bash
pwd
```
**Real case:**  
You’re lost in folders → run `pwd` to confirm your exact location.

---

### `ls` — List Files & Folders
```bash
ls        # list files
ls -l     # detailed list (size, date, permissions)
ls -a     # include hidden files
ls -lh    # readable file sizes
```
**Real case:**  
Check whether screenshots, README, or output files exist before moving or deleting.

---

### `cd` — Change Directory
```bash
cd folder_name
cd ..
cd ~
cd /Users/username/Desktop
```
**Real case:**  
Navigate to your project folder before running Python scripts or zipping files.

---

## 📂 File & Folder Creation

### `mkdir` — Make Directory
```bash
mkdir screenshots
mkdir project logs backups
```
**Real case:**  
Create folders to organize images, logs, or backup files before uploading to GitHub.

---

### `touch` — Create Empty File
```bash
touch README.md
touch app.py
```
**Real case:**  
Quickly create files for documentation or starting new code.

---

## 🗑️ Delete Files & Folders

### `rm` — Remove File
```bash
rm file.txt
```

### `rm -r` — Remove Folder
```bash
rm -r screenshots
```

⚠️ Permanent delete (no recycle bin)

**Real case:**  
Delete unused files or wrong screenshots before final submission.

---

## 📄 Copy, Move & Rename

### `cp` — Copy Files
```bash
cp file.txt copy.txt
cp -r screenshots backup/
```
**Real case:**  
Create backups before editing important files.

---

### `mv` — Move or Rename
```bash
mv old.txt new.txt
mv ui-main.png screenshots/
```
**Real case:**  
Rename output files or move screenshots into proper folders.

---

## 📦 Zip & Unzip

### `zip` — Create Zip File
```bash
zip file.zip file.txt
zip -r project.zip project/
zip -r Matrix-Calculator-macOS.zip "Matrix Calculator.app"
```

**Explanation:**
- `-r` → recursive (folders)
- First name → zip file
- Second name → file/folder to zip

**Real case:**  
Compress project or app files before sharing or uploading.

---

### `unzip` — Extract Zip
```bash
unzip project.zip
unzip project.zip -d output_folder/
```
**Real case:**  
Extract downloaded project or assignment files.

---

## 🖼️ Open Files & Folders (macOS)

```bash
open .
open image.png
open "Matrix Calculator.app"
```
**Real case:**  
Instantly preview images, apps, or folders without Finder clicks.

---

## 🔍 Search Files

```bash
find . -name "*.png"
```
**Real case:**  
Locate all screenshots or images inside a large project.

---

## ⚙️ Permissions

```bash
chmod +x script.sh
```
**Real case:**  
Make shell or Python scripts executable before running them.

---

## 🧹 Clear Terminal

```bash
clear
```
Shortcut: `Cmd + K`

**Real case:**  
Clean cluttered terminal output to focus on fresh commands.

---

## 🧠 System Info

```bash
whoami
date
```
**Real case:**  
Confirm logged-in user or timestamp logs/debug output.

---

## 🌱 Git Basics (Only Essentials)

```bash
git status
git add .
git commit -m "message"
```
**Real case:**  
Check changes and save project progress.

---

## 🔑 Important Symbols

| Symbol | Meaning |
|------|--------|
| . | Current directory |
| .. | Parent directory |
| ~ | Home directory |
| / | Root directory |
| * | Wildcard |

Example:
```bash
rm *.png
```
Deletes all PNG files in the current folder.

---

## 🧠 Real-Life Example Workflow

```bash
cd python/GUI_app
ls
mkdir screenshots
mv ui*.png screenshots/
cd screenshots
zip -r ui-images.zip .
open .
```

👉 Clean → organize → zip → preview → upload.

---

## 🎯 Golden Rule

The terminal does **exactly** what you tell it.

If something fails, always check:
```bash
pwd
ls
```
---
# Python Virtual Environment (venv) Cheat Sheet

A quick reference guide for managing isolated Python environments and dependencies.

## 🛠 Basic Commands

### 1. Check Python Installation
*Confirm Python is installed on your system.*

**macOS / Linux:**
```bash
python3 --version
```

**Windows:**
```bash
python --version
```

### 2. Create Project Folder
*Keeps your project files organized.*
```bash
mkdir python_project
cd python_project
```

### 3. Create Virtual Environment
*Creates an isolated Python environment in a folder named `venv`.*

**macOS / Linux:**
```bash
python3 -m venv venv
```

**Windows:**
```bash
python -m venv venv
```

### 4. Activate Virtual Environment
*Switches your terminal to use the isolated Python & pip. Look for `(venv)` in your prompt.*

**macOS / Linux:**
```bash
source venv/bin/activate
```

**Windows (CMD / PowerShell):**
```bash
venv\Scripts\activate
```

### 5. Install Package
*Installs a package ONLY inside the virtual environment.*
```bash
pip install numpy
```

### 6. Check Installed Packages
*Shows a list of all packages currently installed in the active environment.*
```bash
pip list
```

### 7. Save Dependencies
*Saves exact package versions to a file. Critical for sharing projects.*
```bash
pip freeze > requirements.txt
```
*Example content:* `numpy==1.26.4`

### 8. Install Dependencies from File
*Recreates the exact same environment on another system.*
```bash
pip install -r requirements.txt
```

### 9. Start Python Interpreter
*Starts the Python shell.*

**Inside venv:**
```bash
python
```

**macOS System (Outside venv):**
```bash
python3
```

### 10. Check Which Python is Running
*Confirms if you are using the `venv` Python or the System Python.*

**macOS / Linux:**
```bash
which python
```

**Windows:**
```bash
where python
```

### 11. Deactivate Virtual Environment
*Exits the virtual environment and returns to system Python.*
```bash
deactivate
```

---

## 🌍 Real-Life Examples & Use Cases

### Example 1: Avoiding Version Conflicts
* **Scenario:** Project A needs `numpy 1.26` but Project B needs `numpy 1.22`.
* **Without venv:** Installing one version breaks the other project.
* **With venv:** Both projects have their own folders and work separately without issues.

### Example 2: College/University Projects
* **Scenario:** Your teacher runs your code.
* **Workflow:** They run `pip install -r requirements.txt`.
* **Result:** The project runs exactly the same on their machine as it did on yours.

### Example 3: GitHub Collaboration
* **Scenario:** You push your code to GitHub.
* **Best Practice:** You commit your Python files and `requirements.txt` (but **not** the `venv` folder).
* **Result:** Anyone who downloads your repo can recreate your environment instantly.

### Example 4: Learning & Experiments
* **Scenario:** You are testing a new library and it breaks your setup.
* **Solution:** Simply delete the folder (`rm -rf venv`) and create it again.
* **Benefit:** Your main system remains clean and unbroken.

### Example 5: Professional Workflow
* **Scenario:** Applying for jobs or internships.
* **Expectation:** Companies expect you to use virtual environments and dependency files.
* **Verdict:** Using `venv` demonstrates a professional development workflow.
