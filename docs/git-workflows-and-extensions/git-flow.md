---

title: Gitflow
description: Gitflow is a list of rules to keep a repo’s history organized, and is used to make the release process, bug fixes, and feature creation easier.

---

Gitflow is a list of rules to keep a repo’s history organized, and is used to make the release process, bug fixes, and feature creation easier.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/eTOgjQ9o4vQ?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***
## Configuration
First initialize Gitflow in <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Gitflow</em> and change the default branch names if desired.

<img src="/img/documentation/repositories/gitflow/gitflow.png" srcset="/img/documentation/repositories/gitflow/gitflow.png" class="img-bordered img-responsive center">

Once initialized, two branches will always be present: `master` (The version in production) and `develop` (The version currently in development for the next release).  

Changes are merged into these branches.  If you do not currently have these branches in your local repository, GitKraken Client will create them when Gitflow is initialized.

***
## Usage
With Gitflow initialized in your repo, you will get an additional menu in the left panel.  Start or finish any of your Gitflow branches here.

<img src="/img/documentation/repositories/gitflow/git-flow-start.png" srcset="/img/documentation/repositories/gitflow/git-flow-start@2x.png" class="img-bordered img-responsive center">

Create new Gitflow branches by clicking the green button on the Gitflow menu on the left.  

Or whenever you add a branch, include the prefix for the Gitflow branch type i.e.
`feature/branch-name`.  Any branches that do not have the prefix, will be displayed in the local
repository section, but not in the Gitflow menu.

<img src="/img/documentation/repositories/gitflow/git-flow-folders.png" srcset="/img/documentation/repositories/gitflow/git-flow-folders@2x.png" class="img-bordered img-responsive center">

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Gitflow has the benefit of adding all features, hot-fixes, and release branches in different folders.</p>
</div>

Gitflow branches can be pushed to a remote which is the same as '_Publishing_' the Gitflow object in the command line.

### Feature
Feature branches are used for new features or bug fixes.  They typically exist only in local repos and aren't shared with others.  

When finishing a feature branch, GitKraken Client will merge the feature branch into `develop`, and delete the feature branch from the local repository.

<img src="/img/documentation/repositories/finish-feature.gif" class="img-bordered img-responsive center">

You also have the option to rebase the `feature` branch on top of `develop`.

### Release
Releases are major and minor versions of your product.  They're often shared with other collaborators working on the same version.  

When finishing a release, the release branch is merged into both `master` and `develop` branches. This creates a tag with the release name for future reference.

<img src="/img/documentation/repositories/finish-release.gif" class="img-bordered img-responsive center">

### Hotfix
Hotfixes are the same as Releases in Gitflow, except hotfix branches are created on top of `master`, while release branches are created on top of `develop`.

Hotfixes are for quickly pushing out a change to your production branch.  Common examples of hotfixes are fixing typos, and bugs that need to be pushed out as soon as possible to production.  

When finishing a hotfix, GitKraken Client will merge the changes into both `master` and `develop`.  

<img src="/img/documentation/repositories/finish-hotfix.gif" class="img-bordered img-responsive center">
