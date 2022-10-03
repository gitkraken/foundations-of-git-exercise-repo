---

title: Pushing and Pulling
description: Pushing and Pulling data from Remote Repos.

---

Pushing and pulling are the keys to collaboration.  🤝

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/Lb4yvfrX_7I?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>


***
## Adding Remotes
To add a new remote, click the <button class='button button--success button--ui button--nolink'>+</button> icon when hovering over <em class='context-menu'><img src='/img/documentation/icons/gk-remote-icon.svg' style='height:1em;'> Remote</em> in the left panel, then fill in the remote URL.  

<img src="/img/documentation/repositories/add-remote.png" srcset="/img/documentation/repositories/add-remote@2x.png" class="img-bordered img-responsive center">

When using an integration like GitHub or Bitbucket, select the remotes from your collaborators in the dropdown box.  This makes viewing other forks of the same repository quick and easy.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> When using an integration, the drop-down box will only display <strong>Forks</strong> of this repository. If you would like to add a remote that is not a fork you can still do so via the URL option.</p>
</div>

You can identify remote branches in the graph through the following icons:

 + <em class='context-menu'><i class="fab fa-github"></i></em> &mdash; GitHub
 + <em class='context-menu'><i class="fab fa-bitbucket" aria-hidden="true"></i></em> &mdash; Bitbucket
 + <em class='context-menu'><i class="fab fa-gitlab" aria-hidden="true"></i></em> &mdash; GitLab
 + <em class='context-menu'><i class="fab fa-windows" aria-hidden="true"></i></em> &mdash; Azure DevOps
 + <em class='context-menu'><i class="fa fa-globe" aria-hidden="true"></i></em> &mdash; Other Remote Server

All remote branches are located in the left panel.

***

## Push <img src='/img/documentation/icons/gk-push-icon.svg' style='height:1em;'>
Pushing takes any local changes <em class='context-menu'><i class="fa fa-laptop" aria-hidden="true"></i></em>, and making them available on the remote <em class='context-menu'><i class="fa fa-globe" aria-hidden="true"></i></em>.  

Push the currently checked out branch by clicking <kbd>Push <img src='/img/documentation/icons/gk-push-icon.svg' style='height:1em;'></kbd> in the main toolbar, or by right clicking on the branch, and selecting <em class='context-menu'>Push</em>.

<img src="/img/documentation/repositories/push.png" srcset="/img/documentation/repositories/push@2x.png" class="img-bordered img-responsive center">

Pushing attempts to upload any new commits to the remote branch, then fast-forward the remote to bring it up to date with the local repo.  

If the remote branch cannot be fast-forwarded, the push will be refused.  If this is the case, GitKraken Client will provide the option to _Pull (fast-forward if possible)_, or <button class='button button--danger button--ui button--nolink'>Force Push</button>.  

<div class='callout callout--warning'>
    <p><strong>Caution:</strong> Forcing a push is considered destructive because it overwrites the remote branch by replacing it with the local branch.</p>
</div>

If the branch pushed does not exist on the remote, GitKraken Client will prompt you to name and create the new remote branch.  This is typically the fork name followed by a slash, and the branch name. i.e. `origin/my-branch`.

### Drag and drop to push

Drag and drop a branch to a remote to access the <kbd>Push</kbd> action. You may drag a branch to a remote branch on the graph, or to a remote branch listed in the left panel.

<img src="/img/documentation/repositories/drag-and-drop-to-push.gif" srcset="/img/documentation/repositories/drag-and-drop-to-push.gif" class="img-bordered img-responsive center">

***
## Fetching
Pulling and fetching take updates from the remote and get them into our local repo.

<img src="/img/documentation/repositories/pull-options.png" srcset="/img/documentation/repositories/pull-options@2x.png" class="img-bordered img-responsive center">

### Fetch All
Fetching gets updates from remote branches, but does not update any files in your working directory.  

Updates will appear in the graph, and also update any branches on the left to show how many commits you are ahead or behind.

When you're behind the remote, it means that there are commits on the remote branch which have not been incorporated into the local repo. _Pull (fast-forward if possible)_ to get these changes on local.  

<img src="/img/documentation/repositories/fetch.png" srcset="/img/documentation/repositories/fetch@2x.png" class="img-bordered img-responsive center">

