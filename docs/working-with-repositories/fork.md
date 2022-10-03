---

title: Forking GitHub Repos
description: Fork your GitHub Repos using GitKraken Client.

---

If you are using the [GitHub integration](/integrations/github/) or the [GitHub Enterprise integration](/integrations/github-enterprise/), then you may fork repos right from GitKraken Client.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> The fork feature is only available through the <a href="https://support.gitkraken.com/integrations/github/">GitHub Integration</a>.</p>
</div>

***
## Forking a repo
To add a new fork, first [open a repository](/working-with-repositories/open-clone-init/#opening-an-existing-project) in GitKraken Client.

Then click the <button class='button button--success button--ui button--nolink'>+</button> icon when hovering over <em class='context-menu'><img src='/img/documentation/icons/gk-remote-icon.svg' style='height:1em;'> Remote</em> in the left panel and click on the <kbd>GitHub.com</kbd> or the <kbd>GitHub Enterprise</kbd> tab.

<img src="/img/documentation/repositories/add-remote.png" srcset="/img/documentation/repositories/add-remote@2x.png" class="img-bordered img-responsive center">

If GitKraken Client does not detect an existing fork of this repo, the app will present the option to fork the repo and then add it as a remote.

<img src="/img/documentation/repositories/fork/fork.png" srcset="/img/documentation/repositories/fork/fork@2x.png" class="img-bordered img-responsive center">

Click <button class='button button--success button--ui button--nolink'>Fork and Add Remote</button> to fork the repo on GitHub, and then add it as remote in GitKraken Client's left panel:

<img src="/img/documentation/repositories/fork/add-fork-remote.png" srcset="/img/documentation/repositories/fork/add-fork-remote@2x.png" class="img-bordered img-responsive center">

## Add an existing fork

Click the <button class='button button--success button--ui button--nolink'>+</button> icon when hovering over <em class='context-menu'><img src='/img/documentation/icons/gk-remote-icon.svg' style='height:1em;'> Remote</em> in the left panel and click on the <kbd>GitHub.com</kbd> or the <kbd>GitHub Enterprise</kbd> tab.

GitKraken Client will detect whether a fork exists, but has yet to be added as a remote in the app. Click <button class='button button--success button--ui button--nolink'>Add this Remote</button> to add the fork as remote.

<img src="/img/documentation/repositories/fork/detect-fork.png" srcset="/img/documentation/repositories/fork/detect-fork@2x.png" class="img-bordered img-responsive center">

And remember, you can always [add a remote](/working-with-repositories/pushing-and-pulling/#adding-remotes) for any repo that is reachable over HTTPS or SSH. 



