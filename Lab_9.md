# Lab Create Branch Push Code Create Pull Request Approve and Merge

Hello Students

In this lab you are going to learn complete real world GitHub workflow:

Create local branch

Commit changes

Push branch to GitHub

Create Pull Request

Review and Approve Pull Request

Merge branch into main

Delete branch after merge

This is how real DevOps and development teams work.

---

# IMPORTANT CONCEPT FIRST

---

# WHAT IS A BRANCH

A branch is:

* independent line of development

Purpose:

* isolate work safely
* develop features independently

Example:

```text id="prconcept1"
main branch = production stable code

feature branch = temporary development work
```

---

# WHAT IS A PULL REQUEST

Pull Request means:

```text id="prconcept2"
Request to merge code from one branch into another branch
```

Usually:

```text id="prconcept3"
feature branch
    →
main branch
```

---

# WHY PULL REQUEST IS IMPORTANT

Pull Request provides:

* code review
* approval process
* discussion
* automated testing
* safer merging

---

# COMPLETE WORKFLOW

```text id="prconcept4"
Create Branch
    ↓
Write Code
    ↓
Commit Changes
    ↓
Push Branch
    ↓
Create Pull Request
    ↓
Review and Approve
    ↓
Merge into Main
```

---

# STEP 1 Move into Repository

Run:

```bash id="prlab1"
cd git-remote-lab
```

---

# STEP 2 Verify Current Branch

Run:

```bash id="prlab2"
git branch
```

Current branch will be:

* main
  or
* master

---

# STEP 3 Create New Feature Branch

Run:

```bash id="prlab3"
git switch -c feature-payment
```

Meaning:

* create branch
* switch immediately

---

# STEP 4 Verify Branch

Run:

```bash id="prlab4"
git branch
```

You will see:

```text id="prlab5"
main
feature-payment
```

Star symbol indicates active branch.

---

# STEP 5 Create New File

Run:

```bash id="prlab6"
echo "Payment module added" > payment.txt
```

---

# STEP 6 Verify File

Run:

```bash id="prlab7"
ls
```

---

# STEP 7 Check Git Status

Run:

```bash id="prlab8"
git status
```

You will see:

* untracked file

---

# STEP 8 Add File into Staging Area

Run:

```bash id="prlab9"
git add .
```

---

# STEP 9 Commit Changes

Run:

```bash id="prlab10"
git commit -m "Added payment module"
```

Now:

* commit created locally
* branch pointer moves forward

---

# STEP 10 Push Feature Branch to GitHub

Run:

```bash id="prlab11"
git push origin feature-payment
```

This uploads:

* local branch
  to
* GitHub remote repository

---

# IMPORTANT CONCEPT

At this stage:

```text id="prlab12"
main branch remains unchanged
```

Only:

* feature-payment branch contains new code

---

# STEP 11 Open GitHub Repository

Go to GitHub repository in browser.

You will notice:
GitHub shows message:

```text id="prlab13"
Compare and Pull Request
```

Click it.

---

# STEP 12 Create Pull Request

You will see:

```text id="prlab14"
Base branch = main
Compare branch = feature-payment
```

Meaning:

```text id="prlab15"
Merge feature-payment into main
```

---

# STEP 13 Add Pull Request Details

Provide:

Title:

```text id="prlab16"
Added payment module
```

Description:

```text id="prlab17"
Implemented payment module feature
```

Click:

```text id="prlab18"
Create Pull Request
```

---

# IMPORTANT CONCEPT

Pull Request allows:

* team discussion
* review process
* automated CI validation
* approval workflow

Before code enters production branch.

---

# STEP 14 Review Pull Request

Inside Pull Request:

* review changed files
* verify code
* add comments if needed

---

# STEP 15 Approve Pull Request

Click:

```text id="prlab19"
Review Changes
```

Select:

```text id="prlab20"
Approve
```

Then:

```text id="prlab21"
Submit Review
```

---

# IMPORTANT CONCEPT

Approval means:

* reviewer verified code quality
* reviewer accepts merge request

Usually done by:

* senior developer
* tech lead
* DevOps reviewer

---

# STEP 16 Merge Pull Request

Click:

```text id="prlab22"
Merge Pull Request
```

Then:

```text id="prlab23"
Confirm Merge
```

Now:
feature branch code enters main branch.

---

# WHAT HAPPENS INTERNALLY

GitHub performs:

```text id="prlab24"
git merge feature-payment
```

inside remote repository.

---

# STEP 17 Delete Feature Branch

Click:

```text id="prlab25"
Delete Branch
```

Reason:

* feature work completed
* keep repository clean

---

# STEP 18 Pull Latest Changes Locally

Back in Git Bash run:

```bash id="prlab26"
git switch main
```

Then:

```bash id="prlab27"
git pull origin main
```

Now:
local main branch receives merged changes.

---

# VERIFY FILE

Run:

```bash id="prlab28"
ls
```

You should now see:

```text id="prlab29"
payment.txt
```

---

# FINAL ARCHITECTURE FLOW

```text id="prlab30"
Local Feature Branch
        ↓
git push
        ↓
GitHub Feature Branch
        ↓
Pull Request
        ↓
Code Review
        ↓
Approval
        ↓
Merge into Main
        ↓
git pull
        ↓
Local Main Updated
```

---

# EXPECTED LEARNING OUTCOME

After completing this lab students should understand:

Complete GitHub collaboration workflow

Difference between branch and Pull Request

Why Pull Request is important

How approval and merge process works

How teams safely integrate code into production branch
