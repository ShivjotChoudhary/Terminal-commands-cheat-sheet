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

Practice daily.  
**Terminal confidence = developer confidence.**
Python Virtual Environment (venv) – Commands + Real-Life Examples
===============================================================

1) Check Python installation

macOS / Linux:
python3 --version

Windows:
python --version

Use: confirms Python is installed


2) Create project folder

mkdir python_project
cd python_project

Use: keeps project files organized


3) Create virtual environment

macOS / Linux:
python3 -m venv venv

Windows:
python -m venv venv

Use: creates isolated Python environment in venv/


4) Activate virtual environment

macOS / Linux:
source venv/bin/activate

Windows (CMD / PowerShell):
venv\Scripts\activate

Use: switches Python & pip to venv
Indicator: (venv) appears in terminal


5) Install package (example)

pip install numpy

Use: installs package only inside venv


6) Check installed packages

pip list

Use: shows packages installed in active environment


7) Save dependencies

pip freeze > requirements.txt

Use: saves exact package versions
Example content:
numpy==1.26.4


8) Install dependencies from file

pip install -r requirements.txt

Use: recreates same environment on another system


9) Start Python interpreter

Inside venv:
python

macOS system (outside venv):
python3

Use: starts Python shell


10) Check which Python is being used

macOS / Linux:
which python

Windows:
where python

Use: confirms Python is from venv or system


11) Deactivate virtual environment

deactivate

Use: switches back to system Python


------------------------------------------------
REAL-LIFE EXAMPLES
------------------------------------------------

Example 1: Two projects conflict
Project A needs numpy 1.26
Project B needs numpy 1.22

Without venv → one project breaks
With venv → both work separately


Example 2: College project
Teacher runs:
pip install -r requirements.txt

Project runs exactly the same


Example 3: GitHub project
You push:
- Python files
- requirements.txt

Anyone can recreate environment easily


Example 4: Learning & experiments
If environment breaks:
rm -rf venv

Create again and start fresh


Example 5: Job / internship workflow
Companies expect:
- virtual environment
- requirements.txt
- clean dependency management

Using venv = professional Python workflow
