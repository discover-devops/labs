Lab Create and Connect Local Git Repository with GitHub Repository

Hello Students

In this lab you are going to learn:

How to create GitHub repository

How to create local Git repository using Git Bash

How to connect local repository with GitHub repository

---

Step 1 Create GitHub Repository

Open browser and go to:

```text id="yjlwm1"
https://github.com
```

Login with your GitHub account.

---

Step 2 Create New Repository

Click:

New Repository

Provide:

Repository Name:

```text id="yjlwm2"
git-remote-lab
```

Select:
Public

Do not select:
Add README
Add .gitignore
Add License

Click:
Create Repository

---

Step 3 Copy Repository URL

After repository creation you will see repository URL.

Example:

```text id="yjlwm3"
https://github.com/yourusername/git-remote-lab.git
```

Copy this URL.

---

Step 4 Open Git Bash

Open Git Bash on Windows laptop.

---

Step 5 Create Local Project Directory

Run:

```bash id="yjlwm4"
mkdir git-remote-lab
cd git-remote-lab
```

---

Step 6 Initialize Local Git Repository

Run:

```bash id="yjlwm5"
git init
```

Now local Git repository is created.

---

Step 7 Configure Git Username

Run:

```bash id="yjlwm6"
git config --global user.name "YourName"
```

Example:

```bash id="yjlwm7"
git config --global user.name "Rahul"
```

---

Step 8 Configure Git Email

Run:

```bash id="yjlwm8"
git config --global user.email "yourmail@example.com"
```

Example:

```bash id="yjlwm9"
git config --global user.email "rahul@gmail.com"
```

---

Step 9 Verify Configuration

Run:

```bash id="yjlwm10"
git config --global --list
```

---

Step 10 Create First File

Run:

```bash id="yjlwm11"
echo "Hello GitHub" > file1.txt
```

---

Step 11 Verify File

Run:

```bash id="yjlwm12"
ls
```

---

Step 12 Add File to Staging Area

Run:

```bash id="yjlwm13"
git add .
```

---

Step 13 Commit File

Run:

```bash id="yjlwm14"
git commit -m "Initial commit"
```

---

Step 14 Connect Local Repository with GitHub Repository

Run:

```bash id="yjlwm15"
git remote add origin https://github.com/yourusername/git-remote-lab.git
```

Replace:
yourusername
with your actual GitHub username.

---

Step 15 Verify Remote Connection

Run:

```bash id="yjlwm16"
git remote -v
```

You should see:

```text id="yjlwm17"
origin  https://github.com/yourusername/git-remote-lab.git fetch
origin  https://github.com/yourusername/git-remote-lab.git push
```

---

Expected Learning Outcome

After completing this lab students should understand:

How to create GitHub repository

How to initialize local Git repository

How to create commits locally

How to connect local repository with remote GitHub repository

How Git establishes local and remote repository communication
