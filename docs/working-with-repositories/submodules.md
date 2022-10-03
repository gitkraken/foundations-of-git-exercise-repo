---

title: Submodules
description: Submodules allow you to include other Git repositories within another Git repository. Work with submodules in GitKraken Client.

---

Submodules allow you to include other Git repositories within a Git repository and can be managed directly inside of GitKraken Client.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/moC2KyxGb10?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***
## Adding submodules
Add a submodule by clicking the <button class='button button--success button--ui button--nolink'>+</button> when hovering over <em class='context-menu'><img src='/img/documentation/icons/gk-submodules-icon.svg' style='height:1em;'> Submodules</em> in the left panel. Paste the HTTPS or SSH link to the repository, and then enter the path.

<img src="/img/documentation/repositories/add-submodule.png" srcset="/img/documentation/repositories/add-submodule@2x.png" class="img-bordered img-responsive center">

Adding a submodule to the repository adds a link to the submodule's repository in the <code>.gitmodules</code> file.  

When the parent repository is cloned, it includes the reference to any submodules and the submodules require initialization.  

Your repository tracks the submodule's checked out commit.  If there are any updates to the submodule, the files will not automatically update your working directory.  

### Updating submodules

To update submodules, navigate to the Submodule pane in the left panel and right click on the submodule.

<img src="/img/documentation/repositories/update-submodule.png" srcset="/img/documentation/repositories/update-submodule@2x.png" class="img-bordered img-responsive center">

If you clone a repository that contains a submodule, you will be prompted to initialize the submodule.  This will clone the submodule's repository and check out the referenced commit.

### Changing pointer commit
To change the pointer commit, open the submodule in GitKraken Client and then check out the new commit. You may need to first create a branch on the target commit before you can check it out.

Then when you exit the submodule, GitKraken Client will detect the change and ask you if you wish to save the change.

<img src="/img/documentation/repositories/submodule-commit.png" srcset="/img/documentation/repositories/submodule-commit@2x.png" class="img-bordered img-responsive center">



### Statuses
Below are possible statuses of your submodules and their remedies:

- _Out of sync_ -- The checked out commit of the submodule has changed.  There is a change to the submodule reference in your work in progress that should be stashed, committed or discarded.  

- _Added but not initialized_ -- Right click and select initialize.
- _Added and initialized but not committed_ -- When adding a submodule, commit the submodule folder to the repository and insert the reference to the submodule in the <code>.gitmodules</code> file.

### GitKraken Client and subtree, not submodules
GitKraken Client does not currently support subtree in-app.
