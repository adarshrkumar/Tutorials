# A Complete Guide to Collaboration with GitHub Desktop

**Course Length:** 15-20 minutes
**Audience:** Beginners using GitHub Desktop. This guide covers the entire lifecycle, from creating a project to making your first collaborative contribution.
**Goal:** Learn the fundamental workflow for creating and contributing to a shared project using GitHub.

---

## Table of Contents

1.  [Step 1: Create the Shared Repository on GitHub](#1-step-1-create-the-shared-repository-on-github)
2.  [Step 2: Clone the Repository to Your Computer](#2-step-2-clone-the-repository-to-your-computer)
3.  [Step 3: The Core Collaboration Workflow](#3-step-3-the-core-collaboration-workflow)
    *   [A. Sync Your `main` Branch (`Fetch`/`Pull`)](#a-sync-your-main-branch-fetchpull)
    *   [B. Create a New Branch](#b-create-a-new-branch)
    *   [C. Make and Commit Changes](#c-make-and-commit-changes)
    *   [D. Share Your Branch (`Push`)](#d-share-your-branch-push)
4.  [Step 4: Create a Pull Request (PR)](#4-step-4-create-a-pull-request-pr)
5.  [Step 5: Review and Merge the PR (For Maintainers)](#5-step-5-review-and-merge-the-pr-for-maintainers)
6.  [Step 6: Clean Up Your Workspace](#6-step-6-clean-up-your-workspace)
7.  [Bonus: Handling Basic Merge Conflicts](#7-bonus-handling-basic-merge-conflicts)

---

### 1. Step 1: Create the Shared Repository on GitHub

Every project starts with a central "remote" repository. One person on the team will create this on the GitHub website.

1.  Log in to [GitHub.com](https://github.com).
2.  In the top-right corner, click the **`+`** icon and select **"New repository"**.
3.  **Repository name:** Choose a short, memorable name for your project (e.g., `team-website-project`).
4.  **Description:** Add a brief, one-sentence description of the project.
5.  **Public vs. Private:** Choose `Private` if you want to control who sees and contributes to your project.
6.  **Initialize this repository with:**
    *   **[✅] Add a README file:** **This is highly recommended.** A README explains what your project is. It also ensures the repository isn't empty, which makes it easier to clone.
    *   **[✅] Add .gitignore:** This is a special file that tells Git to ignore certain files (like temporary files or secret keys). Select a template from the dropdown that matches your project's technology (e.g., `Node`, `Python`).
7.  Click the green **"Create repository"** button.

Your remote repository is now live on GitHub! Next, you need to invite your collaborators. Go to **Settings > Collaborators > Add people** to grant them access.

### 2. Step 2: Clone the Repository to Your Computer

Now, every team member (including the person who created it) needs to get a local copy of the project.

1.  On the project's page on GitHub.com, click the green **"<> Code"** button.
2.  Select the **"Open with GitHub Desktop"** option. Your browser may ask for permission to open the application.
3.  GitHub Desktop will launch and ask where you want to save the project on your computer (the "Local Path").
4.  Choose a location and click **"Clone"**.

The application will download the repository, and you now have a local copy ready for work.

### 3. Step 3: The Core Collaboration Workflow

This is the cycle you will repeat for every new feature or bug fix.

**The Golden Rule:** Never work directly on the `main` branch! Always create a new branch for your changes.

#### A. Sync Your `main` Branch (`Fetch`/`Pull`)

Before starting any work, ensure your local `main` branch has the latest changes from the team.

1.  In GitHub Desktop, use the **"Current Branch"** dropdown at the top to select the `main` branch.
2.  Click the **"Fetch origin"** button in the top bar. If others have made changes, this button will turn into **"Pull origin"**. Click it to download and integrate the latest updates.

#### B. Create a New Branch

A branch is a safe, isolated space to make changes without affecting the stable `main` branch.

1.  Click on the **"Current Branch"** dropdown again.
2.  Click the blue **"New Branch"** button.
3.  Give your branch a descriptive name (e.g., `feature/add-contact-page` or `fix/navbar-bug`).
4.  Click **"Create Branch"**. GitHub Desktop automatically switches you to your new branch.

#### C. Make and Commit Changes

Make changes to the project files using your favorite code editor. As you save files, they will appear in the **"Changes"** tab in GitHub Desktop.

1.  Review the changed files listed on the left.
2.  Check the boxes next to the files you want to include in this commit.
3.  At the bottom-left, enter a short, clear message in the **"Summary"** field.
4.  Click the blue **"Commit to `branch-name`"** button.

#### D. Share Your Branch (`Push`)

Your new branch and its commits only exist on your computer. To share them, you need to **push** them to GitHub.

1.  Click the blue **"Publish branch"** button in the main panel. This sends your branch and all its commits to the remote repository.
    *   *Note: For any future commits on this same branch, this button will read **"Push origin"**.*

### 4. Step 4: Create a Pull Request (PR)

A Pull Request is a formal proposal to merge your changes from your feature branch into the `main` branch. It's where code review happens.

1.  Immediately after you publish your branch, GitHub Desktop will prompt you. Click the **"Create Pull Request"** button.
2.  This opens the GitHub website in your browser, pre-filled with your branch information.
3.  Give your PR a clear title and a description of the changes you made.
4.  Click **"Create pull request"**.

### 5. Step 5: Review and Merge the PR (For Maintainers)

The project owner or a designated maintainer will now get a notification. They will review your PR on GitHub.com.

1.  They'll go to the **"Pull requests"** tab in the repository.
2.  They can review the code, look at the changes, and leave comments.
3.  If everything looks good, they will click the green **"Merge pull request"** button, and then **"Confirm merge"**.

Your changes are now officially part of the `main` branch!

### 6. Step 6: Clean Up Your Workspace

Once your PR is merged, your feature branch is no longer needed. It's good practice to clean up.

1.  In GitHub Desktop, switch back to the **`main`** branch.
2.  **Pull** the latest changes by clicking **"Pull origin"** (this will download your recently merged work).
3.  Go to the menu bar and select **Branch > Delete...** and choose your old feature branch.

You're now back on an up-to-date `main` branch, ready to start the workflow again for your next task!

### 7. Bonus: Handling Basic Merge Conflicts

A merge conflict happens when two people change the same line in the same file. When you try to `pull`, GitHub Desktop will warn you.

1.  A dialog will appear listing the conflicted files. Click **"Open in [your editor]"**.
2.  In your code editor, you will see markers like `<<<<<<<`, `=======`, and `>>>>>>>`.
    *   The code between `<<<<<<<` and `=======` is **your** conflicting change.
    *   The code between `=======` and `>>>>>>>` is the **incoming** change.
3.  **Manually edit the file.** Delete all the `<<<`, `===`, `>>>` markers and decide what the final, correct code should look like. Save the file.
4.  Back in GitHub Desktop, once all conflicts are resolved, a bar will appear at the top. Click **"Commit merge"** to finish.

Conflicts are a normal part of teamwork. Learning to resolve them is a key skill!
