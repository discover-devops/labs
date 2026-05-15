# Lab Git Push Git Pull and Git Fetch

Hello Students

In this lab you are going to learn:

What is git push

What is git pull

What is git fetch

Difference between push pull and fetch

How local and remote repositories communicate

---

# PART 1

# Git Push

---

# WHAT IS GIT PUSH

git push sends:

* local commits
  to
* remote GitHub repository

It uploads your local changes to GitHub.

---

# STEP 1 Move into Repository

Run:

```bash id="push1"
cd git-remote-lab
```

---

# STEP 2 Verify Remote Connection

Run:

```bash id="push2"
git remote -v
```

---

# STEP 3 Create New File

Run:

```bash id="push3"
echo "This file is pushed to GitHub" > push-demo.txt
```

---

# STEP 4 Add File

Run:

```bash id="push4"
git add .
```

---

# STEP 5 Commit Changes

Run:

```bash id="push5"
git commit -m "Added push demo file"
```

---

# STEP 6 Push Changes to GitHub

Run:

```bash id="push6"
git push origin main
```

If local branch is master:

```bash id="push7"
git push origin master
```

---

# STEP 7 Verify on GitHub

Refresh GitHub repository page.

You should see:
push-demo.txt

---

# WHAT HAPPENED

```text id="push8"
Local Repository
        |
        |
    git push
        |
        |
Remote GitHub Repository
```

---

# PART 2

# Git Fetch

---

# WHAT IS GIT FETCH

git fetch downloads:

* latest remote changes

BUT:

* does not merge them into local branch

Safe operation.

---

# STEP 1 Create New File Directly in GitHub

Open GitHub repository.

Create:

```text id="fetch1"
fetch-demo.txt
```

Commit directly on GitHub.

---

# STEP 2 Run Git Fetch

Back in Git Bash run:

```bash id="fetch2"
git fetch origin
```

---

# STEP 3 Verify Fetch

Run:

```bash id="fetch3"
git status
```

You may notice:
remote branch updated.

---

# STEP 4 Verify File

Run:

```bash id="fetch4"
ls
```

You will notice:
fetch-demo.txt is NOT present yet.

Reason:
fetch only downloads metadata and commits.
No merge happens.

---

# WHAT HAPPENED

```text id="fetch5"
GitHub Repository
        |
        |
    git fetch
        |
        |
Local Git Database Only
```

No working directory update.

---

# PART 3

# Git Pull

---

# WHAT IS GIT PULL

git pull performs:

```text id="pull1"
git fetch
+
git merge
```

It:

* downloads remote changes
* merges them into current branch

---

# STEP 1 Pull Latest Changes

Run:

```bash id="pull2"
git pull origin main
```

If branch is master:

```bash id="pull3"
git pull origin master
```

---

# STEP 2 Verify Files

Run:

```bash id="pull4"
ls
```

Now you will see:

```text id="pull5"
fetch-demo.txt
```

---

# WHAT HAPPENED

```text id="pull6"
GitHub Repository
        |
        |
     git pull
        |
        |
Downloads + Merges
        |
        |
Local Working Directory Updated
```

---

# FINAL DIFFERENCE

| Command   | Purpose                           |
| --------- | --------------------------------- |
| git push  | Upload local commits to GitHub    |
| git fetch | Download remote changes only      |
| git pull  | Download and merge remote changes |

---

# IMPORTANT CONCEPT

git fetch is safer because:

* it does not automatically merge
* allows review before integration

git pull is faster because:

* fetch + merge together

---

# EXPECTED LEARNING OUTCOME

After completing this lab students should understand:

How local and remote repositories synchronize

Difference between push pull and fetch

How GitHub communication works

Difference between downloading and merging remote changes
