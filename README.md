("""
✅ Uploading a Local Project from Visual Studio Code to GitHub Using Git

🟨 I opened VS Code and created a new folder using:
    mkdir <foldername>
    cd <foldername>

🟨 Before initializing Git, I ran:
    ls -a
This command lists all files, including hidden ones. Output:
    .  ..
- `.` means the current directory.
- `..` means the parent directory.

We use `ls -a` to check for hidden files like `.git`, `.gitignore`, etc.

🟨 I initialized Git in my project folder using:
    git init
This creates a hidden `.git` folder — the brain of Git — which tracks all commits, branches, remote connections, and changes.

🟨 After `git init`, running `ls -a` shows:
    .  ..  .git

🟨 I created files (e.g., main.py, index.html), wrote code, and saved them.

🟨 I created a repository on GitHub (with the same name for easy linking).

🟨 Checked the current branch using:
    git branch
Output was: * master

🟨 Since GitHub uses `main` by default, I renamed the local branch:
    git branch -m main

🟨 Then I added my files to Git's staging area:
    git add .

🟨 I saved the snapshot with a commit:
    git commit -m "First commit"

🟨 (Optional) Checked if remote link is added:
    git remote -v

🟨 Then I connected to my GitHub repository using:
    git remote add origin <your-repo-link>

🟨 Again, I checked the current branch using:
    git branch
If it's `master` and GitHub uses `main`, rename it:
    git branch -m master main

🟨 I pushed my code to GitHub:
    git push -u origin main

✅ Git Branches

🔹 Definition: A branch is a separate workspace to work on features or fixes without affecting the main code.

🎯 Real-life Example: Like writing a book — `main` is the published version, and each `feature` branch is like writing a new chapter separately.

🟢 Benefits of Branches:
- Work independently without breaking main code
- Collaborate with a team
- Safely test and experiment
- Manage multiple features or fixes

🔧 Git Branch Workflow:
1. View current branch:
    git branch
2. Create a new branch:
    git branch feature1
3. Switch to that branch:
    git checkout feature1
   OR create and switch together:
    git checkout -b feature1
4. Make changes, then:
    git add .
    git commit -m "Work on feature1"
5. Push to GitHub:
    git push -u origin feature1
6. Merge changes back into main:
    git checkout main
    git merge feature1
7. Delete a branch:
   - Local: git branch -d feature1
   - Remote: git push origin --delete feature1

🔀 Branch Naming Conventions:
- main: stable production code
- feature/*: new feature development (e.g., feature/login-page)
- bugfix/*: bug fixes (e.g., bugfix/login-error)
- hotfix/*: urgent production fix (e.g., hotfix/server-crash)
- release/*: pre-release preparations (e.g., release/v1.0.0)

📚 Git Flow Strategy:
A common branching model:
    main
    ├── feature/login
    ├── feature/payment
    ├── release/1.0.0
    └── hotfix/urgent-crash

🧨 Common Errors:
- `src refspec branch-name does not match any`: wrong branch name → fix: check with `git branch`
- `fatal: A branch named 'main' already exists.`: branch already exists → fix: switch to it
- `error: failed to push some refs`: branch mismatch → fix: use `-u` flag and correct branch name

💬 Final Tips:
- Name branches clearly (avoid random names like `abc123`)
- Always push with `git push -u origin branchname`
- Use `git branch -a` to see local + remote branches
- Clean unused branches regularly

🔄 Summary of Key Git Branch Commands:

Task                           | Command
------------------------------|-------------------------------
Check current branch           | git branch
Rename branch                 | git branch -m newname
Switch branches                | git checkout branchname
Create + switch to new branch | git checkout -b branchname
Merge a branch into main       | git checkout main → git merge branchname
Delete local branch            | git branch -d branchname
Delete remote branch           | git push origin --delete branchname

✅ Most Commonly Used Git Branch Commands:
- `git branch` (check current branch)
- `git branch -m main` (rename branch)
- `git checkout branchname` (switch to a branch)
- `git checkout -b newbranch` (create and switch)
- `git branch -d branchname` (delete local branch)


""")