---

title: Detached HEAD state
description: Learn how to enter detached HEAD state to interact with commits without impact to other branches

---

Git power-users of GitKraken Client: rejoice! Entering detached HEAD state is just a right click away.

***
Detached HEAD state gives you the power to check out any commit and explore the older state of a repository without having to create a local branch. 

### Entering detached HEAD state

Right click on the commit you’d like to checkout, and navigate to <kbd>Checkout this commit</kbd>. 

<img src='/img/documentation/working-with-files/commits/checkout.png' srcset='/img/documentation/working-with-files/commits/checkout@2x.png 2x' class='img-bordered img-responsive center'>

The checked out commit will be tagged as `HEAD`, serving as your indication that you’ve entered detached HEAD state. 

<img src='/img/documentation/working-with-files/commits/head-tag.png' srcset='/img/documentation/working-with-files/commits/head-tag@2x.png 2x' class='img-bordered img-responsive center'>

You now have access to the full history of the commit. 

### Leaving detached HEAD state 

Feel free to stay a while; you can look around, make some experimental changes and commit them, all without impacting other branches. The commits you make in this state are “detached” from the rest of your project’s development - so when you’re ready to discard the commits you’ve made in this state, simply checkout a branch. 

When you check out a branch, the `HEAD` tag indicator will disappear and your repo will be business as usual. 

<img src='/img/documentation/working-with-files/commits/discard-commits.gif' class='img-bordered img-responsive center'>
 
<div class='callout callout--danger'>
    <p><strong>IMPORTANT:</strong> Any commits made in detached HEAD state will be lost when you check out any branch. 
</p>
</div>

Luckily, GitKraken Client will explicitly remind you of your detached state when you make a commit. You'll find this warning in at the top of the commit panel.

<img src='/img/documentation/working-with-files/commits/detached-warning.png' srcset='/img/documentation/working-with-files/commits/detached-warning@2x.png 2x' class='img-bordered img-responsive center'>

### Keeping your commits 

If you hit that stride and create changes in the detached HEAD state that you’d ultimately like to keep, you can easily do so by right clicking on your checked out commit and selecting <kbd>Create branch here</kbd>.

<img src='/img/documentation/working-with-files/commits/create-branch.png' srcset='/img/documentation/working-with-files/commits/create-branch@2x.png 2x' class='img-bordered img-responsive center'>

### Recovering lost commits

If you unintentionally checkout another branch, you can [Undo](https://support.gitkraken.com/working-with-commits/undo-and-redo/) to recover the commit. If you are unable to undo the change, these commits will still be tracked in the repository. Using the CLI, you can use [git reflog](https://git-scm.com/docs/git-reflog) to find the SHA of the missing commit and [git checkout <SHA\>](https://git-scm.com/docs/git-checkout) to checkout that commit.