# Lab 1 Git Branch Command

Hello Students

In this lab you are going to learn:

What is a branch

How to create branch

How to switch branch

How branches work independently

---

Step 1 Create New Project

Run:

```bash id="i40j8w"
mkdir git-branch-lab
cd git-branch-lab
git init
```

---

Step 2 Create Initial File

Run:

```bash id="0g1d1h"
echo "Version 1" > app.txt
```

---

Step 3 Add and Commit

Run:

```bash id="j4kp7s"
git add .
git commit -m "Initial commit"
```

---

Step 4 Check Existing Branch

Run:

```bash id="v4a1fj"
git branch
```

You will see:

```bash id="fybshs"
main
```

or

```bash id="a7v40h"
master
```

---

Step 5 Create New Branch

Run:

```bash id="g1ksxv"
git branch feature-login
```

---

Step 6 Verify Branches

Run:

```bash id="0gb4d7"
git branch
```

You will see:

```bash id="u2w92o"
main
feature-login
```

Current active branch will contain star symbol.

---

Step 7 Switch to Feature Branch

Run:

```bash id="12v69r"
git switch feature-login
```

---

Step 8 Modify File

Run:

```bash id="q2i1md"
echo "Login feature added" >> app.txt
```

---

Step 9 Commit Changes

Run:

```bash id="62qud8"
git add .
git commit -m "Added login feature"
```

---

Step 10 Switch Back to Main Branch

Run:

```bash id="kgpn5u"
git switch main
```

---

Step 11 Verify File Content

Run:

```bash id="hm0gb7"
cat app.txt
```

You will notice:
Login feature does not exist in main branch.

This proves branch isolation.

---

# Lab 2 Git Fast Forward Merge

Hello Students

In this lab you are going to learn:

What is fast forward merge

How Git moves branch pointer

How branches merge without merge commit

---

Step 1 Create Feature Branch

Run:

```bash id="88eg93"
git switch -c feature-payment
```

---

Step 2 Modify File

Run:

```bash id="g8iv2l"
echo "Payment feature added" >> app.txt
```

---

Step 3 Commit Changes

Run:

```bash id="rwjlwm"
git add .
git commit -m "Added payment feature"
```

---

Step 4 Switch Back to Main

Run:

```bash id="0p48fk"
git switch main
```

---

Step 5 Merge Feature Branch

Run:

```bash id="d8i4q0"
git merge feature-payment
```

Git performs:
Fast Forward Merge

Reason:
Main branch had no new commits.

---

Step 6 Verify Merge History

Run:

```bash id="l1dc9j"
git log --oneline --graph
```

You will notice:
Straight line history.

No merge commit created.

---

# Lab 3 Git Three Way Merge

Hello Students

In this lab you are going to learn:

What is three way merge

How merge conflicts happen

How Git creates merge commit

---

Step 1 Create New Branch

Run:

```bash id="7vk9x8"
git switch -c feature-search
```

---

Step 2 Modify File in Feature Branch

Run:

```bash id="4mjlwm"
echo "Search feature added" >> app.txt
```

---

Step 3 Commit Changes

Run:

```bash id="86a5o0"
git add .
git commit -m "Added search feature"
```

---

Step 4 Switch Back to Main

Run:

```bash id="12qk2q"
git switch main
```

---

Step 5 Modify Same File in Main

Run:

```bash id="1ptv2r"
echo "Main branch update" >> app.txt
```

---

Step 6 Commit Main Branch Changes

Run:

```bash id="8cjlwm"
git add .
git commit -m "Updated main branch"
```

Now:
Both branches moved independently.

---

Step 7 Merge Feature Branch

Run:

```bash id="9qlahv"
git merge feature-search
```

Git performs:
Three Way Merge

Reason:
Both branches contain new commits.

---

Step 8 Verify Merge History

Run:

```bash id="a0wjlwm"
git log --oneline --graph
```

You will notice:
Merge commit created.

History becomes non linear.

---

Expected Learning Outcome

After completing these labs students should understand:

How Git branches work

How branch isolation works

Difference between fast forward and three way merge

How Git merges independent histories

How merge commits are created
