# Quick Fix for Git Errors

## Problem
You're getting errors because Git doesn't know your identity. Here's how to fix it:

## Solution

Run these commands in your terminal (PowerShell) in the project directory:

### Step 1: Configure Git Identity

```powershell
# Set your name (use your actual name)
git config --global user.name "Mayank Gawade"

# Set your email (use your GitHub email or the one associated with your GitHub account)
git config --global user.email "mayankgawade211@gmail.com"
```

### Step 2: Verify Configuration

```powershell
# Check if it's set correctly
git config --global user.name
git config --global user.email
```

### Step 3: Now Commit and Push

```powershell
# Stage all files
git add .

# Create the commit (this should work now)
git commit -m "Initial commit: Portfolio website"

# Check if remote already exists (if it does, skip the next command)
git remote -v

# If remote doesn't exist, add it (replace mayg05 with your username if different)
git remote add origin https://github.com/mayg05/mayankgawade-portfolio.git

# If remote already exists and you need to update it:
git remote set-url origin https://github.com/mayg05/mayankgawade-portfolio.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

## If You Still Get Errors

### Error: "remote origin already exists"
- This is fine! Just skip the `git remote add` command
- If you need to change the URL, use: `git remote set-url origin https://github.com/mayg05/mayankgawade-portfolio.git`

### Error: "Authentication failed"
- GitHub no longer accepts passwords
- You need a Personal Access Token:
  1. Go to GitHub.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
  2. Generate new token (classic)
  3. Select scope: `repo` (full control of private repositories)
  4. Copy the token
  5. Use the token as your password when pushing

### Error: "src refspec main does not match any"
- This means the commit failed
- Make sure you completed Step 1 (configuring Git identity) first
- Then try committing again

## Quick Copy-Paste Solution

Copy and paste this entire block into PowerShell:

```powershell
git config --global user.name "Mayank Gawade"
git config --global user.email "mayankgawade211@gmail.com"
git add .
git commit -m "Initial commit: Portfolio website"
git branch -M main
git push -u origin main
```

If you get an authentication error, you'll need to create a Personal Access Token on GitHub first.
