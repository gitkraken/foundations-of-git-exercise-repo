---

title: Workspaces
description: Workspaces allow you to create groups of repositories.

---

GitKraken Workspaces allow you to create easily accessible groups of repositories, take action across multiple repos, view details about their state at a glance, and share them with your team.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong> 
            Workspaces can contain repositories hosted on GitHub.com, GitHub Enterprise, GitLab.com, GitLab Self-Managed, Bitbucket.org, and Azure DevOps. To create a Workspace, the integration must be connected under <kbd>Preferences > Integrations</kbd>.
    </p>
</div>

***

## Create a workspace

To create a Workspace, navigate to the Workspaces tab. If this is your first time creating one, select <button class="button button--success button--ui button--nolink">+ Create Worspace</button>. Otherwise, select <button class="button button--success button--ui button--nolink">+ New Workspace</button>.

You can give the Workspace a name, icon, description, and make it personal or shared with your organization. Under _Add repositories_, select which hosting service these repositories will be from. If you have not connected the integration, selecting that service will take you to the integration connection. Finally, select the desired repositories for the workspace and then <button class="button button--success button--ui button--nolink">Create Workspace</button>.

<img src="/img/documentation/repositories/workspaces/create-workspace.gif" class="img-bordered img-responsive center">

## Team Workspaces

Workspaces are available as either a *Personal* or *Team* type.

**Personal Workspaces** are only accessible by you on this machine.

**Team Workspaces** will be available for the selected teams within your organization. This helps ensure that everyone is up-to-date on the same set of repositories by offering <a href="https://support.gitkraken.com/working-with-repositories/workspaces/#multi-repository-actions">multi-repository actions</a> and the ability to <a href="https://support.gitkraken.com/working-with-repositories/workspaces/#pull-requests">work with all pull requests</a> from these repositories. 

<img src="/img/documentation/repositories/workspaces/workspace-type.png" srcset="/img/documentation/repositories/workspaces/workspace-type@2x.png" class="img-bordered img-responsive center">

Learn more about [how to create a team](https://support.gitkraken.com/start-here/teams/). 

## Edit a workspace

Edit a workspace by selecting the ellipsis <i class="fas fa-ellipsis-v"></i> icon by the Workspace name.

<img src="/img/documentation/repositories/workspaces/edit-a-workspace.png" srcset="/img/documentation/repositories/workspaces/edit-a-workspace@2x.png" class="img-bordered img-responsive center">

## Multi-repository actions

All repositories in a Workspace can be cloned, fetched, or opened at once, making it easy to get a new member of your team onboarded quickly or keep repository information up-to-date. Repositories can be effortlessly opened in GitKraken, in your <a href="/start-here/preferences/#external-editor">default editor</a>, or on their hosting service. 

To perform an action on multiple repositories, select the check box next to the repository name and then select the desired action from the options at the top.

<img src="/img/documentation/repositories/workspaces/multi-action.png" srcset="/img/documentation/repositories/workspaces/multi-action@2x.png" class="img-bordered img-responsive center">

## Repository statuses

Workspaces expose the state of all repositories so you can see the last checked-out branch, how many commits are ahead or behind the remote, and your work in progress with counts of modified added, deleted, and renamed files.

<img src="/img/documentation/repositories/workspaces/repos-status.png" srcset="/img/documentation/repositories/workspaces/repos-status@2x.png" class="img-bordered img-responsive center">


## Workspace breadcrumb in toolbar

The option to remove the Workspace breadcrumb in the toolbar can be toggled under <kbd> Preferences > UI Customization > _Show Workspace breadcrumb in toolbar_</kbd>.

<img src="/img/documentation/repositories/workspaces/breadcrumb-setting.png" srcset="/img/documentation/repositories/workspaces/breadcrumb-setting@2x.png" class="img-bordered img-responsive center">

## View Repository Details

You may select the list icon to open the repository details.

<img src="/img/documentation/repositories/workspaces/repository-details.png" srcset="/img/documentation/repositories/workspaces/repository-details@2x.png" class="img-bordered img-responsive center">

## Pull requests

The Pull Request section will show all open pull requests for all repositories within the selected workspace. Information shown here includes the pull request title, pull request number, CI status, the name of the branch being merged, and number of comments.

To view a workspaces pull requests, select a workspace and then select `Pull Requests`.

<img src="/img/documentation/repositories/workspaces/pull-requests.png" srcset="/img/documentation/repositories/workspaces/pull-requests@2x.png" class="img-bordered img-responsive center">

Select `Filter pull requests` to filter for pull requests with the following options:

* "Opened by Me", to show pull requests that were opened by the user. This filter is available for GitHub, GitHub Enterprise, GitLab, and GitLab Self-Managed repositories.
* "At Risk", to show any pull requests that are not drafts and have been open for longer than 7 days. This filter is currently only available for GitHub, GitHub Enterprise, GitLab, and GitLab Self-Managed repositories.
* "By repository", to limit the view to a single repo within the Workspace. This filter is currently available for Azure DevOps, GitHub, GitHub Enterprise, Gitlab, and Gitlab Self-Managed repositories.

The search allows searching by pull request titles for all services. For GitHub.com workspaces, <a href="https://docs.github.com/en/search-github/searching-on-github/searching-issues-and-pull-requests">GitHub's search syntax</a> can also be used.

<img src="/img/documentation/repositories/workspaces/filter-and-search.png" srcset="/img/documentation/repositories/workspaces/filter-and-search@2x.png" class="img-bordered img-responsive center">

At risk pull requests are pull requests that have not been updated in more than 7 days and are not in draft. This is shown for GitHub, GitHub Enterprise, GitLab and GitLab Self-Managed pull requests. This is indicated by the `At risk` label.

<img src="/img/documentation/repositories/workspaces/at-risk.png" srcset="/img/documentation/repositories/workspaces/at-risk@2x.png" class="img-bordered img-responsive center">

### GitHub pull request view

If you are working with a GitHub.com workspace, you may select a pull request to work with the <a href="/working-with-repositories/pull-requests/#github-pull-request-view">GitHub pull request view</a>. 

<img src="/img/documentation/repositories/workspaces/github-pull-request.png" srcset="/img/documentation/repositories/workspaces/github-pull-request@2x.png" class="img-bordered img-responsive center">