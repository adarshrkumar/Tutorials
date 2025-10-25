# A Beginner's Guide to Git Collaboration with GitHub Desktop

**Course Length:** 20-25 minutes
**Audience:** Absolute beginners who have not yet installed Git or created a GitHub account.
**Goal:** To install all necessary tools and master the standard team collaboration workflow using a personal repository as a safe practice environment.

---

## Introduction

Welcome to version control! This guide will teach you the standard workflow used by development teams worldwide to collaborate on code. We will use three key tools:

*   **Git:** The underlying version control system that tracks changes to your files.
*   **GitHub:** A website that hosts your projects and allows for collaboration (like code reviews). It's the "remote" location for your code.
*   **GitHub Desktop:** A user-friendly application that provides a graphical interface for Git, making it easier to see changes and perform commands without using the command line.

By the end of this tutorial, you will have installed everything you need and practiced the complete cycle of making a change to a project.

## Table of Contents

*   [Part 1: Setup and Installation](#part-1-setup-and-installation)
    *   [Step 1: Install Git](#step-1-install-git)
    *   [Step 2: Create a GitHub Account](#step-2-create-a-github-account)
    *   [Step 3: Install and Configure GitHub Desktop](#step-3-install-and-configure-github-desktop)
*   [Part 2: The Collaborative Workflow Practice](#part-2-the-collaborative-workflow-practice)
    *   [Step 1: Create Your Practice Repository](#step-1-create-your-practice-repository)
    *   [Step 2: Clone the Repository to Your Computer](#step-2-clone-the-repository-to-your-computer)
    *   [Step 3: The Development Cycle](#step-3-the-development-cycle)
    *   [Step 4: Create a Pull Request](#step-4-create-a-pull-request)
    *   [Step 5: Review and Merge the Pull Request](#step-5-review-and-merge-the-pull-request)
    *   [Step 6: Sync and Clean Up Your Workspace](#step-6-sync-and-clean-up-your-workspace)

---

## Part 1: Setup and Installation

Before we can practice the workflow, we need to set up our tools.

### Step 1: Install Git

Even though we'll be using a graphical application, GitHub Desktop is a visual tool *for* Git. The underlying Git software must be installed on your computer first.

1.  Go to the official Git download page: [https://git-scm.com/downloads](https://git-scm.com/downloads)
2.  Download the installer for your operating system (Windows, Mac, or Linux).
3.  Run the installer. For most users, **the default settings are all you need**. You can click "Next" through all the installation steps.

### Step 2: Create a GitHub Account

GitHub is where your projects will be stored and shared.

1.  Go to [https://github.com](https://github.com).
2.  Click **"Sign up"** and follow the instructions to create your free account. Choose a username you like—it will be part of your public profile.

### Step 3: Install and Configure GitHub Desktop

This is the main application we will use for our workflow.

1.  Go to the GitHub Desktop official website: [https://desktop.github.com](https://desktop.github.com)
2.  Download and run the installer for your operating system.
3.  Once the installation is complete, launch GitHub Desktop.
4.  The application will prompt you to **"Sign in to GitHub.com"**. Click this and follow the steps to authorize the application with the GitHub account you created in Step 2.

**Setup is complete!** You are now ready to learn the collaborative workflow.

---

## Part 2: The Collaborative Workflow Practice

### Step 1: Create Your Practice Repository

Every project lives in a "repository" on GitHub. Let's create one to practice in.

1.  Go to your GitHub.com dashboard.
2.  In the top-right corner, click the **`+`** icon and select **"New repository"**.
3.  **Repository name:** `team-workflow-practice`
4.  **Description:** "A repository for practicing the GitHub collaborative workflow."
5.  **Initialize this repository with:**
    *   **[✅] Add a README file:** **This is essential.** It gives us our first file to work with.
    *   **[✅] Add .gitignore:** Select a template from the dropdown, like `HTML`.
6.  Click the green **"Create repository"** button.

### Step 2: Clone the Repository to Your Computer

"Cloning" means making a local copy of a remote repository.

1.  On your new repository's page on GitHub.com, click the green **"<> Code"** button.
2.  Select the **"Open with GitHub Desktop"** option.
3.  Your browser will ask for permission to open GitHub Desktop. Allow it.
4.  GitHub Desktop will launch and ask where on your computer you want to save the project (the "Local Path"). Choose a location you'll remember.
5.  Click **"Clone"**.

### Step 3: The Development Cycle

Imagine you've been assigned a task: add a "Project Goals" section to the README file.

**The Golden Rule:** Never commit directly to the `main` branch. This branch is reserved for stable, approved code.

#### A. Create a New Branch

You will do your work on a separate "feature branch."

1.  In GitHub Desktop, ensure the "Current Branch" at the top says **`main`**.
2.  Click the **"Current Branch"** dropdown and then click **"New Branch"**.
3.  Name your branch based on the task, like `docs/add-project-goals`. Click **"Create Branch"**.

#### B. Make and Commit Changes

1.  Open the project folder in your favorite code editor. Edit the `README.md` file by adding a new "Project Goals" heading and a sentence or two. Save the file.
2.  Return to GitHub Desktop. Your modified `README.md` file will appear in the **"Changes"** tab.
3.  In the **"Summary"** field at the bottom-left, type a commit message: "Docs: Add project goals section".
4.  Click the blue **"Commit to `docs/add-project-goals`"** button.

#### C. Push the Branch to GitHub

Your commit and branch are currently only on your machine. "Pushing" sends them up to GitHub.

1.  Click the blue **"Publish branch"** button in the center of the application.

### Step 4: Create a Pull Request

A Pull Request (PR) is a formal request to merge your changes into the `main` branch. It's how you present your work to the team for review.

1.  After publishing, click the **"Create Pull Request"** button in GitHub Desktop.
2.  Your browser will open the "Open a pull request" page on GitHub.
3.  Review the title and description, then click **"Create pull request"**.

### Step 5: Review and Merge the Pull Request

Now, you will act as the project maintainer who approves changes.

1.  On the Pull Request page on GitHub.com, you can review the proposed changes under the **"Files changed"** tab.
2.  Since the changes look good, go back to the **"Conversation"** tab.
3.  Click the green **"Merge pull request"** button, and then **"Confirm merge"**.

Your work is now officially part of the project's `main` branch!

### Step 6: Sync and Clean Up Your Workspace

The final step is to update your local copy of the project.

1.  Go back to GitHub Desktop.
2.  Use the **"Current Branch"** dropdown to switch back to the **`main`** branch.
3.  Click the **"Pull origin"** button at the top to download the changes you just merged. Your local `main` branch is now up-to-date.
4.  To keep your workspace tidy, delete the old branch. In the menu bar, go to **Branch > Delete...** and choose `docs/add-project-goals`.

**Congratulations!** You have successfully completed the entire collaborative workflow. You are now equipped with the fundamental skills needed to contribute to projects with a team.
