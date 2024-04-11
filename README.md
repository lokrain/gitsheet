## Working with Git in IntelliJ IDEA:

### Creating a Git Repository:

#### Initialize Repository:
- **When to Use:** To start tracking changes in a new or existing project.
- **UI:** 
  - For an empty folder:
    - Right-click on the folder where you want to initialize the repository, then select "Git -> Initialize Repository" from the context menu.
  - For a folder with existing files:
    - Navigate to the project directory, right-click on it, then select "Git -> Add" from the context menu to stage all files.
    - Next, right-click on the project directory again, and this time select "Git -> Commit Directory" from the context menu to create the initial commit.
- **CLI:**
  - `cd /path/to/project`: Navigate to the project directory in the terminal.
  - `git init`: Initialize a new Git repository in the current directory.
  - `git add .`: Stage all existing files for commit.
  - `git commit -m "Initial commit"`: Commit the staged changes with a descriptive message.

#### Clone Repository:
- **When to Use:** To copy a remote repository to your local machine.
- **UI:** 
  - Click on "Get from Version Control" on the welcome screen or go to "VCS -> Get from Version Control" in the toolbar, then enter the repository URL and choose the directory to clone into.
- **CLI:**
  - `git clone <repository-url>`: Clone the remote repository to your local machine.

### Committing Changes:

#### Stage Changes:
- **When to Use:** To prepare changes for committing.
- **UI:** 
  - In the Project tool window, right-click on the file(s) you want to stage, then select "Git -> Add" from the context menu.
- **CLI:**
  - `git add <file>`: Stage a specific file for commit.
  - `git add .`: Stage all changes in the working directory for commit.

#### Commit Changes:
- **When to Use:** To save staged changes to the repository.
- **UI:** 
  - Click on "Commit" in the toolbar or go to "VCS -> Commit" in the menu.
- **CLI:**
  - `git commit -m "Commit message"`: Commit staged changes with a descriptive message.

### Pushing Changes:

#### Push to Remote:
- **When to Use:** To upload committed changes to a remote repository.
- **UI:** 
  - Click on "Push" in the toolbar or go to "VCS -> Git -> Push" in the menu.
- **CLI:**
  - `git push origin <branch-name>`: Push committed changes to the remote repository.

### Pulling Changes:

#### Pull from Remote:
- **When to Use:** To fetch and integrate changes from a remote repository into your local repository.
- **UI:** 
  - Click on "Pull" in the toolbar or go to "VCS -> Git -> Pull" in the menu.
- **CLI:**
  - `git pull origin <branch-name>`: Pull changes from the remote repository into your local repository.

### Branching:

#### Create Branch:
- **When to Use:** To create a new branch for working on a feature or bug fix.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Branches" tab, and finally click on the "+" button to create a new branch.
- **CLI:**
  - `git checkout -b <branch-name>`: Create a new branch and switch to it.

#### Switch Branch:
- **When to Use:** To switch between branches in your repository.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Branches" tab, and finally double-click on the desired branch.
- **CLI:**
  - `git checkout <branch-name>`: Switch to the specified branch.

#### Merge Branch:
- **When to Use:** To integrate changes from one branch into another.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Branches" tab, and finally right-click on the branch you want to merge into, and select "Merge into Current" or "Merge into Selected" from the context menu.
- **CLI:**
  - `git merge <branch-name>`: Merge the specified branch into the current branch.

### Resolving Conflicts:

#### Resolve Conflicts:
- **When to Use:** To manually resolve conflicts that occur during a merge or rebase operation.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Log" tab, and finally double-click on the commit with merge conflicts to open the merge tool.
- **CLI:**
  - Resolve conflicts manually in the affected files, then stage the changes and commit the merge.

### Viewing History:

#### View Commit History:
- **When to Use:** To view a list of commits in the repository.
- **UI:** 
  - Click on "Log" in the toolbar or go to "VCS -> Git -> Show History" in the menu.
- **CLI:**
  - `git log`: View commit history in the terminal.

#### View File History:
- **When to Use:** To see the history of changes made to a specific file.
- **UI:** 
  - Right-click on the file in the Project tool window, then select "Git -> Show History" from the context menu.
- **CLI:**
  - `git log <file>`: View commit history for a specific file.

### Undoing Changes:

#### Discard Changes:
- **When to Use:** To discard changes made to a file since the last commit.
- **UI:** 
  - Right-click on the file in the Project tool window, then select "Git -> Revert" from the context menu.
- **CLI:**
  - `git checkout -- <file>`: Discard changes made to a specific file.

#### Reset to Commit:
- **When to Use:** To reset the repository to a previous commit.
- **UI:** 
  - Click on "Reset" in the toolbar or go to "VCS -> Git -> Reset" in the menu, then select the desired commit to reset to.
- **CLI:**
  - `git reset --hard <commit>`: Reset the repository to the specified commit.

### Other Operations:

#### Ignore Files:
- **When to Use:** To prevent certain files or directories from being tracked by Git.
- **UI:** 
  - Create a file named ".gitignore" in the project root, then add file patterns to it (e.g., "*.log" to ignore all log files).
- **CLI:**
  - Create a file named ".gitignore" in the project root, then add file patterns to it using a text editor.

#### Resolve Merge Conflicts:
- **When to Use:** To manually resolve conflicts that occur during a merge operation.
- **UI:** 
  - Open the files with conflicts in the editor, then resolve conflicts manually by editing the files.
- **CLI:**
  - Open the files with conflicts in a text editor, then resolve conflicts manually by editing the files.

#### Revert Commit:
- **When to Use:** To undo the changes introduced by a specific commit.
- **UI:** 
  - Right-click on the commit in the Log tool window, then select "Revert Commit" from the context menu.
- **CLI:**
  - `git revert <commit>`: Create a new commit that undoes the changes made by the specified commit.

#### Stash Changes:
- **When to Use:** To temporarily store changes that are not ready to be committed.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Log" tab, and finally click on the "Stash Changes" button.
- **CLI:**
  - `git stash`: Temporarily store changes in the stash.

#### Apply Stash:
- **When to Use:** To apply changes stored in the stash to the working directory.
- **UI:** 
  - Click on "Git" in the status bar at the bottom right, then click on the "Log" tab, and finally right-click on the desired stash and select "Apply Stash" from the context menu.
- **CLI:**
  - `git stash apply`: Apply changes stored in the stash to the working directory.

#### Cherry-pick Commit:
- **When to Use:** To apply the changes introduced by a specific commit to the current branch.
- **UI:** 
  - Right-click on the commit in the Log tool window, then select "Cherry-pick Commit" from the context menu.
- **CLI:**
  - `git cherry-pick <commit>`: Apply the changes introduced by the specified commit to the current branch.

