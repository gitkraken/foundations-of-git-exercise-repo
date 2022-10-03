---

title: New to Git
description: Learn how to get started with GitKraken Client.

---

Whether you are a newborn or a wizened deep-ocean octopod, this Getting Started Guide uses a basic workflow to provide an overview of GitKraken Client interface from cloning your repository to successfully executing Git actions.

***

## Learning Git with GitKraken

In this series, we'll provide Git tutorial videos. You'll learn Git concepts and how to apply them in GitKraken Client.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU" frameborder="0" gesture="media" allowfullscreen></iframe>
</div>

Interested in how version control fits into a DevOps workflow? Check out our [DevOps Tools Report](https://www.gitkraken.com/resources/devops-report-2020) to learn more.
***

## GitKraken Tutorials

Need a hand jumping into the product? Here's a playlist with a few video tutorials.

<div class='embed-container embed-container--16-9'>
<iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV78WqGmGSq8JPnafR3lAa55n" frameborder="0" gesture="media" allowfullscreen></iframe>
</div>

***

## Define local

Most of the work you do in GitKraken Client is using the local repository, meaning the files and changes are saved on your local machine.

You can easily identify any local branches in the graph as they are shown with the <em class='context-menu'><i class="fa fa-laptop" aria-hidden="true"></i></em> icon.

One of the reasons why Git is so fast when compared to other SCM tools is because all changes are made locally rather than on a remote server.  The local repository includes all of the branches, and changes made to the repo, since the time it was created.  

Because you make a copy of the entire remote repo, you can change branches, view history, and commit changes without needing a network connection.  It also means if there is a catastrophic event on the remote server, or if another user makes an unwanted change on a remote, all of the other members of the team would still have a copy of the full repo so it can easily be restored.

### .git folder
When initializing a Git repo or cloning from a remote, you will notice a `.git` folder in the project root.  This contains all of the information required for the Git repository and if this folder is deleted, you would no longer be able to switch branches, pull from remotes, or view commit history.

### Working directory
The working directory is the currently checked out version of the files in the local repository.  When you change branches, pull in changes, or reset, GitKraken Client will update the files in the working directory to reflect the changes.

For more information on Git repositories, check out the [Git repository tutorial](https://blog.axosoft.com/2016/10/28/git-tutorial-repository/) blog post including a video from one of our developers.

***

## Workflow Example
Once your repository is initialized and the [interface](/start-here/interface) is out of the way, it's time to get cracking ... _Whaahh-pssh!_ ... and tie all of the interface and concepts together to perform work on your repository.


Up until this point, you have created an entire folder representing your project with great potential. With this example, we'll take the next step and make a commit to production in a basic workflow.


### Branching
The newly initialized repository created results in a default `master` branch.  Synonymous with production, typically commits are not made directly to this, but rather are reviewed and merged in.

<div class='callout callout--basic'>
    <p>Branches can be thought of as an area to silo where to commit. Its reference is specifically a moving pointer to an individual commit object.</p>
</div>

<img src='/img/documentation/getting-started/create-new-branch.png' srcset='/img/documentation/getting-started/create-new-branch@2x.png 2x' class='img-bordered img-floated img-floated--right'>

On our newly created repo, we'll branch off from `master` to silo our normal development.  To do this, right-click master on the graph and select <em class='context-menu'>Create branch here</em>.  Let's call this branch `develop` in "_enter branch name_" which is going to be an indefinite main track branch to the project.

Once created, GitKraken Client will auto checkout `develop` and switch to that new branch.

### Changing file content
Now that `develop` is set, we can make some new changes without affecting anything on production.

In the example, the `README.md` file was created automatically to provide context about the project. This involves creating the file, writing content, and then saving it to disk.  With Git, the last step to save becomes more granular in order to write desired changes for revision history.  


`README.md` was created as a placeholder and the project can become more meaningful by modifying the file with the project context, as well as adding additional project files.  Any modifications and additions will have to be staged and committed, which will only affect our current branch.


You can select _Initial Commit_ from the graph, and click `README.md` to open the built-in editor.

<img src='/img/documentation/getting-started/open-file.gif' class='img-bordered img-responsive center'>

### Staging and Committing
Say you made changes to the `README.md` file. When selecting the _//WIP_ node, there will now be pending changes to `README.md` in the staging panel under _Unstaged Files_.

<img src='/img/documentation/getting-started/unstage.png' srcset='/img/documentation/getting-started/unstage@2x.png 2x' class='img-bordered img-floated img-floated--right'>

Next, let's move these changes into the _Staged Files_ section by selecting the green <button class='button button--success button--ui button--nolink'>Stage all changes</button> button.

Outside of Git, work is done in a typical <em class='context-menu'>File <i class="fa fa-caret-right"></i> Save</em> method or written automatically when changes are detected.  In a way, committing in Git is like the Save, where we've made a pointer to the changes in this current version of the file to keep in history.

From here, type a brief summary of your changes and click <button class='button button--success button--ui button--nolink'>Commit</button> to save your changes to the `README.md` file.  This effectively updates the reference on `develop`, pointing to your first modification after _Initial Commit_.

<div class='callout callout--basic'>
    <p>It's easy to distinguish between different types of changes including Added, Modified, Renamed, and Deleted files.</p>
</div>

Visit [staging](/working-with-commits/staging) for vast coverage of the topic, including staging individual lines or hunks of file changes. Be sure to check out [commits](/working-with-commits/commits) too.

### Merging
Now that our `develop` branch is up to date, we want to roll out these changes into production.

From the graph we see that `develop` is ahead of `master` by exactly 1 commit.  

<img src='/img/documentation/getting-started/graph-commit.png' srcset='/img/documentation/getting-started/graph-commit@2x.png 2x' class='img-bordered img-responsive center'>

In order to add this commit into the original branch, we will merge `develop` back into `master`.  This will take all of the changes introduced since the last commit and play them on this branch by performing a new commit (called a merge commit) with the changes.

There are a few ways to perform the merge action in GitKraken Client, but perhaps the easiest is from within the graph.

In the graph, you can see we have things in a new branch, `develop`, that we want in our source branch, `master`. Like any sensible person, we would only have to pick up `develop` and throw it at `master` right? Right! Simply drag `develop` and drop it on `master` to get the merge option.

<img src='/img/documentation/getting-started/draganddrop.gif' class='img-bordered img-responsive center'>

Alternatively the same merge can be performed through right click and other means.  Revisit and learn more about merging and other options available through [Branching and Merging](/working-with-repositories/branching-and-merging).

### Summary

In the end, this is as simple as it gets in terms of workflow and paves the way for incorporating changes into [pushing and pulling](/working-with-repositories/pushing-and-pulling) or venturing to advanced models like [GitFlow](/git-workflows-and-extensions/git-flow).

Remember, you must crawl before you can walk and without a doubt you will be running in no time!

Below is a sample video on how a simple commit is created as was explained in this guide.  For more topics `checkout` the rest of the categories and pages listed.

Your quest continues!


<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/9YCO-3_MApI?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>
