# Introduction to Git: Setup and Basic Commands

This guide provides step-by-step instructions on how to install and configure Git, initialize a new repository, and use basic Git commands such as `git add` and `git commit`.

## Prerequisites
Before proceeding, make sure you have:
- A terminal (command-line) interface.
- Git installed on your machine. If not, follow the [Git Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## Installation and Setup

1. **Install Git:**
   - For Windows: Download from [git-scm.com](https://git-scm.com/download/win).
   - For macOS: Use Homebrew by running `brew install git`.
   - For Linux: Use your package manager, e.g., `sudo apt-get install git`.

2. **Configure Git:**
   After installing Git, configure your Git user identity. Open a terminal and run the following commands:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "youremail@example.com"
   ```

   This step ensures that every Git commit you make uses the correct username and email.

3. **Initialize a Git Repository:**
   - Create a new folder for your project or navigate to your existing project directory.
   - Initialize Git in this folder:

   ```bash
   mkdir my-project
   cd my-project
   git init
   ```

   This command sets up a new Git repository in your project directory.

## Basic Git Commands

1. **Add Files to the Repository:**
   Use the `git add` command to stage files for commit.

   ```bash
   git add <filename>
   ```

   To add all the files in the directory:

   ```bash
   git add .
   ```

2. **Commit Changes:**
   Once files are added, commit them to your local repository with a message describing the changes.

   ```bash
   git commit -m "Initial commit"
   ```

   Each commit creates a snapshot of your project at that point in time.

## Additional Commands

1. **Check Status:**
   To check the status of your repository and see which files are staged, run:

   ```bash
   git status
   ```

2. **View Commit History:**
   To view the commit history of your repository, run:

   ```bash
   git log
   ```

---

### Happy coding! 🎉
```

This README file provides instructions to help users get started with Git, from installation to basic commands like `git add` and `git commit`, reflecting the key points from your document. You can modify it as per your specific needs!
