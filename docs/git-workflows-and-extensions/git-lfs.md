---

title: Initialize and Configure Git LFS
description: Learn how to initialize and configure Git LFS within GitKraken Client.

---

Once you meet the [System Requirements](/git-workflows-and-extensions/intro-and-requirements/#git-lfs-requirements
), initialize LFS on an existing repo or create a repo and initialize LFS from the start.

***



## Initializing LFS on an existing repo

Navigate to your Preferences and you should see the LFS tab in the left panel:

<img src='/img/documentation/git-lfs/lfs-tab.png' srcset='/img/documentation/git-lfs/lfs-tab@2x.png 2x' class='img-responsive center img-bordered' />

<div class='callout callout--warning'>
    <p><strong>Note:</strong> If you do not see the LFS tab, make sure you have a GitKraken Client v3.0.0+ installed and you meet these <a href="/git-workflows-and-extensions/intro-and-requirements/#git-lfs-requirements">System Requirements</a>.</p>
</div>

Click to initialize LFS on the repo:

<img src='/img/documentation/git-lfs/init-lfs.png' srcset='/img/documentation/git-lfs/init-lfs@2x.png 2x' class='img-responsive center img-bordered' />

Exit preferences to access two new things: an LFS button in the toolbar and an unstaged change to the `.gitattributes` file that needs to be committed.

<img src='/img/documentation/git-lfs/lfs-toolbar.png' srcset='/img/documentation/git-lfs/lfs-toolbar@2x.png 2x' class='img-responsive center img-bordered' />

Stage and commit the changes to the `.gitattributes` file to finish the LFS initialization.  

Existing files need to be untracked from Git and re-tracked to count as LFS files.  Consider removing the files from the repository (Git will think they have been removed/deleted), commit, then re-add the files and re-commit.

The re-added files should now follow your new LFS tracking pattern.

## Initializing LFS on a new repo

When you initialize a new repository, you will have the option to _Initialize with LFS_.

<img src='/img/documentation/git-lfs/init-with-lfs.png' srcset='/img/documentation/git-lfs/init-with-lfs@2x.png 2x' class='img-responsive center img-bordered'/>

## Configuring LFS

Once LFS is initialized on a repository, add tracking patterns to the `.gitattributes` file.  These tracking patterns will tell LFS which files to monitor in your repository.  

<img src='/img/documentation/git-lfs/tracking-patterns.png' srcset='/img/documentation/git-lfs/tracking-patterns@2x.png 2x' class='img-responsive center img-bordered'/>

Access the `.gitattributes` file by going to <em class='context-menu'>Preferences <i class="fa fa-caret-right"></i> LFS</em> or by editing the `.gitattributes` file directly in your text editor.  

As another option, add tracking patterns to the repository’s `.gitattributes` file through the Unstage pane in the right panel.

Select the WIP node, right click the file you wish to be tracked by LFS, and select the desired option under LFS.

<img src='/img/documentation/git-lfs/context-menu.png' srcset='/img/documentation/git-lfs/context-menu@2x.png 2x' class='img-responsive center img-bordered' />

<div class='callout callout--success'>
    <p>Note: GitKraken Client will automatically perform an LFS pull after cloning a repo or initializing a submodule with LFS </p>
</div>