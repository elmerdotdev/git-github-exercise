### Extended Git and GitHub Exercise: Mastering Git Commands

**Objective**: This exercise aims to teach students how to manage a Git repository, including using `git add`, `git commit`, `git restore`, `git mv`, `git rm`, `git clean`, `git revert`, `git log`, and how to sync with a GitHub repository.

#### Setup
1. Create a new directory called `git-github-exercise` and navigate into it:
   - `mkdir git-github-exercise`
   - `cd git-github-exercise`

2. Initialize a new Git repository:
   - `git init`

#### Part 1: Basic Add and Commit
1. Create a `README.md` file and write a simple welcome message:
   - `echo "# Welcome to My Git Project" > README.md`

2. Stage and commit the file:
   - `git add README.md`
   - `git commit -m "Add README.md with welcome message"`

#### Part 2: Updating and Using Git Restore
1. Modify the `README.md` file by adding a section about the project description:
   - `echo "\n## Description" >> README.md`
   - `echo "This project demonstrates basic Git and GitHub operations." >> README.md`

2. Stage and commit the changes:
   - `git add README.md`
   - `git commit -m "Update README.md with project description"`

3. Accidentally modify another section:
   - `echo "\nAccidental addition" >> README.md`

4. Restore the last accidental addition:
   - `git restore README.md`

#### Part 3: Advanced File Handling
1. Rename `README.md` to `INTRO.md`:
   - `git mv README.md INTRO.md`
   - `git commit -m "Rename README.md to INTRO.md"`

2. Accidentally add a temporary file:
   - `touch temp.txt`
   - `git add temp.txt`

3. Remove `temp.txt` from tracking and delete it:
   - `git rm temp.txt`
   - `git commit -m "Remove temporary file"`

4. Clean up any untracked files (like if `temp.txt` was never added):
   - `git clean -f`

#### Part 4: Using Git Log and Revert
1. Introduce a new change:
   - `echo "\nThis will be reverted soon." >> INTRO.md`
   - `git add INTRO.md`
   - `git commit -m "Add line to be reverted"`

2. Use `git log` to view the commit history:
   - `git log`

3. Revert the last commit:
   - `git revert HEAD --no-edit`

#### Part 5: Creating and Using a GitHub Repository
1. Create a new repository on GitHub named `git-github-exercise` (do not initialize with README, .gitignore, or License).

2. Link your local repository to your GitHub repository:
   - `git remote add origin https://github.com/yourusername/git-github-exercise.git`
   - Replace `yourusername` with your actual GitHub username.

3. Push your local repository to GitHub:
   - `git push -u origin main`

#### Part 6: Making Additional Changes and Pushing Again
1. Make additional changes to `INTRO.md`:
   - `echo "\nThis project helps to understand pushing to remote repositories." >> INTRO.md`
   - `git add INTRO.md`
   - `git commit -m "Update INTRO.md with remote repo info"`

2. Push the changes to GitHub:
   - `git push`

