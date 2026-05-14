# Lab 1 Git Restore

Hello Students

In this lab you are going to learn:

How git restore works

How to discard local file changes

How to restore file back to previous committed state

---

Step 1 Create Project

Run:

```bash id="mpu3vx"
mkdir git-restore-lab
cd git-restore-lab
git init
```

---

Step 2 Create File

Run:

```bash id="2zjlwm"
echo "Version 1" > demo.txt
```

---

Step 3 Add and Commit

Run:

```bash id="y6j0we"
git add .
git commit -m "Initial commit"
```

---

Step 4 Modify File

Run:

```bash id="gq1x5u"
echo "Version 2" >> demo.txt
```

---

Step 5 Verify File Content

Run:

```bash id="91jlwm"
cat demo.txt
```

You will see:

```text id="c7q44r"
Version 1
Version 2
```

---

Step 6 Check Git Status

Run:

```bash id="7xjlwm"
git status
```

You will notice:
File is modified.

---

Step 7 Restore File

Run:

```bash id="5jlwmx"
git restore demo.txt
```

---

Step 8 Verify File Again

Run:

```bash id="vwjlwm"
cat demo.txt
```

You will notice:
Version 2 disappeared.

File restored to previous commit state.

---

# Lab 2 Git Reset Soft

Hello Students

In this lab you are going to learn:

How soft reset works

How commit is removed

How staging area remains preserved

---

Step 1 Create Project

Run:

```bash id="jlwmx1"
mkdir git-reset-soft-lab
cd git-reset-soft-lab
git init
```

---

Step 2 Create Initial File

Run:

```bash id="jlwmx2"
echo "Version 1" > demo.txt
git add .
git commit -m "Commit 1"
```

---

Step 3 Modify File

Run:

```bash id="jlwmx3"
echo "Version 2" >> demo.txt
git add .
git commit -m "Commit 2"
```

---

Step 4 Verify Commit History

Run:

```bash id="jlwmx4"
git log --oneline
```

You will see:
Two commits.

---

Step 5 Perform Soft Reset

Run:

```bash id="jlwmx5"
git reset --soft HEAD~1
```

---

Step 6 Check Git Status

Run:

```bash id="jlwmx6"
git status
```

You will notice:
Changes remain staged.

---

Step 7 Verify Log

Run:

```bash id="jlwmx7"
git log --oneline
```

Latest commit disappeared.

---

Expected Result

Commit removed

Changes still inside staging area

---

# Lab 3 Git Reset Mixed

Hello Students

In this lab you are going to learn:

How mixed reset works

How staging gets removed

How changes remain in modified area

---

Step 1 Create Project

Run:

```bash id="jlwmx8"
mkdir git-reset-mixed-lab
cd git-reset-mixed-lab
git init
```

---

Step 2 Create Initial File

Run:

```bash id="jlwmx9"
echo "Version 1" > demo.txt
git add .
git commit -m "Commit 1"
```

---

Step 3 Modify File

Run:

```bash id="jlwmx10"
echo "Version 2" >> demo.txt
git add .
git commit -m "Commit 2"
```

---

Step 4 Perform Mixed Reset

Run:

```bash id="jlwmx11"
git reset --mixed HEAD~1
```

---

Step 5 Check Git Status

Run:

```bash id="jlwmx12"
git status
```

You will notice:
File is modified
But not staged.

---

Step 6 Verify File Content

Run:

```bash id="jlwmx13"
cat demo.txt
```

You will still see:
Version 2 exists.

---

Expected Result

Commit removed

Staging removed

Changes preserved in working directory

---

# Lab 4 Git Reset Hard

Hello Students

In this lab you are going to learn:

How hard reset works

How commits disappear

How changes are deleted permanently

---

Step 1 Create Project

Run:

```bash id="jlwmx14"
mkdir git-reset-hard-lab
cd git-reset-hard-lab
git init
```

---

Step 2 Create Initial File

Run:

```bash id="jlwmx15"
echo "Version 1" > demo.txt
git add .
git commit -m "Commit 1"
```

---

Step 3 Modify File

Run:

```bash id="jlwmx16"
echo "Version 2" >> demo.txt
git add .
git commit -m "Commit 2"
```

---

Step 4 Verify File Content

Run:

```bash id="jlwmx17"
cat demo.txt
```

You will see:

```text id="jlwmx18"
Version 1
Version 2
```

---

Step 5 Perform Hard Reset

Run:

```bash id="jlwmx19"
git reset --hard HEAD~1
```

---

Step 6 Verify File Again

Run:

```bash id="jlwmx20"
cat demo.txt
```

You will notice:
Version 2 disappeared.

---

Step 7 Verify Commit History

Run:

```bash id="jlwmx21"
git log --oneline
```

Latest commit removed completely.

---

Expected Result

Commit removed

Staging removed

Working directory changes deleted permanently
