Hello Git!
Feature 1 added!
This line was added on GitHub!
"This line was added on GitHub!" actually




Step 1: Install Git

Download from 👉 https://git-scm.com

Run installer → Keep defaults → Finish installation.

Verify:

git --version

Step 2: Configure Git (Global Settings)

Set your identity once:

git config --global user.name "Ansal P Chaubey"
git config --global user.email "ansalchaubey2006@gmail.com"
git config --global color.ui auto

Step 3: Create a GitHub Repository

Go to https://github.com

Create a new repository (e.g., git-lab).

Copy the HTTPS URL (like https://github.com/username/git-lab.git)

Step 4: Create Local Repository
cd C:\git-lab
git init

Step 5: Create and Add a File
echo "Hello Git!" > readme.txt
git add readme.txt
git commit -m "First commit"

Step 6: Connect Local to Remote
git remote add origin https://github.com/<username>/git-lab.git

Step 7: Rename Default Branch (Optional but Common)

GitHub uses main instead of master:

git branch -M main

Step 8: Push to GitHub
git push -u origin main


✅ This uploads your code to GitHub for the first time.

Step 9: Verify

Check your repository online — readme.txt should appear.

🧭 Useful Commands After Setup
🔹 Check Status & History
git status       # Shows untracked or modified files
git log          # Shows commit history

🌿 Branching and Merging
🔹 Create and Switch Branch
git branch feature1       # Create new branch
git checkout feature1     # Switch to that branch


Now make a change:

echo "Feature 1 added!" >> readme.txt
git add readme.txt
git commit -m "Added feature1 update"

🔹 Merge Back to Main
git checkout main
git merge feature1


If everything merges cleanly:

Fast-forward
 readme.txt | 1 +
 1 file changed, 1 insertion(+)


🔹 Fetch (See Remote Changes)
git fetch


➡ Downloads the latest changes from GitHub,
but does not change your local files yet.

🔹 Merge (Apply Fetched Changes)
git merge


➡ Combines the fetched changes into your local branch.
If there are no conflicts, it will fast-forward smoothly.

🔹 Pull (Fetch + Merge Together)
git pull


➡ Shortcut command — it both fetches and merges in one go.
This keeps your local repo up to date with GitHub.
