---

## 📦 How to Upload This Package to GitHub

Follow these steps to upload your local package to GitHub:

---

### 1️⃣ Create a Repository on GitHub

1. Go to [GitHub](https://github.com/)
2. Click **+** (top right) → **New repository**
3. Fill in:

   * **Repository name** → choose a name (e.g., `my_ros_package`)
   * Visibility → Public or Private
   * **Do NOT** initialize with README (avoid conflicts)
4. Click **Create repository**
5. Copy the repository URL (e.g. `https://github.com/your-username/my_ros_package.git`)

---

### 2️⃣ Initialize Git in Your Local Package

Open a terminal (or Git Bash) and navigate to your package folder:

```bash
cd ~/Downloads/my_ros_package
```

Initialize git and create a `main` branch:

```bash
git init
git branch -M main
```

---

### 3️⃣ Add the Remote Repository

```bash
git remote add origin https://github.com/your-username/my_ros_package.git
```

---

### 4️⃣ Add & Commit Your Files

```bash
git add .
git commit -m "Initial commit of my package"
```

---

### 5️⃣ Push to GitHub

```bash
git push -u origin main
```

---

### ⚠️ Fixing LF → CRLF Warnings (Windows Users)

If you see warnings like:

```
warning: LF will be replaced by CRLF the next time Git touches it
```

This just means Git detected Linux-style line endings (LF) but Windows uses CRLF.
For ROS/Gazebo packages, **keep LF endings** for better cross-platform compatibility:

```bash
git config core.autocrlf input
```

Or make it global (applies to all repos):

```bash
git config --global core.autocrlf input
```

Optional: You can add a `.gitattributes` file to your repo to force LF endings for all text files:

```gitattributes
* text=auto eol=lf
```

Commit it:

```bash
git add .gitattributes
git commit -m "Add gitattributes to enforce LF endings"
git push
```

---

### 🔄 Updating the Repository Later

When you make changes locally, update GitHub with:

```bash
git add .
git commit -m "Describe your changes here"
git push
```

---
