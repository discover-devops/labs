# Lab Configure SSH Authentication Between Local Machine and GitHub

Hello Students

In this lab you are going to learn:

How to generate SSH key

How to configure SSH authentication

How to add SSH public key into GitHub

How to establish secure communication between local machine and GitHub

---

# WHAT IS SSH AUTHENTICATION

SSH authentication allows:

* secure communication
* passwordless authentication
* encrypted GitHub access

Instead of username and password:

* GitHub verifies your SSH key

---

# STEP 1 Open Git Bash

Open:
Git Bash

on Windows laptop.

---

# STEP 2 Check Existing SSH Keys

Run:

```bash id="ssh1"
ls -al ~/.ssh
```

If SSH keys already exist you may see:

```text id="ssh2"
id_rsa
id_rsa.pub
```

or

```text id="ssh3"
id_ed25519
id_ed25519.pub
```

---

# STEP 3 Generate New SSH Key

Run:

```bash id="ssh4"
ssh-keygen -t ed25519 -C "yourmail@example.com"
```

Example:

```bash id="ssh5"
ssh-keygen -t ed25519 -C "rahul@gmail.com"
```

---

# STEP 4 Save SSH Key

Git Bash asks:

```text id="ssh6"
Enter file in which to save the key
```

Press:
Enter

to accept default location.

---

# STEP 5 Set Passphrase

Git asks:

```text id="ssh7"
Enter passphrase
```

You can:

* provide passphrase
  or
* press Enter for no passphrase

---

# STEP 6 Verify SSH Key Creation

Run:

```bash id="ssh8"
ls ~/.ssh
```

You should see:

```text id="ssh9"
id_ed25519
id_ed25519.pub
```

---

# STEP 7 Start SSH Agent

Run:

```bash id="ssh10"
eval "$(ssh-agent -s)"
```

---

# STEP 8 Add SSH Private Key to SSH Agent

Run:

```bash id="ssh11"
ssh-add ~/.ssh/id_ed25519
```

---

# STEP 9 Copy Public SSH Key

Run:

```bash id="ssh12"
cat ~/.ssh/id_ed25519.pub
```

Copy complete output.

Example:

```text id="ssh13"
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAxxxxxxxx rahul@gmail.com
```

---

# STEP 10 Login to GitHub

Open browser and login to:

```text id="ssh14"
https://github.com
```

---

# STEP 11 Open GitHub Settings

Click:
Profile Picture

Then:
Settings

---

# STEP 12 Open SSH Keys Section

Navigate to:

```text id="ssh15"
SSH and GPG Keys
```

---

# STEP 13 Add New SSH Key

Click:

```text id="ssh16"
New SSH Key
```

---

# STEP 14 Provide SSH Key Details

Title:

```text id="ssh17"
Windows Laptop SSH Key
```

Key:
Paste copied public key.

---

# STEP 15 Add SSH Key

Click:

```text id="ssh18"
Add SSH Key
```

GitHub may ask password confirmation.

---

# STEP 16 Test SSH Authentication

Run:

```bash id="ssh19"
ssh -T git@github.com
```

Expected output:

```text id="ssh20"
Hi username
You have successfully authenticated
```

---

# STEP 17 Clone Repository Using SSH

Go to GitHub repository.

Click:
Code

Select:
SSH

Copy SSH URL.

Example:

```text id="ssh21"
git@github.com:yourusername/git-remote-lab.git
```

---

# STEP 18 Clone Repository

Run:

```bash id="ssh22"
git clone git@github.com:yourusername/git-remote-lab.git
```

---

# EXPECTED LEARNING OUTCOME

After completing this lab students should understand:

How SSH authentication works

Difference between HTTPS and SSH authentication

How GitHub validates SSH keys

How secure passwordless authentication is established

How to securely connect local machine with GitHub repository