If you are ahead of the remote branch, there are local commits that have not yet been pushed to the remote.

It is possible to be both ahead of and behind a remote.  However if you are both ahead and behind a remote, you will not be able to perform a _Pull (fast-forward if possible)_ as the branches have diverged. Consider rebasing onto the remote first.

GitKraken Client automatically fetches updates from your remote repositories every minute by default.  You can change this setting from <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> General</em> menu.

### Fast-forwarding
Fast forwarding moves the currently checked out commit to one that was added later, replaying all commits in between in the order which they happened.  

<img src="/img/documentation/repositories/pull-options.png" srcset="/img/documentation/repositories/pull-options@2x.png" class="img-bordered img-responsive center">

To fast-forward your currently checked out commit, you can right click on the branch with newer commits, and select the <em class='context-menu'>Fast-Forward</em> option from the menu.  

<img src="/img/documentation/repositories/pushing-pulling/fast-forward.png" srcset="/img/documentation/repositories/pushing-pulling/fast-forward@2x.png" class="img-bordered img-responsive center">

***
## Pulling <img src='/img/documentation/icons/gk-pull-icon.svg' style='height:1em;'>
Pulling first performs a fetch and then incorporates any commits in the remote repository into the local copy.  

There are three pulling options. Let's demonstrate what each one does by starting with an example 2 commits made locally, and 2 that have been made on the remote.
<figure class='figure center'>
    <img src='/img/documentation/repositories/ahead-behind.png'>
    <figcaption>The remote commits display on the graph because they have been fetched,</br>but have not been incorporated into the local repo.</figcaption>
</figure>

### Pull (fast-forward if possible)
_Pull (fast-forward if possible)_ fetches any updates on the remote branch, then attempts to _fast-forward_ the local branch.  If a _fast-forward_ is not possible, a _merge_ will be performed.  

This is the default option for new GitKraken Client users.

<figure class='figure center'>
    <img src='/img/documentation/repositories/example-pull-ff.png'>
    <figcaption>A fast-forward was not possible, so the remote branch was merged into the local branch.</figcaption>
</figure>

### Pull (fast-forward only)
_Pull (fast-forward only)_ fetches any updates and then attempts a _fast-forward_.  If a fast-forward is not possible, GitKraken Client will not make any changes to the local repo.

In our 2-commit example, a fast-forward is not possible as there are new commits added to both branches.

### Pull (rebase)
_Pull (rebase)_ stashes all commits on this branch, pulls in new commits from the remote, and then replays your commits.  This has the added benefit of maintaining all commits in a single line, as opposed to creating branches which are then merged back together.  

<figure class='figure center'>
    <img src='/img/documentation/repositories/example-pull-rebase.png'>
    <figcaption>The remote commits were pulled in, then the local commits were moved on top of them.</figcaption>
</figure>

<div class='callout callout--basic'>
    <p><strong>Note</strong>: Remember the golden rule of rebasing, <em>'Never rebase while you're on a public branch'</em>, which is covered in our <a href='https://blog.axosoft.com/2016/10/20/golden-rule-of-rebasing-in-git/'>blog post</a>.</p>
</div>

### Setting a default pull option
Set the default pull option by clicking the down arrow to the right, and clicking on the circle button by each option.  

<img src="/img/documentation/repositories/pushing-pulling/set-default.png" srcset="/img/documentation/repositories/pushing-pulling/set-default@2x.png" class="img-bordered img-responsive center">

Our [interface](/start-here/interface) page covers this and more.


***
## Setting the upstream branch
Whenever pushing, pulling, or fetching, GitKraken Client gets updates from the _Upstream_ branch.

The _Upstream_ defaults to the remote branch where the local branch was checked out, but you may change the _Upstream_ to push, pull, or fetch from a different branch.  

Right click on a branch to <a href="https://gitkraken.com/learn/git/problems/git-set-upstream-branch" target="_blank">set the upstream</a> or click the <kbd> <i class="fa fa-ellipsis-v"></i> </kbd> option.

<img src="/img/documentation/repositories/upstream.png" srcset="/img/documentation/repositories/upstream@2x.png" class="img-bordered img-responsive center">

Alternatively, drag and drop a branch to push instead of setting upstream. 

<img src="/img/documentation/repositories/pushing-pulling/drag-and-drop.gif" class="img-bordered img-responsive center">