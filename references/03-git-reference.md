# **Git Reference**

This cheatsheet covers the essential Git commands for beginners using **Visual Studio Code**.

---

## **Initial Setup:**

Before starting, you need to configure Git with your name, email, and other settings. This ensures your commits are associated with your identity.

- **Set your username**:

  ```bash
  git config --global user.name "Your Name"
  ```

- **Set your email**:

  ```bash
  git config --global user.email "your.email@example.com"
  ```

- **Set automatic push behavior** (so you don’t need to specify a remote every time):

  ```bash
  git config --global --add --bool push.autoSetupRemote true
  ```

---

## **Cloning a Repository**

Cloning is the process of downloading an existing GitHub repository to your local machine.

- **Command**:

  ```bash
  git clone <repository-url>
  ```

  - Example: `git clone https://github.com/username/repo.git`

After cloning, open the project in **VSCode**.

---

## **Staging Changes (git add)**

After making changes to files, you need to stage them before committing.

- **Command**:

  ```bash
  git add <file>
  ```

  - To add all modified files:

    ```bash
    git add .
    ```

---

## **Committing Changes (git commit)**

Once files are staged, you can commit them. A commit is a snapshot of your project at a specific point.

- **Command**:

  ```bash
  git commit -m "Your commit message"
  ```

- **Best Practice**: Write clear and descriptive commit messages so others (and future you) can understand the changes easily.

---

## **Pushing Changes to GitHub (git push)**

After committing, you need to push your changes to GitHub.

- **Command**:

  ```bash
  git push origin <branch-name>
  ```

  - Example for the default branch:

    ```bash
    git push origin main
    ```

If you’re pushing for the first time or authenticating to GitHub, VSCode may prompt you to log in or authenticate with GitHub.

---

## **Pulling Changes from GitHub (git pull)**

To sync your local repository with changes others made on GitHub, use the `git pull` command.

- **Command**:

  ```bash
  git pull
  ```

This downloads the latest changes from the remote repository and merges them with your local code.

---

## **Authentication Tips**

If GitHub asks for authentication when pushing or pulling:

1. **Set your username and email** (as shown in the setup section above).
2. You may need to authenticate using **GitHub Personal Access Tokens** (if GitHub stopped accepting passwords):
   - When prompted, use the token in place of your password.

---

### **Common Issues**

- **Permission Denied (publickey)**: Ensure your SSH keys are set up or use HTTPS.
- **Authentication Error**: Generate a **GitHub Personal Access Token** and use that instead of a password.

---

This cheat sheet covers the most common Git commands you’ll need as a beginner. As you gain experience, you can explore more advanced commands and workflows!
