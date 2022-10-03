---

title: Git LFS FAQ
description: Frequently asked questions related to LFS.

---
***

## LFS Features &amp; interface

### I updated to v3.0.0 of GitKraken Client but I cannot find LFS anywhere?

You will need to make sure you have Git v1.8.5 and LFS v2.0.0 installed on your local machine.


### I switched repos and now I do not see the LFS BETA button. Where did it go?

It is most likely that you have switched to a repository that does not have LFS initialized. If you wish to initialize this repo with LFS, you can do so by navigating to the hamburger menu → LFS → Initialize LFS on this repo.

### I added a LFS tracking pattern in GitKraken Client but files with that pattern are not being tracked by LFS, what gives?

Only new files will be tracked by the newly added pattern. If files of the newly added pattern are already being tracked by Git, you will need to untrack them and then re-track them.

The easiest way to do this in GitKraken Client is to remove the files from the repository (Git will think they have been removed/deleted), commit, then re-add the files and re-commit. The re-added files should now follow your new tracking pattern.

### After trying to push my files, I see a prompt requiring my credentials. What credentials is it referring to?

This prompt occurs if your LFS server credentials are not cached. If you are using the same remote hosting service (such as GitHub), then enter the hosting service credentials.

If you are using an internal LFS server (or another LFS service), you will need to enter the credentials for the LFS server.

## Common Pitfalls

### Why is LFS STILL not showing up? 

If LFS is still not appearing as an option in GitKraken Client preferences menu, you may need to add it to your `Path` variable. This can happen if git or git LFS is not installed in the default directory. You should [Verify Git and LFS Versions](/git-workflows-and-extensions/intro-and-requirements/#verify-git-and-lfs-versions).

### SSH Keys in GitKraken Client and the CLI
Unlike most features in GitKraken Client, the LFS feature does require git for the CLI as well as LFS. This means that if you are trying to use SSH, your key will need to be configured in your GitKraken Client and for the CLI.

You can automatically generate an SSH Key in GitKraken Client in **Preferences -> Authentication -> General** and save wherever you want locally, or the key will be  in your `.gitkraken\profiles` folder if you generate from a specific integration. 

You can also use the SSH Agent option to setup and manage your keys, and then tell GitKraken Client to use your agent. [Adding an SSH Key to an SSH Agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) by GitHub

### Using LFS installed using Homebrew on macOS

If LFS was installed using Homebrew, it may not appear in your path. You can run `sudo launchctl config user path "/usr/local/bin:$PATH"` to add homebrew utilities to the PATH for GUI apps. You can see more information on this from the [Homebrew documentation](https://docs.brew.sh/FAQ#my-mac-apps-dont-find-usrlocalbin-utilities).

### Can't find your question here? 

[Contact us](https://www.gitkraken.com/contact) and ask away