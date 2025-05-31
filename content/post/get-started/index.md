---
title: Controlling the versions of Git
summary: Take full control of your personal brand and privacy by migrating away from the big tech platforms!
date: 2025-03-21

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com)'

authors:
  - admin

tags:
  - Academic
  - Hugo Blox
  - Markdown
---

## Basics
Git is a set of console utilities that track and commit changes to files (most often source code, but you can use it for any files). Git was originally created by Linus Torvalds while developing the Linux kernel. However, developers found it so useful that it became widely adopted for many other projects. With Git, you can compare, analyze, edit, merge changes, and revert to the last save point. This process is known as version control.

Why do we need it? First, to track changes made to a project over time.

Second, it’s extremely helpful when multiple developers are working on the same project simultaneously. Without Git, chaos would ensue when developers try to copy code back into the main folder after making their changes.

Git is distributed, meaning it doesn’t depend on a central server to store files. Instead, it works completely locally, saving data in directories on your hard drive called repositories. However, you can store a copy of the repository online, which greatly simplifies collaboration. This is where services like GitHub and Bitbucket come in.

## Installation

Installing Git on your machine is simple:

- **Linux** — Just open a terminal and install the app using your distribution's package manager. For Ubuntu, use:
sudo apt-get install git

markdown
Copy
Edit
- **Windows** — We recommend Git for Windows, as it includes both a GUI client and a Bash emulator.
- **OS X** — The easiest way is to use Homebrew. After installing it, run in the terminal:
brew install git

sql
Copy
Edit

## Configuration

Now that Git is installed, we need to configure it a bit. There are many options you can tweak, but we’ll start with the most important: your username and email address. Open a terminal and run:

git config --global user.name "My Name"
git config --global user.email myEmail@example.com

css
Copy
Edit

Now every action will be tagged with your name and email. This adds clarity and accountability.

Git stores all settings in a `.gitconfig` file in your home directory. To make these settings global (i.e., apply to all projects), add the `--global` flag. Without it, they only apply to the current repository.

To view all settings, use:

git config --list

css
Copy
Edit

To make output more visually readable, you can enable color:

git config --global color.ui true
git config --global color.status auto
git config --global color.branch auto

vbnet
Copy
Edit

If you're not fully configured yet, no worries — Git will guide you. For example:

- `git --help` — Shows general Git documentation
- `git log --help` — Shows documentation for a specific command (in this case, `log`)
- Mistyped a command? Git will suggest the correct one.
- Git provides feedback after executing any command.

## Creating a New Repository

As mentioned earlier, Git stores its files and history directly in the project folder. To create a new repository, open a terminal, navigate to your project folder, and run:

mkdir Desktop/git_exercise/
cd Desktop/git_exercise/
git init

vbnet
Copy
Edit

This activates Git in that folder and creates a hidden `.git` directory to store history and settings.

## Checking Status

The `status` command is crucial. It shows the current state of the repository: whether it's up to date, if anything new was added, etc. Running `git status` on our fresh repo should display:

$ git status
On branch master
Initial commit
Untracked files:
(use "git add ..." to include in what will be committed)
hello.txt

sql
Copy
Edit

## Staging Files

Git uses a staging area, a kind of canvas where you place changes you want to commit. It starts empty, then you add files (or parts of files) to it using `add`, and finally commit everything with `commit`.

For example, to add a single file:

git add hello.txt

csharp
Copy
Edit

To add everything in the directory:

git add -A

lua
Copy
Edit

Check the status again:

git status
On branch master
Initial commit
Changes to be committed:
(use "git rm --cached ..." to unstage)
new file: hello.txt

csharp
Copy
Edit

The file is now staged for commit. The message indicates what kind of change occurred — in this case, a new file.

## Committing Changes

### How to Commit

Imagine you add a few new blocks to `index.html` and style them in `style.css`. To save these changes, first stage them:

git add index.html
git add css/style.css

yaml
Copy
Edit

Or, stage everything:

git add .

sql
Copy
Edit

Then create the commit:

git commit -m 'Add some code'

sql
Copy
Edit

The `-m` flag sets the commit message. Follow the golden rule of comments: “Be clear, simple, and informative.”

### Viewing Commits

To view the commit history:

git log

sql
Copy
Edit

It shows each commit’s hash, author, date, and message.

To see details of a specific commit:

git show hash_commit

sql
Copy
Edit

To amend the last commit’s message:

git commit --amend -m 'New message'

css
Copy
Edit

Be careful — this rewrites history and is best done before pushing to a remote.

## Remote Repositories

Our commit is still local — it only exists in the `.git` folder on our machine. While local repos are useful, we often want to share our code or deploy it.

### What Is a Remote Repository?

A remote repo is stored in the cloud on a Git hosting service. It serves as a backup and allows team collaboration. Services often include visual history tools or in-browser editors.

### Cloning

Cloning copies a remote repo to your local machine, including all files and history. For example:

git clone https://github.com/tutorialzine/awesome-project

vbnet
Copy
Edit

By default, it creates a folder with the repo’s name. To clone into a different folder:

git clone https://github.com/tutorialzine/awesome-project new-folder

css
Copy
Edit

### Connecting to a Remote Repo

To push local commits to a remote repo, you must first connect to it. For example:

git remote add origin https://github.com/tutorialzine/awesome-project.git

vbnet
Copy
Edit

You can have multiple remotes with different names. The default is usually `origin`.

### Pushing Changes

To send your commits to the remote repo:

git push origin master

lua
Copy
Edit

Example output:
Counting objects: 3, done.
Writing objects: 100% (3/3), 212 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/tutorialzine/awesome-project.git

[new branch] master -> master

vbnet
Copy
Edit

Unlike `git fetch` (which downloads commits), `git push` uploads them. Use `git remote` to manage remote branches.

Pushing can overwrite changes — use it carefully. It’s often used to share changes with collaborators.

Once you push successfully, you'll see the files (like `hello.txt`) in the remote repo via your browser.

### Pulling Changes

If remote changes were made, use `pull` to fetch and merge them:

git pull origin master

lua
Copy
Edit

Example output:
From https://github.com/tutorialzine/awesome-project

branch master -> FETCH_HEAD
Already up-to-date.

pgsql
Copy
Edit

No new commits — so nothing to download.

## Source

[Proglib](https://proglib.io/p/git-for-half-an-hour)

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/HugoBlox/hugo-blox-builder/blob/main/LICENSE.md) license.
