---

title: Interactive Rebase
description: Learn about interactive rebase in GitKraken Client.

---

Learn how to rewrite your commit history with interactive rebase in GitKraken Client.

***

## Initiating Interactive Rebase
To initiate interactive rebase, drag and drop one branch onto another branch or right-click the target branch and select <em class='context-menu'>Interactive Rebase</em>.

<img src='/img/documentation/repositories/interactive-rebase/interactive-rebase-init.gif' class='img-bordered img-responsive center' />

Right-click on any parent commit to see the interactive rebase option. However, please note that interactive rebase is not available for merge commits. 

### Interactive rebase limits

The drag and drop option will only show the interactive rebase option if:

- No merge commits are present on the branch you’re rebasing
- The 2 branches share a common ancestor
- Neither branch has the repo’s initial commit
- You are not attempting to rebase a parent branch onto a child (like master into a feature branch)

<div class='callout callout--note'>
    <p><strong>Note:</strong> If you start the interactive rebase with GitKraken Client you must finish the rebase with GitKraken Client.</p>
</div>

---

## Commit Actions

### Pick
Pick takes the commits from one branch and places them onto the last commit of another branch.

<img src='/img/documentation/repositories/interactive-rebase/pick.gif' class='img-bordered img-responsive center' />

### Reword
When selecting reword you will see the <em class='context-menu'>Reword commit message</em> modal open. Here you can edit the summary and description of your commit. 

<img src='/img/documentation/repositories/interactive-rebase/reword.png' class='img-bordered img-responsive center' />

### Squash
When you squash you are taking the child commit and in turn writing that commit to the parent commit. In order for squash to be an option there will have to be a parent child relationship. 

<img src='/img/documentation/repositories/interactive-rebase/squash.png' class='img-bordered img-responsive center' />

### Drop commit
Drop removes the commit from the branch, completes rebase and rewrites the commit graph.

<img src='/img/documentation/repositories/interactive-rebase/drop.gif' class='img-bordered img-responsive center' />

---

### Keyboard Shortcuts and Reset
Use keyboard shortcuts <kbd>P</kbd>ick, <kbd>S</kbd>quash, <kbd>R</kbd>eword and <kbd>D</kbd>rop to perform commit actions. If you wish to start over, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Reset</span></button>. 

<img src='/img/documentation/repositories/interactive-rebase/keyboard-shortcut-reset.gif' class='img-bordered img-responsive center' />