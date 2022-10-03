---

title: Preferences
description: Customize your GitKraken Client experience to match your tastes!

---

Navigate to <i class="fas fa-cog"></i> <em class='context-menu'>Preferences </em> to customize your GitKraken Client experience. Here are what each of the major sections do.


<img src="/img/documentation/getting-started/preferences.png" srcset="/img/documentation/getting-started/preferences@2x.png 2x" class="img-responsive center img-bordered">

*** 

## Organization

This section will actually be labeled with your organization name rather than "Organization".  It shows the members and teams within your organization. Click `switch organization` to swap to another organization.

The Owner and any Admins are able to:

- Change role of members within the organization
- Invite members to the organization and purchase licenses
- Create and manage teams


<div class='callout callout--warning'>
    <p><strong>Note:</strong> the Organization section is only availibe to users who have a Pro or Enterprise license.
</p>
</div>

## General

### Auto-Fetch

Set the number of minutes between auto-fetches. This value must be between 0 and 60 minutes, and it will fetch all visible remotes for the repository. Setting the value to 0 minutes will disable auto-fetch.

If you’re experiencing issues with performance, consider setting your auto-fetch value to 0 and restarting the application. 
 
### Auto-Prune

Removes any remote-tracking references that no longer exist on the remote.

### Default Branch Name

Set the default name when initializing a new repo. The app defaults to `main`.

### External Merge Tool

This is where you may set your preferred external merge tool. 

- [Supported Merge Tools](/working-with-repositories/branching-and-merging/#external-merge-tools)
 
### External Diff Tool

There is where you may set your preferred external diff tool.

- [Supported Diff Tools](/working-with-commits/diff/#external-diff-tools)

### External Editor

You may open a repo in your preferred external editor program using the [Command Palette](/start-here/command-palette/). Supported editors include:

- VS Code
- Atom
- Sublime
- IntelliJ


### Delete ".orig" files

GitKraken Client will make .orig files during a merge. If turned off, these before and after files will not be automatically deleted. 

### Default Terminal

You may open the current repo folder in terminal by navigating to  <em class="context-menu">File <i class='fa fa-caret-right'></i> Open Terminal</em> or use the keyboard shortcuts <kbd>opt</kbd> + <kbd>T</kbd> (Mac) / <kbd>alt</kbd> + <kbd>T</kbd> (Windows + Linux). 

Set your preferred terminal from this preference option for this action.
 
### Use Custom Terminal Command

Enables the option to specify a custom command to open a terminal window. 

For example, to set up GitKraken Client to open Powershell 7, use the command ` start "" "C:\Program Files\PowerShell\7\pwsh.exe" -noexit -command "cd %d"`

### Show All Commits in Graph

Enabling this option will force GitKraken Client to always show all commits in repo. 
This setting may cause performance issues with large repositories.

### Max Commits in Graph

Set the max number of commits GitKraken Client will show in the graph. 
Lower counts may help improve performance, and the minimum value is 2000 commits.

### Remember tabs

This will remember open tabs when you quit GitKraken Client. This option will also remember what tabs you have open for each profile. 

### Longpaths (Windows Only)

For Windows users, GitKraken Client will respect the `core.longpaths` setting in the global .gitconfig. Adjusting this setting will change `core.longpaths` in your .gitconfig. `core.longpaths` only applies to the files in the working directory, not in the .git directory, to maintain compatibility with Git for Windows.

### AutoCRLF (Windows Only)

For Windows users, GitKraken Client will respect the `core.autocrlf` setting in the global .gitconfig. Adjusting this setting will change `core.autocrlf` in your .gitconfig. Enabling this option auto-converts CRLF line endings into LF when adding a file to index, and vice versa when checking out code onto your file system. For more information check out this [git documentation](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_core_autocrlf)

### Use extended logging in activity log

Provides more information for the activity log. You may access the activity log from <em class="context-menu">Help <i class='fa fa-caret-right'></i> Support Logs <i class='fa fa-caret-right'></i> Activity Logs</em>.

### Forget all Usernames and Passwords

Removes credentials that currently stored by GitKraken Client.

### Share work-in-progress status with my team

Allows other users in your team to see your local work in progress files. This is directly related to the [Teams](/working-with-repositories/teams) feature.

## Profiles

GitKraken Client uses profiles to store your app preferences, current [Tabs](/start-here/interface/#tabs), and Git config information.

[Learn more about Profiles](/start-here/profiles)

## SSH & Integrations

GitKraken Client supports HTTPS and SSH authentication, and provides useful integrations with many Git hosting services. Here's how to get started.

- [General SSH settings](/integrations/authentication/#ssh)
- [GitHub Integration](/integrations/github/)
- [GitHub Enterprise Integration](/integrations/github-enterprise/)
- [GitLab Integration](/integrations/gitlab/)
- [GitLab Self-Managed Integration](/integrations/gitlab-self-hosted/)
- [Bitbucket Integration](/integrations/bitbucket/)
- [Bitbucket Server Integration](/integrations/bitbucket-server/)
- [Azure DevOps Integration](/integrations/visual-studio-team-services/)
- [TFS, AWS CodeCommit, custom service, etc](/integrations/authentication/)
- [Jira Cloud Integration](/integrations/jira/)
- [Jira Server Integration](/integrations/jira-server/)

## Notifications

GitKraken Client's notification system is designed to tell you about updates, bug fixes, product tips, and more. The following preferences are available:

- Enable Desktop Notifications
- Receive Marketing Notifications
- Receive Help Notifications

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Marketing notifications can only be disabled by Pro users.
</p>
</div>


## UI Customization

The following UI preferences are available:

- [Theme](/start-here/themes)
- Notification location
- Show toolbar icon labels
- Enable spell checking
- Display author initials instead of avatars (Gravatar) 
- Show GitKraken Boards button in toolbar
- Show GitKraken Timelines in toolbar
- Show commit author in graph
- Show commit date/time in graph
- Show commit sha in graph

## GPG Preferences

Learn more about how to [configure GPG signing](/git-workflows-and-extensions/commit-signing-with-gpg/#configure-gpg-in-gitkraken) in GitKraken Client.

## Editor Preferences

Customize the following settings for your GitKraken Client editor and diff:

- Font
- Font size
- Tab size
- End of line character
- Syntax highlighting
- Show line numbers
- Word wrap

## Terminal

These settings only effect `Terminal` tabs.

- Font
- Font Size
- Enable Autocomplete Suggestions
- Show Graph Panel by Default
- Terminal Theme
 
## Repo-Specific Preferences

Repo-Specific preferences only apply to the repo currently open in GitKraken Client. The following preferences are repo-specific:

- [Gitflow](/git-workflows-and-extensions/git-flow/)
- [Git Hooks](/working-with-repositories/githooks/)
- [Commit Template](/working-with-commits/commits/#commit-templates)
- [LFS](/git-workflows-and-extensions/intro-and-requirements/)
- [Issues](/integrations/jira/)
- [Team](/working-with-repositories/team-view)

You may configure unique repo-specific settings for each repo.

