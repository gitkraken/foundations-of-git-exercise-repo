---

title: Git hooks example
description: Basic example on how to create a git hook.

---

Git hooks are scripts that perform automated actions when a specific action is performed in GitKraken Client or the command line. The git hook name usually indicates the hook's trigger _(e.g. pre-commit)_. 

Git hooks live under the `.git` folder of your repo in a directory called hooks. The path to the hooks will look similar to `repo/.git/hooks`.

***

### Tools needed
- GitKraken Client
- Text Editor - I will be using [Visual Studio Code](https://code.visualstudio.com/)
- Terminal - I will be using [iTerm2](https://www.iterm2.com/)

### Hook Purpose
In this example, we'll create a `pre-commit` hook. This hook validates the git config's global user email and checks whether a _gpg key_ exists. The hook is useful so that the commits contain the correct committer email address and also to ensure the commits are signed.

### Creating the git hook

#### Step 1
First navigate to the hooks directory for the target repo. Open a Visual Studio Code window and navigate to <em class="context-menu">repo&nbsp;&nbsp;&nbsp;<i class="fa fa-caret-right"></i>&nbsp; &nbsp;.git &nbsp;&nbsp;&nbsp;<i class="fa fa-caret-right">&nbsp;&nbsp;&nbsp;</i>hooks</em>. From here, add a new file to the `.git/hooks` directory called `pre-commit`.

<img src='/img/documentation/repositories/githooks-example/vscode-to-hooks.png' class='img-responsive center img-bordered' />

<div class='callout callout--warning'>
    <p>Note 📝 - To make the .git folder visible in Visual Studio Code you will need to remove **/.git from files.exclude in the Visual Studio Code settings.</p>
</div>

#### Step 2
Now that we have our pre-commit file, we need to make it executable. To do this we will need the command line. 

Open a terminal window by using `option + T` in GitKraken Client. Once the terminal windows is open, change directory to `.git/hooks`. 

Then use the command `chmod +x pre-commit` to make the pre-commit file executable.

<img src='/img/documentation/repositories/githooks-example/chmod-pre-commit-hook.gif' class='img-responsive center img-bordered' />

<div class='callout callout--warning'>
    <p>Note 📝 - If you do not have your terminal setup in GitKraken Client, please review the <a href="/start-here/tips/#9-open-terminal">Start Here Tips</a> for setup details.</p>
</div>

#### Step 3
Now we create our script using bash. In order for the script to run, we first need to specify our shell. Do this by using `#!/bin/bash` at the beginning of your script for bash or `#!/bin/sh` if using the sh shell. Any script that exits with anything other than exit code 0 is considered a fail. 

This `pre-commit` hook watches for incorrect commit authors and unsigned commits using the script below.

**Script variables:**<br>
`PWD` - Print working directory<br>
`globalEmail` - Get email in global git config<br>
`signingKey` - Get key in global git config<br>
`workEmail` - This is your target email address. The email needed to commit successfully.<br>

Now to explore the conditions we have set for our script. First we validate that the working directory contains *demo* and that the global git config user.email matches with our workEmail. If it fails we will see:

```
        echo "Commit email and global git config email differ"
        echo "Global commit email: "$globalEmail""
        echo "Committing email expected: $workEmail"
        exit 1

```

If the condition is met we move on to the next condition. If the global user.signingKey is empty we display:

```
        echo "No signing key found. Check global gitconfig"
        exit 1
```
If the condition is successful the script will run and the commit will be made. 

#### Full Script
```
#!/bin/bash

PWD=`pwd`
globalEmail=`git config --global --get user.email`
signingKey=`git config --global --get user.signingkey`
workEmail="example@axosoft.com"

if [[ $PWD != "*demo*" && $globalEmail != $workEmail ]];
then
        echo "Commit email and global git config email differ"
        echo "Global commit email: "$globalEmail""
        echo "Committing email expected: $workEmail"
        exit 1
elif [[ $signingKey -eq "" ]];
then
        echo "No signing key found. Check global gitconfig"
        exit 1
else
        echo ""
        exit 0
fi
```

### Git hook in action
<img src='/img/documentation/repositories/githooks-example/hook-in-action.gif' class='img-responsive center img-bordered' />