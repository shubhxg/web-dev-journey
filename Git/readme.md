 # ![icons8-github-64](https://github.com/shubhsharma19/web-development-notes/assets/69891912/c582b458-d102-4373-8b3e-426f6bff613d) Git and GitHub Notes


- Git is a **Version control system (VCS)**, VCS is a tool that helps you track changes of your files over time.
- There are many different VCSs available, but some of the most popular include **Git, Mercurial, and Subversion**.
- Once you've chosen a VCS, you can start using it to track your changes. To do this, you'll first need to create a repository. A repository is a central location where all of your files are stored. You can then add files to your repository and make changes to them.
- VCS is very powerful tool as it helps you keep track of your work, creates a backup of the files and helps in collaboration.

## History of Git and GitHub
- **Linus Torwalds** created Git.
- Prior to Git, the Linux kernel development team used a proprietary version control system called **BitKeeper**. However, a dispute arose between the BitKeeper creators and the Linux community, leading to the need for a new solution and creation of Git.
- The first public release of Git was in **April 2005**. It was made available for download and quickly gained attention within the open-source community due to its performance and flexibility.


![Screenshot from 2023-03-18 23-17-00](https://github.com/shubhsharma19/web-development-notes/assets/69891912/59b9a615-5caa-4d24-b0db-78705342ab96)

> 🎈 Funfact: GitHub has 100+ million users in 2023 and gains over 500+ users everyday.

## Why use Git? 

- Fast
- Keeps track of changes
- Easy to use
- Non-linear
- Distributed
- Large

## What is a Commit? ☄

- In Git, a commit is a **snapshot** of the changes made to a repository at a particular point in time.
- It represents a set of changes made to the codebase, such as adding or modifying files, or making changes to existing files.
- Each commit has a **unique identifier**, called a hash, that allows you to refer to it and track the changes made to the code over time.
- When you create a commit, you also add a **commit message** that describes the changes you've made.

---

**A meme**

![bbeuhgg47kh51](https://github.com/shubhsharma19/web-development-notes/assets/69891912/5d96fb6b-881e-4c52-8711-dc0740020a6f)

> This meme is famous because developers need to commit and push their changes in this situation so that the history of the code remains on the central repo (GitHub)


## What is a Branch? 🌿

![2023-05-11 12_58_39-GitHub for Noobs (2_4) – Common Workflows - YouTube - Brave](https://github.com/shubhsharma19/web-development-notes/assets/69891912/706f95dc-7d38-4f87-9f03-7f790e4c32d4)

- Git branches are like those smaller branches on a tree.
- They're separate paths of development that come from the `main` branch.
- Each branch can have its own set of changes and updates.
- The changes that you made on a branch will not affect the `main` branch.

## What is a Pull Request? ⛓

![2023-05-11 13_02_02-GitHub for Noobs (2_4) – Common Workflows - YouTube - Brave](https://github.com/shubhsharma19/web-development-notes/assets/69891912/05db3fe2-d27c-4e09-b164-9565737a6dce)

- If someone else wants to make a change in your code they can do that and can ask you if you want to pull these changes into your code.
- To do that, they can create a separate branch or a fork of the code.
- These changes then can be merged into the main branch using a **PR or a pull request.**
- A pull request is a report of all the changes made.
- Once that branch is merged into main, you can also delete that branch.

## What is a fork?

- A Fork is a way to create a copy of a repository (a project) that belongs to someone else. 
- When you fork a repository, you're essentially making a duplicate of the project and creating your own version of it.
- Changes made in your forked repository won't affect the original project or anyone else's fork of it.

![2023-05-11 13_18_13-Excalidraw - Brave](https://github.com/shubhsharma19/web-development-notes/assets/69891912/038dcc12-87ee-4a48-922f-edc56241c4a4)

## Why do we need GitHub if Git is the game changer?

- GitHub is used as a centralised place to distribute code from 
- You can have your repo on github, you pull the code from repo into your local machine, you make some changes and you commit and then you push those changes from your local machine to the repo on the GitHub.

## Let's start with some basic git commands ![icons8-git-48](https://github.com/shubhsharma19/web-development-notes/assets/69891912/a5acf77b-efcc-41c0-a947-bf4bc8e67c78)

- Intializing git repo: 
> `git init` 
- To see the changes that are not saved (unsaved or uncommited changes) [files are red]
> `git status`
- To place the changes on the stage [this will turn the files green]
> `git add file` or `git add .`
- To commit  the changes 
> `git commit -m “message goes here”`
- To check the history of the changes
> `git log`
- To unstage the files
> `git restore —staged file`
- To put the changes on the stash (backstage lol)
> `git stash`
 
> Note: Remember that in order to put them in the backstage you first have to put these changes on the stage, you cant stash it if you have not staged it first.

Example: 

![2023-05-22 20_43_56-Welcome - Javascript from Jonas - Visual Studio Code](https://github.com/shubhsharma19/web-development-notes/assets/69891912/070f2aa6-b9ed-4ae9-a6d1-dce4c149ba49)

- To put stashed changes back to the staging area
> `git stash pop`

Example: 

![2023-05-22 20_46_18-Welcome - Javascript from Jonas - Visual Studio Code](https://github.com/shubhsharma19/web-development-notes/assets/69891912/2f3905e4-3f57-46e2-84b3-0e7984d3213b)

- To delete the stashed changes (all the stashed changes will be gone)
> `git stash clear`
