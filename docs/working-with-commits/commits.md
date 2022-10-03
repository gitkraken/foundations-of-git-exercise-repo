---

title: Committing Changes
description: Commit to save your work with GitKraken Client easily when changing files.  Learn how to squash, amend and save work when committing.

---

Commit to save work with GitKraken Client when changing files.  Whether you commit to other things in life is up to you...


***

<a id="making-a-commit"></a>

## Making a commit

To make a commit in GitKraken Client, select your _Work in Progress_ and to view recent changes on the Commit Panel.

<img src='/img/documentation/working-with-files/commits/WIP-stage.png' srcset='/img/documentation/working-with-files/commits/WIP-stage@2x.png 2x' class='img-bordered img-responsive center'>

Select the files you wish to stage, and click on any files you wish to review in the diff. To stage all your files, use the keyboard shortcut <kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>S</kbd> for Mac or <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>S</kbd> for Windows or Linux.

When you’re ready, type your message and hit commit to commit your changes. You can also use this **Commit** keyboard shortcut <kbd>&#8984;</kbd> + <kbd>Enter</kbd> for Mac or <kbd>Ctrl</kbd> + <kbd>Enter</kbd> if you are on Linux or Windows.

<img src='/img/documentation/working-with-files/commits/commit.png' srcset='/img/documentation/working-with-files/commits/commit@2x.png 2x' class='img-bordered img-responsive center'>

The graph updates with your commit, but the undo button or this keyboard shortcut
<kbd>&#8984;</kbd> + <kbd>Z</kbd> for Mac or <kbd>Ctrl</kbd> + <kbd>Z</kbd> for Windows/Linux can undo a commit made by mistake.

<a id="committing-with-co-authors"></a>

### Committing with Co-Authors

To add co-authors to a commit, add a line to your commit description using the following format: 
```
    Co-authored-by: INSERT NAME 1 <Email address 1>
    Co-authored-by: INSERT NAME 2 <Email address 2>
    ...and so on
    
```

<img src='/img/documentation/working-with-files/commits/co-author.png' srcset='/img/documentation/working-with-files/commits/co-author@2x.png 2x' class='img-bordered img-responsive center'>

The commit panel will then show the co-author in the history for that commit:

<img src='/img/documentation/working-with-files/commits/co-author-history.png' srcset='/img/documentation/working-with-files/commits/co-author-history@2x.png 2x' class='img-bordered img-responsive center'>

***

<a id="commit-templates"></a>

## Commit Templates

<a id="reading-the-commit-template"></a>

### Reading the Commit Template
When you open a repository, GitKraken Client will first check for a commit template set up in your repository's `.git/config`. If no commit template is found, it will then check your default (global) `.gitconfig`. If no commit template is found there either, then no commit template will be populated in GitKraken Client.

<a id="creating-and-updating-the-commit-template"></a>

### Creating and Updating the Commit Template
You can create and update a commit template in GitKraken Client by visiting <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i>Commit Template</em>.

If a commit template was read from your local git config, any changes you make to the template in GitKraken Client will save to the file specified.

If a commit template was not read from your default `.gitconfig` or you are creating a template for the first time, any change you make to the template in GitKraken Client will be written to a file called `gkcommittemplate.txt` in your repository's `.git/` directory. GitKraken Client will also update your repository's git config `commit.template` setting to point to this file. This allows you to make changes to your local commit template without overwriting your global commit template for all of your other repositories.

Checking the `Apply this template to commit messages` option will automatically apply the template to the commit message pane.  If this option is not checked, the commit message pane will be blank.

<img src='/img/documentation/working-with-files/commits/create-template.png' srcset='/img/documentation/working-with-files/commits/create-template@2x.png 2x' class='img-bordered img-responsive center'>

There are three different ways to set up commit templates in GitKraken Client:

* **Create the template in GitKraken Client** - This will create a file called `gkcommittemplate.txt` in your repository's `.git/` directory.

* **Add a repo-specific commit template** - Open a terminal in your local repository and run `git config commit.template <path_to_template>`

* **Add a global commit template** - Open a terminal window and run `git config --global commit.template <path_to_template>`
<div class='callout callout--basic'>
    <p>**Note:** Any changes made in GitKraken Client to a global commit template will cause GitKraken Client to create a `gkcommittemplate.txt` file in your local `.git/` directory and point your repository's git config `commit.template` setting to the `gkcommittemplate.txt` file</p>
</div>


***

<a id="amending-commits"></a>

## Amending commits

GitKraken Client allows you to amend a commit message, add additional changes, or both.

To add more changes, amend a commit by clicking on the _//WIP_ node on the graph.

<img src='/img/documentation/working-with-files/commits/WIP-node.png' srcset='/img/documentation/working-with-files/commits/WIP-node@2x.png 2x' class='img-bordered img-responsive center'>

If you only need to update the commit message, select the most recent commit and click in the message box to amend the message.

<img src='/img/documentation/working-with-files/commits/amend.png' srcset='/img/documentation/working-with-files/commits/amend@2x.png 2x' class='img-bordered img-responsive center'>

To accommodate viewing a longer commit description, click on the bar at the the bottom of the message box and drag downwards to dynamically resize the text field.

<img src='/img/documentation/working-with-files/commits/resize.gif' class='img-bordered img-responsive center'>


Select <button class='button button--success button--ui button--nolink'>Update Message</button> to save your changes or <button class='button button--danger button--ui button--nolink'>Cancel Amend</button> to discard.  

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Amending commits which are already pushed to a remote are more difficult to apply and would require a force push for the rewrite.</p>
</div>

***

<a id="resetting-commits"></a>

## Resetting commits
Git keeps track of your current commit in a file called the HEAD.  When resetting a commit, you update the HEAD of your repo to point to the selected commit.  GitKraken Client offers the following reset options:

* **Soft** - resets the HEAD to the selected commit, but keeps your changes staged and in your WIP directory
* **Mixed** - resets the HEAD to the selected commit, unstages your changes, but keeps them in your WIP directory
* **Hard** - resets the HEAD to the selected commit, unstages your changes, and deletes your WIP files

<img src='/img/documentation/working-with-files/commits/reset-commit.png' srcset='/img/documentation/working-with-files/commits/reset-commit@2x.png 2x' class='img-bordered img-responsive center'>

You may also drag and drop a branch onto another to select from the three reset options above or access the reset options from your local repos in the left panel.

***

<a id="reverting-changes"></a>

## Reverting changes
<img src='/img/documentation/working-with-files/commits/undo.png' srcset='/img/documentation/working-with-files/commits/undo@2x.png 2x' class='img-bordered img-responsive center'>

Undo, undo, undo. You can undo many of your actions in GitKraken Client with the Undo icon.

If you're a keyboard fan, you may also enjoy using the keyboard shortcut
<kbd>&#8984;</kbd> + <kbd>z</kbd> for Mac or <kbd>Ctrl</kbd> + <kbd>Z</kbd> for not-Mac.

<a id="reverting-commits"></a>

### Reverting commits

If you wish to revert a commit (perhaps Undo is not available), the option is available when right-clicking on a commit node. This will create a new commit to reverse your previous changes.

<img src='/img/documentation/working-with-files/commits/revert-commit.png' srcset='/img/documentation/working-with-files/commits/revert-commit@2x.png 2x' class='img-bordered img-responsive center'>
