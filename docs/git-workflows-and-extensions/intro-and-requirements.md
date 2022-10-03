---

title: Git LFS Requirements
description: Learn how to configure and work with Git LFS within GitKraken Client.

---

## What is Git LFS and how does it work?

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/S03EEusFxoI?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Git LFS (<s>Legendary Fabled Squid</s> Large File Storage) is a Git extension for storing large binary files.

Git LFS allows the user to track binary files directly or by extension. After the files are tracked, Git LFS manages the files as Git normally would, while Git just maintains a text file with metadata about the binary file.

When viewing the diff of tracked LFS files in GitKraken Client, you will see a versioned URL, a generated SHA, and a size pertaining to the size of the original contents of the file:

<img src='/img/documentation/git-lfs/lfs-ref.png' srcset='/img/documentation/git-lfs/lfs-ref@2x.png 2x' class='img-responsive center img-bordered' />

Git LFS stores the binary file content on a custom server or via GitHub, GitLab, or BitBucket’s built-in LFS storage. To find the binary content's location, look in your repository’s `.git/lfs/objects` folder.

Git LFS uses a special Git Hook to handle pushing your LFS files to the special LFS location. Because LFS uses Git filters for handling diffs and proper storage, make sure Git Hooks can run on your machine.

When pulling or checking out a new branch, all files run through a smudge filter. The smudge filter puts a file into your working directory.

LFS reads the SHA stored in Git, then uses that to find the appropriate binary file in the `.git/lfs/objects` folder. If it does not find the file it needs, it attempts to download the file from the LFS server found in the local repository’s git config file.

Once the proper file is found or downloaded, Git LFS replaces the SSH-agent with the binary file in your working directory.

LFS uses the Git clean filter for changes ready for commit and runs when a file is staged. This filter reads the binary content from the file and converts it to a SHA, which will then be stored in Git while the original binary content will be stored in the `.git/lfs/objects` folder.

If you wish to learn more about how Git LFS works with Git, visit the [GitHub repository ](https://github.com/git-lfs/git-lfs) documentation.

***

## Git LFS Requirements

To enable LFS in GitKraken Client, you must first install Git and LFS. The minimum requirements are:

* Git version 2.3+
* LFS version 2.0.1+

<div class='callout callout--success'>
    <p><strong>Note:</strong> Usually GitKraken Clientdoes not require Git CLI to perform its operations. However, since we do utilize Git CLI to interact with LFS files you will need to have <a href="https://git-scm.com/" target="_blank">Git installed</a> on your machine if you plan to use LFS. </p>
</div>

### Verify Git and LFS Versions

To verify whether you have the proper version of Git installed, open a terminal or CMD and type the following:
```
git --version
```
You should see something like this:
```
git version 2.13.0
```
On Windows you may see some extra characters appended to the version which is expected. If an error appears, please install (or upgrade) Git on your machine.

GitKraken Client requires version 2.3+ to run LFS. To install or upgrade Git on your machine, visit the [git-scm website](https://git-scm.com/).

Run the following command in terminal or CMD to verify your machine's version of Git LFS:
```
git lfs version
```
You should get output similar to the following:
```
git-lfs/2.1.0 (GitHub; windows 386; go 1.8.1; git bd2c9987)
```
If you do not have Git LFS installed or you have a version less than 2.0.0 installed, visit the [Git LFS website](https://git-lfs.github.com/) to install the proper version.

After both Git and Git LFS are installed, verify that they are on your path either by running the commands above or by checking your path in the terminal.

<div class='callout callout--success'>
    <p><strong>Note:</strong> If GitKraken Client still cannot find Git or Git LFS, the terminal or CMD may be using a different path than the system or user path. For example, on OSX applications launched from the GUI have a different path than those launched from the terminal.</p>
</div>

On OSX and Linux, you can run the following command to see the location of Git LFS on the path:
```
which git-lfs
```
and this command to see the location of Git on the path:
```
which git
```
On Windows Command prompt, use:
```
where git-lfs
```
and:
```
where git
```

*On Windows you can add to your Path Environmental Variable with the following method:*

Search `Env` in the start menu.

<img src="/img/documentation/git-lfs/lfs-AddPathVariable-0.png" class="img-responsive center img-bordered">

Next navigate to `Environmental Variables...` <i class='fa fa-caret-right'></i> Double click **Path** <i class='fa fa-caret-right'></i> Click `New` to add the paths.

<img src="/img/documentation/git-lfs/lfs-AddPathVariable-1.png" srcset="/img/documentation/git-lfs/lfs-AddPathVariable@2x-1.png 2x" class="img-responsive center img-bordered">

<img src="/img/documentation/git-lfs/lfs-AddPathVariable-2.png" srcset="/img/documentation/git-lfs/lfs-AddPathVariable@2x-2.png 2x" class="img-responsive center img-bordered">

<img src="/img/documentation/git-lfs/lfs-AddPathVariable-3.png" srcset="/img/documentation/git-lfs/lfs-AddPathVariable@2x-3.png 2x" class="img-responsive center img-bordered">

You will likely need to add both git and git LFS (LFS can have multiple paths, you would want to add them all).
