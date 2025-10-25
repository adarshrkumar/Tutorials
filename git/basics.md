# A Quick Guide to Collaboration with GitHub Desktop

**Course Length:** 10-15 minutes
**Audience:** Beginners who have GitHub Desktop installed and are new to collaborating on a shared project.
**Goal:** Learn the fundamental workflow for contributing to a shared project using the GitHub Desktop application.

---

## Table of Contents

1.  [The Core Concept: Remote vs. Local](#1-the-core-concept-remote-vs-local)
2.  [Step 1: Get the Code (`Clone` & `Fetch`)](#2-step-1-get-the-code-clone--fetch)
3.  [Step 2: Create Your Workspace (New `Branch`)](#3-step-2-create-your-workspace-new-branch)
4.  [Step 3: Do Your Work (`Commit`)](#4-step-3-do-your-work-commit)
5.  [Step 4: Share Your Work (`Push`)](#5-step-4-share-your-work-push)
6.  [Step 5: Propose Your Changes (The Pull Request)](#6-step-5-propose-your-changes-the-pull-request)
7.  [Step 6: Update and Clean Up](#7-step-6-update-and-clean-up)
8.  [Bonus: Handling Basic Merge Conflicts](#8-bonus-handling-basic-merge-conflicts)

---

### 1. The Core Concept: Remote vs. Local

When you collaborate, there are at least two copies of the project:

*   **Remote Repository (`origin`):** This is the single source of truth, hosted on GitHub.com. Everyone on the team trusts this version.
*   **Local Repository:** This is the copy on *your* computer where you do all your work.

The goal is to keep your local copy in sync with the remote, contribute your changes safely in a separate branch, and then merge your work back into the remote repository.

### 2. Step 1: Get the Code (`Clone` & `Fetch`)

First, you need a local copy of the project.

#### A. If it's your first time working on the project:

Use **Clone** to download the entire project from GitHub to your computer.

1.  On the project's page on GitHub.com, click the green **"Code"** button and select the **"Open with GitHub Desktop"** option.
2.  Alternatively, in GitHub Desktop, go to **File > Clone Repository**.
3.  In the dialog, select the **URL** tab, paste the repository URL, choose a local path on your computer, and click **"Clone"**.

#### B. If you already have the project:

Before you start any work, make sure your local `main` branch is up-to-date.

1.  In GitHub Desktop, select the project from the "Current Repository" list.
2.  Make sure the "Current Branch" at the top says **`main`**.
3.  Click the **"Fetch origin"** button in the top bar. If there are new changes on the remote, this button will change to **"Pull origin"**. Click it to download the latest updates.

### 3. Step 2: Create Your Workspace (New `Branch`)

**The Golden Rule:** Never work directly on the `main` branch!

Always create a new **branch** for each new feature or bug fix. A branch is a safe, isolated space to make changes.

1.  Click on the **"Current Branch"** dropdown at the top of the application.
2.  Click the blue **"New Branch"** button.
3.  Give your branch a descriptive name (e.g., `feature/add-user-login` or `fix/header-alignment`).
4.  Click **"Create Branch"**.

GitHub Desktop automatically switches you to your new branch.

### 4. Step 3: Do Your Work (`Commit`)

Now, make changes to the project files using your favorite code editor. As you save files, they will appear in the **"Changes"** tab in GitHub Desktop.

1.  Review the changed files listed on the left.
2.  Check the boxes next to the files you want to include in this commit. You can check the box at the top to select all files.
3.  At the bottom-left, enter a short, clear message in the **"Summary"** field (e.g., "Feat: Add user login form component").
4.  Optionally, add more detail in the **"Description"** field.
5.  Click the blue **"Commit to `branch-name`"** button.

### 5. Step 4: Share Your Work (`Push`)

Your new branch and your commits only exist on your computer. To share them, you need to **push** them to the remote repository on GitHub.

After you make your first commit on a new branch, a blue button will appear in the main panel.

1.  Click the **"Publish branch"** button.

This pushes your branch and its commits to GitHub. For any future commits on this same branch, this button will read **"Push origin"**.

### 6. Step 5: Propose Your Changes (The Pull Request)

Now that your branch is on GitHub, you can ask for it to be merged into `main`. This is done via a **Pull Request** (PR).

1.  Immediately after you publish or push a branch, a new option will appear in GitHub Desktop. Click the **"Create Pull Request"** button.
2.  This will open the GitHub website in your browser, pre-filled with your branch information.
3.  Ensure the "base" branch is `main` and the "compare" branch is your feature branch.
4.  Give your PR a clear title and description.
5.  Click **"Create pull request"**.

Your team can now review your code online, leave comments, and a maintainer will **merge** it.

### 7. Step 6: Update and Clean Up

Once your Pull Request is merged on GitHub.com, your work is done! The last step is to clean up your local workspace.

1.  In GitHub Desktop, switch back to the **`main`** branch using the "Current Branch" dropdown.
2.  **Pull** the latest changes (which now include your merged work) by clicking **"Pull origin"**.
3.  Go to the menu bar and select **Branch > Delete...** and choose your old feature branch. GitHub Desktop will warn you if it hasn't been merged yet.

You are now ready to start the cycle again for the next task!

### 8. Bonus: Handling Basic Merge Conflicts

Sometimes, you and a teammate change the same line in the same file. When you try to `pull` changes, GitHub Desktop will stop and tell you there is a **merge conflict**.

1.  A dialog will appear saying "Resolve conflicts before merging".
2.  It will list the conflicted files. Click **"Open in [your editor]"**.
3.  In your code editor, you will see markers like `<<<<<<<`, `=======`, and `>>>>>>>`.
    *   The code between `<<<<<<< HEAD` and `=======` is **your** conflicting change.
    *   The code between `=======` and `>>>>>>>` is the **incoming** change from the remote.
4.  **Manually edit the file.** Delete the markers and decide what the final code should look like. Save the file.
5.  Go back to GitHub Desktop. The conflict warning for the file you fixed will be gone.
6.  Once all conflicts are resolved, a bar will appear at the top. Click **"Commit merge"** to finish the process.

Don't be afraid of conflicts; they are a normal part of teamwork!

---

**Congratulations!** You now know the fundamental workflow for collaborating on a project with GitHub Desktop.
