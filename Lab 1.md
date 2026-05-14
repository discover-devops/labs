Lab 1 Creating and Committing a New File in Git

Hello Students

In this lab you are going to learn how to:

Create a new file

Initialize Git repository

Add file into staging area

Commit the file into Git repository

This is your first complete Git workflow lab.

Step 1 Create Project Directory

Run:

```bash
mkdir git-lab1
cd git-lab1
```

Step 2 Initialize Git Repository

Run:

```bash
git init
```

This creates a hidden .git directory.

Now Git starts tracking this project.

Step 3 Configure Git Username

Run:

```bash
git config --global user.name "YourName"
```

Example:

```bash
git config --global user.name "Rahul"
```

Step 4 Configure Git Email

Run:

```bash
git config --global user.email "yourmail@example.com"
```

Example:

```bash
git config --global user.email "rahul@gmail.com"
```

Step 5 Create a New File

Run:

```bash
echo "Hello Git" > file1.txt
```

Step 6 Verify File Exists

Run:

```bash
ls
```

You should see:

```bash
file1.txt
```

Step 7 Check Git Status

Run:

```bash
git status
```

You will notice:

```bash
Untracked file
```

Meaning:
Git sees the file
But Git is not tracking it yet.

Step 8 Add File to Staging Area

Run:

```bash
git add file1.txt
```

Now Git prepares this file for commit.

Step 9 Check Git Status Again

Run:

```bash
git status
```

You will see:

```bash
Changes to be committed
```

Meaning:
The file is now inside staging area.

Step 10 Commit the File

Run:

```bash
git commit -m "Added first file"
```

Now Git creates:

* snapshot
* version history
* commit ID

Step 11 Verify Commit

Run:

```bash
git log --oneline
```

You will see your commit history.

Expected Learning Outcome

After completing this lab students should understand:

How to create Git repository

How Git tracks files

Difference between untracked and staged files

How git add works

How git commit works

How Git stores history internally
