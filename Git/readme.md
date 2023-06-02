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
```
git init
``` 
- To see the changes that are not saved (unsaved or uncommited changes) [files are red]
```
git status
```
- To place the changes on the stage [this will turn the files green]
- To place `single file` in staging area
```
git add file 
```
- To place `All the files` in staging area
```
git add .
```
- To commit  the changes 
```
git commit -m “message goes here”
```
- To check the history of the changes
```
git log
```
- To unstage the files
```
git restore —staged file
```
- To put the changes on the stash (backstage lol)
```
git stash
```
 
> Note: Remember that in order to put them in the backstage you first have to put these changes on the stage, you cant stash it if you have not staged it first.

Example: 

![2023-05-22 20_43_56-Welcome - Javascript from Jonas - Visual Studio Code](https://github.com/shubhsharma19/web-development-notes/assets/69891912/070f2aa6-b9ed-4ae9-a6d1-dce4c149ba49)

- To put stashed changes back to the staging area
```
git stash pop
```

Example: 

![2023-05-22 20_46_18-Welcome - Javascript from Jonas - Visual Studio Code](https://github.com/shubhsharma19/web-development-notes/assets/69891912/2f3905e4-3f57-46e2-84b3-0e7984d3213b)

- To delete the stashed changes (all the stashed changes will be gone)
```
git stash clear
```

## Something about Origin and Upstream 
### Origin 
- **"Origin"** is the default name often given to the remote repository that you cloned from. When you clone a repository, Git sets up a remote named "origin" by default, which points to the repository you cloned from. It allows you to push your changes to and pull updates from that remote repository easily.
> For example, if you cloned a repository from GitHub, the "origin" remote would typically point to your fork of the repository on your GitHub account.

Example: My LinkFree Fork

![2023-05-23 13_38_45-shubhsharma19_LinkFree_ Connect to your audience with a single link  Showcase th](https://github.com/shubhsharma19/web-development-notes/assets/69891912/02726eaa-5386-4ea9-b21e-e09fa9d5da77)


### Upstream
- **"Upstream"** typically refers to the original repository from which your cloned repository was forked. It represents the authoritative source of the codebase. In the context of forking workflows, the "upstream" repository is where you fetch updates from and submit pull requests to if you want to contribute changes back to the original project.
For example, if you forked a repository on GitHub, the "upstream" remote would typically point to the original repository that you forked from. This allows you to keep your forked repository in sync with the latest changes from the upstream repository.

Example: LinkFree Original Repo

![2023-05-23 13_37_46-EddieHubCommunity_LinkFree_ Connect to your audience with a single link  Showcas](https://github.com/shubhsharma19/web-development-notes/assets/69891912/184a524c-022e-4de5-8e0a-e2b563760d8e)


- To connect your github repo to your local machine and make it remote. Origin means your own repos or forked repos.
```
git remote add origin "url goes here"
```
- To check your remote repos
```
git remote -v
``` 
- To clone a repo 
```
git clone "url goes here"
```
- To push the changes from your local git repository to the remote repository in the branch "main"
```
git push origin main
```
- To check branches
```
git branch
```
- To change the name of the branch 
```
git branch -m oldname newname
```
- To change remote url 
```
git remote set-url origin
``` 

**Pro Tip: Always create a separate branch for each new change that you want to create. This way codebase will stay clean and it will be easy for maintainers to maintain the project branches.**

- To create a branch 
```
git branch branch-name
```
- To checkout the branch  
```
git checkout branch-name
```

> Note: `git checkout branch-name` command will put the pointer on the specified branch,  head will now point to `branch-name` instead of `main`
