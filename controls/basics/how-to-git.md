## What is git and what is it used for? 

<img src="../../assets/images/git-logo.png" alt="git logo" style="width:150px; float: right; padding: 25px;">
Git is something called a content tracker which is capable of cataloging all changes you make to tracked files. Git centers around the manipulation of branches of code, the merging and converging of existing code branches to improve a ending product. When you create or edit a file on your computer, the changes you make locally will be recorded and can differ from that of the global codebase otherwise known as the main branch. This dissonance provides greater quality control to the maintainer (permitting these changes), and allows for a more adaptable development cycle for the programmer through quality of life commands such as: "git revert", "git diff", and "git merge" How all of these benefits are achieved is through proper utilization.

### How to use git

Commonly Used Commands:
<ul>
    <li>git add %filename%</li>
    The git add command adds a filename to the tracker and its changes will be recorded by git. Only files added through the git add command will be included in commits and pushes later down the line.
    <li>git commit -m %user message%</li>
    The git commit command will record all changes that you make locally on your device. Said commit will be provided a unique code which can be referenced in other commands ie: revert, push, diff. All commits must contain a message, when writing the description try to be as descriptive as possible while also not overwhelming the reviewer.
    <li>git push origin %branchname%</li>
    How we stage changes in most content tracked codebases is through the introduction of new branches containing our code. The git push command takes our locally committed changes and "pushes" them to the external server connected to the repository.
</ul>

<img src="../../assets/images/git-cycle.png" alt="git development cycle">

For more info on commands and git, type: <a href="https://git-scm.com/docs">"man git"</a> into your command line. Or watch this <a href="https://www.youtube.com/watch?v=HkdAHXoRtos" >video</a>.

### Create a github account

Github is one such online git service provider. To create a new github account follow the instructions below or watch <a href="https://www.youtube.com/watch?v=HkdAHXoRtos">this video</a>!

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

### Having a GitHub account is paramount to contributing to 1675's codebase, it may seem overwelming at first, but keep at it and in no time you'll soon be a master! To Continue and Find Information on Contributions visit: <a href="./how-to-contribute.md">How-To-Contribute</a>.

