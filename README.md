# Question 1 - Project Initialization & First Push

## Objective

Initialize a local Git repository and connect it to GitHub for version control.

---

# Step 1: Initialize Git Repository

Command:

```bash
git init
```

Explanation:

- Creates a new Git repository
- Generates a hidden `.git` folder

---

# Step 2: Create Python File
File name:

```text
app.py
```

After Creating Add:

```python
print("Hello git hub - this is my assessment for git hub")
```


---

# Step 3: Check Git Status

Command:

```bash
git status
```

Explanation:

- Shows repository status
- Displays untracked files

---

# Step 4: Stage Files

Command:

```bash
git add app.py
```

Explanation:

- Adds `app.py` to staging area

---

# Step 5: Commit Changes

Command:

```bash
git commit -m "Initial commit with app.py"
```

Explanation:

- Saves project snapshot into Git history

---

# Step 6: Add Remote Repository

Command:

```bash
git remote add origin [repository_url](https://github.com/vigneshreddy2910-gif/Git-GitHub-Assessment_Vignesh)
```

Explanation:

- Connects local repository with GitHub

---

# Step 7: Verify Remote

Command:

```bash
git remote -v
```

Explanation:

- Displays configured remote repositories

---

# Step 8: Push Code to GitHub

Command:

```bash
git push -u origin main
```

Explanation:

- Uploads local project to GitHub
- Sets upstream tracking branch


---
# Reference Image
<img width="1613" height="700" alt="image" src="https://github.com/user-attachments/assets/af5b272d-5cd5-4ef5-8713-1763ee489505" />


# Conclusion

Successfully initialized a Git repository, tracked project files, committed changes, and pushed the project to GitHub.

---

# Question 2 - Working with Changes & History

## Objective

Track file modifications and manage commit history effectively.

---

# Step 1: Modify app.py

Added new functionality to the Python application.

Example:

```python
print("Added a new feature to the code")
```

---

# Step 2: Check Repository Status

Command:

```bash
git status
```

Explanation:

- Shows modified files before staging

---

# Step 3: View File Differences

Command:

```bash
git diff
```

Explanation:

- Displays exact code changes

---

# Step 4: Stage Specific Changes

Command:

```bash
git add -p
```

Explanation:

- Allows interactive staging

---

# Step 5: Commit Changes

Command:

```bash
git commit -m "Added a newFeature"
```

---

# Step 6: Add Another Change

Added additional improvements to `app.py`.
Example:

```python
print("This is bug fix for the new feature")
```
---

# Step 7: Stage All Changes

Command:

```bash
git add .
```

---

# Step 8: Create Another Commit

Command:

```bash
git commit -m "Added Bug Fix"
```

---

# Step 9: View Full Commit History

Command:

```bash
git log
```

---

# Step 10: View Compact Commit History

Command:

```bash
git log --oneline
```

---

# Reference Images
<img width="1041" height="793" alt="image" src="https://github.com/user-attachments/assets/a99dd42d-4818-4ec5-a242-6cee046cbdd4" />

---

<img width="1018" height="605" alt="image" src="https://github.com/user-attachments/assets/8bd3f232-a431-43cf-9f5a-acab2d48e7d2" />


---
# Conclusion

Successfully managed project changes using Git tracking and commit history commands.

---

# Question 3 - Branching & Feature Development

## Objective

Develop new features in separate branches without affecting the main project.

---

# Step 1: Create Feature Branch

Command:

```bash
git checkout -b feature-update
```

Explanation:

- Creates and switches to a new feature branch

---

# Step 2: Verify Branches

Command:

```bash
git branch
```

Explanation:

- Displays available branches
- Indicates active branch using `*`

---

# Step 3: Modify app.py

Added new feature logic to the application.

Example:

```python
print("new feature feature-1 is added in the new branch")
```

---

# Step 4: Stage Changes

Command:

```bash
git add app.py
```

---

# Step 5: Commit Feature Changes

Command:

```bash
git commit -m "Added new feature in a branch"
```

Explanation:

- Saves feature updates into Git history

---

# Step 6: Switch Back to Main Branch

Command:

```bash
git checkout main
```

---

# Step 7: Merge Feature Branch

Command:

```bash
git merge feature-update
```

Explanation:

- Integrates feature branch into main branch

---

# Step 8: Verify Merge History

Command:

```bash
git log --oneline
```

Explanation:

- Displays concise commit history
- Confirms merge success

---

# Step 9: Delete Feature Branch Safely

Command:

```bash
git branch -d feature-update
```

Explanation:

- Safely deletes merged branch

---

# Reference Images
<img width="1147" height="577" alt="image" src="https://github.com/user-attachments/assets/9efe1d89-a4ab-40dc-a689-eb546b4c4599" />

