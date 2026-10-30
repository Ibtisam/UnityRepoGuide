# Creating a Unity Repository on GitHub

This guide explains how to create a GitHub repository for a Unity game development project and upload the project files using Git Command Line Interface (CLI).

By following these steps, you will be able to initialize Git in your Unity project, configure the repository, connect it to GitHub, and push your project files to the remote repository.

---

## 1. Installation & Setup

Before creating a repository, make sure that Git is installed on your computer and that you have a GitHub account.

### Step 1: Install Git
Download and install Git for Windows from the official website:

https://git-scm.com/install/windows

### Step 2: Create a GitHub Account
If you do not already have an account, create one on GitHub:

https://github.com

---

## 2. Using the Command Line (CLI)

Once Git is installed and your GitHub account is ready, follow the steps below to upload your Unity project.

### Step 1: Open Command Prompt or PowerShell

1. Open **Command Prompt (cmd)** or **PowerShell**.
2. Navigate to your Unity project's root directory using the following command:

```bash
cd <YOUR_PROJ_ROOT>
```

**Important:** Run all the following commands inside your project's root directory (the folder that contains your `Assets` and `ProjectSettings` folders).

### Step 2: Initialize Git

Initialize a new Git repository in your Unity project directory and set the branch name to `main`.

Run the following commands:

```bash
git init
git branch -M main
```

### Step 3: Add the Unity .gitignore

A `.gitignore` file tells Git which files and folders should be excluded from version control.

For Unity projects, this is important because Unity generates temporary and cache files that should generally not be uploaded to GitHub.

Follow these instructions:

1. Manually create a file named `.gitignore` in your Unity project's root directory.
2. Open GitHub's official Unity `.gitignore` template.
3. Copy its contents and paste them into your newly created `.gitignore` file.

**Official Unity .gitignore Template:**

https://github.com/github/gitignore/blob/main/Unity.gitignore

### Step 4: Create the GitHub Remote

Now, create a remote repository on GitHub and connect it to your local Unity project.

1. Go to https://github.com.
2. Create a **blank repository**.
3. Do not initialize it with a README or `.gitignore` this time.
4. Copy the repository URL.
5. Link the GitHub repository to your local machine by running:

```bash
git remote add origin <PASTE_YOUR_GITHUB_REPO_URL_HERE>
```

**Note:** Replace `<PASTE_YOUR_GITHUB_REPO_URL_HERE>` with the URL of your newly created GitHub repository.

### Step 5: Stage, Commit and Push

Finally, upload your Unity project to GitHub.

Execute the following commands in the same sequence:

**1. Stage all project files:**

```bash
git add .
```

**2. Commit the staged files:**

```bash
git commit -m "Initial Unity commit for the game title"
```

**3. Push the project to GitHub:**

```bash
git push -u origin main
```

---

## 3. Verify Your Repository

After successfully executing the push command:

1. Open your GitHub account.
2. Navigate to the repository you created.
3. Refresh the repository page.
4. Verify that your Unity project files and folders are visible.

Your Unity project should now be available on GitHub.

---

## 4. Important Reminders

- Always execute Git commands from the Unity project's root directory.
- Make sure the `.gitignore` file is created before staging your project files.
- Do not upload unnecessary Unity-generated cache and temporary files.
- Make sure your repository URL is correct before adding the remote.
- Keep your repository updated by committing and pushing your changes regularly.

---

**End of Guide**

*Prepared for Game Development Course – Unity Project Version Control.*
