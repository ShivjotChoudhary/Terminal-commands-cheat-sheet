# 🖥️ Terminal Commands Cheat Sheet (Beginner → Advanced)

A simple, practical guide to terminal/command-line usage.
Made for daily practice and quick revision.

---

## 📍 Navigation & Location

### pwd — Print Working Directory
Shows the directory you are currently in.
```bash
pwd
```

---

### ls — List Files & Folders
```bash
ls        # list files
ls -l     # detailed list
ls -a     # include hidden files
ls -lh    # human-readable sizes
```

---

### cd — Change Directory
```bash
cd folder_name
cd ..
cd ~
cd /Users/username/Desktop
```

---

## 📂 File & Folder Creation

### mkdir — Make Directory
```bash
mkdir screenshots
mkdir project logs backups
```

---

### touch — Create Empty File
```bash
touch README.md
touch app.py
```

---

## 🗑️ Delete Files & Folders

### rm — Remove File
```bash
rm file.txt
```

### rm -r — Remove Folder
```bash
rm -r screenshots
```

⚠️ Permanent delete (no recycle bin)

---

## 📄 Copy, Move & Rename

### cp — Copy
```bash
cp file.txt copy.txt
cp -r screenshots backup/
```

---

### mv — Move or Rename
```bash
mv old.txt new.txt
mv ui-main.png screenshots/
```

---

## 📦 Zip & Unzip

### zip — Create Zip File
```bash
zip file.zip file.txt
zip -r project.zip project/
zip -r Matrix-Calculator-macOS.zip "Matrix Calculator.app"
```

Explanation:
- `-r` → recursive (folders)
- First name → zip file
- Second name → file/folder to zip

---

### unzip — Extract Zip
```bash
unzip project.zip
unzip project.zip -d output_folder/
```

---

## 🖼️ Open Files & Folders (macOS)

```bash
open .
open image.png
open "Matrix Calculator.app"
```

---

## 🔍 Search Files

```bash
find . -name "*.png"
```

---

## ⚙️ Permissions

```bash
chmod +x script.sh
```

---

## 🧹 Clear Terminal

```bash
clear
```
Shortcut: `Cmd + K`

---

## 🧠 System Info

```bash
whoami
date
```

---

## 🌱 Git Basics

```bash
git status
git add .
git commit -m "message"
```

---

## 🔑 Important Symbols

| Symbol | Meaning |
|------|--------|
| . | Current directory |
| .. | Parent directory |
| ~ | Home directory |
| / | Root |
| * | Wildcard |

Example:
```bash
rm *.png
```

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

---

## 🎯 Golden Rule

The terminal does **exactly** what you tell it.
If something fails, always check:
```bash
pwd
ls
```

Practice daily. Terminal confidence = developer confidence.