<img width="1123" height="205" alt="image" src="https://github.com/user-attachments/assets/4685d6f5-c897-45fe-a50c-99b3fee351ed" />

---

# Step 10: Create Dummy Branch

Command:

```bash
git checkout -b dummy-branch
```

Explanation:

- Creates temporary branch for testing force delete

---

# Step 11: Commit Dummy Changes

Command:

```bash
git commit -m "Dummy commit temporary changes"
```

---

# Step 12: Attempt Safe Delete

Command:

```bash
git branch -d dummy-branch
```

Explanation:

- Git prevents deletion because branch is unmerged

---

# Step 13: Force Delete Branch

Command:

```bash
git branch -D dummy-branch
```

Explanation:

- Force deletes unmerged branch

---

# Safe Delete vs Force Delete

| Command | Purpose |
|---|---|
| `git branch -d` | Safely delete merged branch |
| `git branch -D` | Force delete unmerged branch |

---

# Reference Imange
<img width="1087" height="135" alt="image" src="https://github.com/user-attachments/assets/cc433d0c-6e46-48bd-a8fa-d7aa2f14efe0" />
<img width="1118" height="247" alt="image" src="https://github.com/user-attachments/assets/ad84f791-ed17-436c-a559-df3644ba1df4" />

---

# Conclusion

Successfully demonstrated Git branching workflows including:

- Branch creation
- Feature isolation
- Branch merging
- Commit verification
- Safe branch deletion
- Force deletion of unmerged branches


--

# Question 4 - Handling Errors Using Stash, Reset, and Revert

## Objective

Learn how to manage unfinished work and safely undo mistakes using Git.

---

# Step 1: Modify app.py Without Commit

Added temporary unfinished changes to the application.

---

# Step 2: Check Git Status

Command:

```bash
git status
```

Explanation:

- Displays modified and untracked files

---

# Step 3: Stash Changes Including Untracked Files

Command:

```bash
git stash -u
```

Explanation:

- Temporarily saves:
  - modified files
  - staged files
  - untracked files

---

# Step 4: View Stash List

Command:

```bash
git stash list
```

Explanation:

- Displays saved stash entries

---

# Step 5: Restore Stashed Changes

Command:

```bash
git stash apply
```

Explanation:

- Restores stashed changes back into working directory

---


# Reference Images
<img width="977" height="711" alt="image" src="https://github.com/user-attachments/assets/1c3cc084-01a8-4411-9fa9-abd993d9b874" />

---
<img width="1031" height="750" alt="image" src="https://github.com/user-attachments/assets/4bd5c725-828b-4148-b034-1ba16b029258" />

---
<img width="906" height="806" alt="image" src="https://github.com/user-attachments/assets/3a580543-f6f6-4985-813f-0d72aae5b7b3" />

---
<img width="1175" height="350" alt="image" src="https://github.com/user-attachments/assets/ff1ca806-4503-4152-9510-7b11a6e0da74" />


# Step 7: Commit Restored Changes

Command:

```bash
git add .
git commit -m "Restored stashed feature work"
```

---

# Step 8: Create Incorrect Commit

Command:

```bash
git commit -m "Added incorrect implementation"
```

Explanation:

- Simulates accidental buggy commit

---

# Step 9: Undo Commit Using Reset

Command:

```bash
git reset --hard HEAD~1
```

Explanation:

- Permanently removes latest commit
- Restores repository to previous state

---

# Step 10: Add Corrected Implementation

Corrected the application logic and committed changes.

---

# Step 11: Create Another Commit

Command:

```bash
git commit -m "Added another feature"
```

---

# Step 12: Undo Commit Using Revert

Command:

```bash
git revert HEAD
```

Explanation:

- Creates new commit that reverses previous commit
- Keeps history intact

---

# Step 13: Verify Commit History

Command:

```bash
git log --oneline
```

Explanation:

- Displays compact commit history

---

# Reset vs Revert

| Feature | Reset | Revert |
|---|---|---|
| Removes commit history | Yes | No |
| Creates new commit | No | Yes |
| Safe for shared repositories | No | Yes |
| Rewrites Git history | Yes | No |

---

# Reference Images
<img width="1116" height="733" alt="image" src="https://github.com/user-attachments/assets/20930a8c-b148-4af4-a459-304b8725635f" />

---
<img width="1126" height="811" alt="image" src="https://github.com/user-attachments/assets/1c114373-cb68-4be1-a8cc-ca9ab752ae87" />

---
<img width="1243" height="681" alt="image" src="https://github.com/user-attachments/assets/37bde1d8-04db-443b-834d-05c8da678826" />

# Conclusion

Successfully demonstrated advanced Git workflows including:

- Stashing unfinished work
- Restoring stashed changes
- Undoing commits using reset
- Safely reversing commits using revert
- Managing Git commit history
