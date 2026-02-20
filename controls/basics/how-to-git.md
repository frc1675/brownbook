## What is git and what is it used for? 

<img id="git-logo" src="../../assets/images/git-logo.png" alt="git-logo" style="width: 150px; float: right; padding: 25px" />

Git is a version control system which is capable of cataloging all changes you make to tracked files. Git centers around the manipulation of branches of code, to work separately on and eventually merge different sets of code to collaborate on a final product. When you create or edit a file on your computer, the changes you make locally can be recorded and can differ from that of the "global" code repository otherwise known as `origin` (for us, this one is hosted under the frc1675 organization). We use git with a specific set of commands and GitHub interactions to enforce a process that provides a higher level of quality assurance via review and testing before new code joins the rest.

### How to use git

`git` is pretty complicated and can do any number of things, but here's how you will and should primarily use it on the team:

#### First time using the repository

* `git clone <repository url>`
  * You get get the repository URL from the GitHub repository page. This creates a copy of the repository for you to work in.

#### When starting a new task

* `git fetch --all`
  * Updates the status of all remotes on your machine to their current statuses. `origin` is the remote that you clone from (GitHub). You want to know the current state of origin before doing the following steps.

* `git checkout orign/main`
  * Sets your current state to be identical to the latest state of `main`. You will see complaining about being in a "detached head" state, but that's ok.

* `git checkout -b <new-branch-name>`
  * Makes a new branch for you to work in, that will be based on the current state of `main`. Commits you make later will be associated to this branch.

#### Saving your changes to the repository

* `git add .`
  * After making and saving changes, `git add` command "stages" changes to be recorded by git. The above command adds all changes in all files in your repository folder.

* `git commit -m <message>`
  * `git commit` saves the current set of changes into the repository. Each commit should be given a brief and descriptive message.

#### Getting new changes from `main`

* `git fetch --all`
  * Updates the status of all remotes on your machine to their current statuses. `origin` is the remote that you clone from (GitHub). You want to know the current state of origin before doing the following steps.

* `git merge origin/main`
  * Automatically merges any new changes from `origin`'s `main` into your branch. You can accept the default merge commit message (ask a mentor if you can't figure out how to accept it). If your changes conflict with the new changes, ask a mentor to help with resolving them.

#### Sharing your changes on GitHub

* `git push origin <new-branch-name>`
  * Adds your branch to the repository on GitHub. Create a pull request to ask for your changes to be pulled into `main` after this is complete.

### Install git

Install git on your development computer. You can get it from https://git-scm.com/ . Team laptops will have git already installed and configured the way we want.

When installing select these options:

* Use Git from Git Bash only
* Use the OpenSSL library
* Checkout Windows-style, commit Unix-style line endings
* Use MinTTY

Those are the important ones to make sure, default on every other screen should be fine.

 Having a GitHub account is required for contributing to 1675's codebase. To continue and find information on contributing code visit: [How to Contribute](./how-to-contribute.md).
