Lab 2 Modify Existing File and Create New File in Git

Hello Students

In this lab you are going to learn:

How to modify an existing file

How Git detects modified files

How to stage modified files

How to commit changes

How to create another new file

How to track multiple files in Git

Step 1 Move into Existing Repository

Run:

```bash id="r9n8f0"
cd git-lab1
```

Step 2 Check Existing Files

Run:

```bash id="8x9m5l"
ls
```

You should see:

```bash id="a5rjrl"
file1.txt
```

Step 3 Modify Existing File

Run:

```bash id="v67ikm"
echo "This is second line" >> file1.txt
```

Step 4 Verify File Content

Run:

```bash id="wrq5zd"
cat file1.txt
```

You should see:

```bash id="34mfpy"
Hello Git
This is second line
```

Step 5 Check Git Status

Run:

```bash id="0x8mml"
git status
```

You will notice:

```bash id="iknjg0"
modified: file1.txt
```

Meaning:
Git detected changes in existing file.

Step 6 Add Modified File to Staging Area

Run:

```bash id="r2a89g"
git add file1.txt
```

Step 7 Verify Staging

Run:

```bash id="qgq66m"
git status
```

You should see:

```bash id="7k3e8k"
Changes to be committed
```

Step 8 Commit Modified File

Run:

```bash id="tdpl08"
git commit -m "Modified file1.txt"
```

Now Git stores updated version of the file.

Step 9 Create Another New File

Run:

```bash id="t6z3hl"
echo "This is second file" > file2.txt
```

Step 10 Verify Files

Run:

```bash id="ejwppv"
ls
```

You should see:

```bash id="rm2mqt"
file1.txt
file2.txt
```

Step 11 Check Git Status

Run:

```bash id="hv4hqq"
git status
```

You will notice:

```bash id="k7mj9z"
Untracked files:
file2.txt
```

Meaning:
Git sees the new file
But it is not tracked yet.

Step 12 Add New File to Staging

Run:

```bash id="6iqmzh"
git add file2.txt
```

Step 13 Commit New File

Run:

```bash id="k9o7qs"
git commit -m "Added file2.txt"
```

Step 14 Verify Commit History

Run:

```bash id="9z9nqo"
git log --oneline
```

You will now see multiple commits.

Expected Learning Outcome

After completing this lab students should understand:

How Git detects file modifications

Difference between modified and staged state

How to commit updated versions of files

How to add new files into existing repository

How Git tracks multiple files and versions
