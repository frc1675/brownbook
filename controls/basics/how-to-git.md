## What is git and what is it used for? 

<img id="git-logo" src="../../assets/images/git-logo.png" alt="git-logo" style="width: 150px; float: right; padding: 25px" />

Git is a version control system which is capable of cataloging all changes you make to tracked files. Git centers around the manipulation of branches of code, to work separately on and eventually merge different sets of code to collaborate on a final product. When you create or edit a file on your computer, the changes you make locally can be recorded and can differ from that of the "global" code repository otherwise known as `origin` (for us, this one is hosted under the frc1675 organization). We use git with a specific set of commands and GitHub interactions to (mostly) enforce a process that provides a higher level of quality assurance via review and testing before new code joins the rest. How all of these benefits are achieved is through proper utilization.


### How to use git

Commonly Used Commands:

* `git add %filename%`

    The `git add` command adds a filename to the tracker and its changes will be recorded by git. Only files added through the `git add` command will be included in commits and pushes later down the line.
* `git commit -m %user message%`

    The git commit command will record all changes that you make locally on your device. Said commit will be provided a unique code which can be referenced in other commands ie: revert, push, diff. All commits must contain a message, when writing the description try to be as descriptive as possible while also not overwhelming the reviewer.
* `git push origin %branchname%`

    How we stage changes in most content tracked codebases is through the introduction of new branches containing our code. The git push command takes our locally committed changes and "pushes" them to the external server connected to the repository.


![git development cycle](../../assets/images/git-cycle.png)


For more info on commands and git, type: [`man git`]("https://git-scm.com/docs") into your command line. Or watch this [video]("https://www.youtube.com/watch?v=HkdAHXoRtos").

### Create a GitHub account

GitHub is one such online git service provider. To create a new GitHub account follow the instructions below or watch [video](https://www.youtube.com/watch?v=HkdAHXoRtos)!

    1. Visit GitHub and Click Sign Up!
    2. Enter Email: Professional/Personal
    3. Create a Password: Memorable!
    4. Select a Username: Professional Recommended
    5. Verify Email and Enjoy!

### Install git

Install git on your development computer. You can get it from https://git-scm.com/ . Team laptops will have git already installed and configured the way we want.

When installing select these options:

* Use Git from Git Bash only
* Use the OpenSSL library
* Checkout Windows-style, commit Unix-style line endings
* Use MinTTY

Those are the important ones to make sure, default on every other screen should be fine.

 Having a GitHub account is required for contributing to 1675's codebase. It may seem overwhelming at first, but keep at it and in no time you'll soon be a master! To continue and find information on contributing code visit: [How to Contribute](./how-to-contribute.md).
