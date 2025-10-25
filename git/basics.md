# A Guide to a Safe Git Workflow with GitHub Desktop (For Solo Projects)

**Course Length:** 15-20 minutes
**Audience:** Solo developers or beginners who want to learn professional Git habits on their own projects using GitHub Desktop.
**Goal:** To master the "feature branch" workflow, keeping your `main` branch clean and stable, even when working alone.

---

## Why Use This Workflow When You're Working Alone?

You might think branches and Pull Requests are only for teams. However, using this workflow on your own projects is one of the best habits you can build:

*   **`main` is Always Stable:** Your `main` branch remains a clean, working version of your project. You can confidently come back to it knowing it's not broken.
*   **Organized Features:** Each new idea or fix lives on its own branch. This makes your work organized and easy to track.
*   **Easy to Abandon Bad Ideas:** If a feature isn't working out, you can simply delete the branch without affecting your main project.
*   **Prepares You for Teamwork:** This is the *exact same workflow* used in professional software development teams. Practicing it now makes you ready for future collaboration.

## Table of Contents

1.  [Step 1: Create Your Project Repository on GitHub](#1-step-1-create-your-project-repository-on-github)
2.  [Step 2: Clone the Repository to Your Computer](#2-step-2-clone-the-repository-to-your-computer)
3.  [Step 3: The Development Cycle: Working on a New Feature](#3-step-3-the-development-cycle-working-on-a-new-feature)
    *   [A. Create a New Branch](#a-create-a-new-branch)
    *   [B. Make and Commit Changes](#b-make-and-commit-changes)
    *   [C. Push the Branch to GitHub](#c-push-the-branch-to-github)
4.  [Step 4: Create a Pull Request (A "Self-Review")](#4-step-4-create-a-pull-request-a-self-review)
5.  [Step 5: Review and Merge Your Own Pull Request](#5-step-5-review-and-merge-your-own-pull-request)
6.  [Step 6: Sync and Clean Up Your Workspace](#6-step-6-sync-and-clean-up-your-workspace)

---

### 1. Step 1: Create Your Project Repository on GitHub

Every project starts with a central "remote" repository on GitHub.com.

1.  Log in to [GitHub.com](https://github.com).
2.  In the top-right corner, click the **`+`** icon and select **"New repository"**.
3.  **Repository name:** Choose a name for your project (e.g., `my-portfolio-site`).
4.  **Description:** Add a brief, one-sentence description.
5.  **Public vs. Private:** Your choice. `Public` is great for portfolio projects.
6.  **Initialize this repository with:**
    *   **[✅] Add a README file:** **This is essential.** It creates the repository with an initial file, making it easy to clone.
    *   **[✅] Add .gitignore:** Select a template that matches your project's technology (e.g., `Node`, `HTML`, `Python`).
7.  Click the green **"Create repository"** button.

### 2. Step 2: Clone the Repository to Your Computer

Now, get a local copy of the project on your machine.

1.  On your new repository's page, click the green **"<> Code"** button.
2.  Select the **"Open with GitHub Desktop"** option.
3.  GitHub Desktop will launch. Choose a "Local Path" (a folder on your computer) to save the project.
4.  Click **"Clone"**.

You now have a local copy of your project, ready for work!

### 3. Step 3: The Development Cycle: Working on a New Feature

Let's pretend you want to add a new "About Me" page to your project.

**The Golden Rule:** Never commit directly to the `main` branch.

#### A. Create a New Branch

You'll make the new page on a dedicated branch.

1.  In GitHub Desktop, ensure the "Current Repository" is your new project. The "Current Branch" should say **`main`**.
2.  Click on the **"Current Branch"** dropdown and then click the blue **"New Branch"** button.
3.  Name your branch something descriptive, like `feature/add-about-page`.
4.  Click **"Create Branch"**. You will automatically be switched to this new branch.

#### B. Make and Commit Changes

Now, do the actual work.

1.  Open the project folder in your code editor.
