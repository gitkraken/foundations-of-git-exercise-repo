---

title: Working with Git LFS Files
description: Learn how to work with LFS files within GitKraken Client.

---

When a file matches a pattern that is being tracked by LFS, an LFS tag appears next to the file name in the right panel.

<img src='/img/documentation/git-lfs/lfs-tag.png' srcset='/img/documentation/git-lfs/lfs-tag@2x.png 2x' class='img-responsive center img-bordered' />

Clicking on the file shows the LFS reference information:

<img src='/img/documentation/git-lfs/lfs-ref.png' srcset='/img/documentation/git-lfs/lfs-ref@2x.png 2x' class='img-responsive center img-bordered'/ >

Staging and committing LFS tracked files results in the reference files being saved to your local repo and the actual files being saved to your local LFS cache.  

Once your repo is pushed to an LFS-capable remote, the reference files will be saved to the remote repo and the actual files will be pushed to your specified LFS server.

Most LFS actions, such as Checkout, Fetch, Pull, and Push will happen automatically as you use the standard commands in GitKraken Client. However, if you want to use an LFS command in isolation, use the LFS toolbar menu:

 <img src='/img/documentation/git-lfs/lfs-dropdown.png' srcset='/img/documentation/git-lfs/lfs-dropdown@2x.png 2x' class='img-responsive center img-bordered' />

Click the arrow on the button and select the desired command. Other than _Prune_, all of the commands are run by GitKraken Client via the traditional operations.

<div class='callout callout--success'>
    <p><strong>Note:</strong> Pruning is not automatic. Pruning is considered a destructive operation, so be careful about when you run the <em>Prune</em> command. See the <a href="https://github.com/git-lfs/git-lfs/blob/master/docs/man/git-lfs-prune.1.ronn" target="_blank">Git LFS documentation</a> to learn more.</p>
</div>
