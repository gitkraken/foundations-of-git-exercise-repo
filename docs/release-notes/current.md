---

title: GitKraken Client Release Notes
description: View a history of the new features and fixes in GitKraken Client's Version 8.
og_image: /img/GitKrakenClient-Hero.png

---

Behold the evolution of GitKraken Client! Find out what&rsquo;s new, what&rsquo;s fixed, or just take a trip down memory lane with a nostalgic swagger, remembering those bugs of yesterday.

<a href="https://www.gitkraken.com/download" target="_blank" class="button button--basic ">Download Current Version Now</a>

Check out our [GitKraken Roadmap](https://www.gitkraken.com/git-client/roadmap) to see what we’re working on.

***
<a id="v8-5-0"></a>
## Version 8.5.0

### Tuesday, May 17th, 2022

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/DJhsfHyL_m8?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>

_The GitKraken team is proud to announce these improvements to Workspaces, Teams, and the GitKraken CLI. Lower your blast shield, trust your feelings, and prepare for the release of GitKraken Client v8.5._


### New ✨

_Git is what gives a dev their power...It binds the galaxy together._

- GitKraken WorkSpaces now support Azure DevOps repositories.
    - Any Workspace created for Azure DevOps will automatically include repos for a selected Azure Project.
    - Workspaces can currently support up to 100 repositories for an Azure Project.
- Visual interactive rebase can now be initiated from the GitKraken CLI, which you can access from a Terminal Tab or a Repo Tab by clicking the <kbd>Terminal</kbd> icon in the top toolbar.
    - Users can type either `gk rebase -i` or `gk rebase --interactive` along with two refs to open the interactive rebase view. If only one ref is passed it will perform the rebase of the branch currently checked out onto the specified ref.

### Improvements 🙌

_An elegant Git client for a more civilized age._

- Git LFS Improvements:
    - Users will experience a reduced delay in updating the graph and commit detail panel when selecting commits in LFS enabled repos.
    - Note: Significant work towards reducing checkout times for LFS repos is underway and we plan to include these improvements in the GitKraken Client v8.6.0 release, scheduled for June.
- When creating a new Team, members can now be added as part of the creation process.
- Team members are now sorted by username in the Teams section, found in the left panel of GitKraken Client.
- Improvements to GitKraken Workspaces: 
    - Workspaces can now be shared as Team Workspaces, allowing users to share the Workspace with specific teams within their Organization.  
	- In the Workspaces Repository view, clicking on the name of a repository will open it in a Repo Tab. 
        - Users can view repository information by clicking on the Open Repository Details option, found on the right side of the Repositories view.  
    - Organization admins and owners will see a new "Show All Workspaces" checkbox, allowing a simplified way to see all available Workspaces.  
    - Users can now leverage [GitHub’s search syntax](https://docs.github.com/en/search-github/searching-on-github/searching-issues-and-pull-requests) when using the Workspaces Pull Requests view search.
    - Users will find more options for filtering in the Workspaces Pull Requests view. The new options include: 
        - "Opened by Me", to show pull requests that were opened by the user. This filter is available for GitHub, GitHub Enterprise, GitLab, and GitLab Self-Managed repositories.
        - "At Risk", to show any pull requests that are not drafts and have been open for longer than 7 days. This filter is currently only available for GitHub, GitHub Enterprise, GitLab, and GitLab Self-Managed repositories.
        - "By repository", to limit the view to a single repo within the Workspace. This filter is currently available for Azure DevOps, GitHub, GitHub Enterprise, Gitlab, and Gitlab Self-Managed repositories.
- For Windows users, GitKraken Client will now respect the `core.longpaths` setting in `.gitconfig`. Previously, GitKraken Client had its own longpaths setting independent of the user’s `.gitconfig` setting.
    - On Windows, `core.longpaths` now only applies to the files in the working directory, not in the .git directory, to maintain compatibility with Git for Windows.
- GitKraken CLI autocomplete will now be able to suggest more than one argument in these commands: 
    - `git add` 
    - `npm install`
    - `npm remove`
    - `yarn add`
    - `yarn remove`
- Notifications with a Call to Action will now be marked as read when the CTA is clicked.
- Users encountering merge conflicts can now right-click on the conflicts shown in the Commit Panel to reveal new options for easier and faster conflict resolution. The new options available are: 
    - "Take current", which applies the changes from the branch currently checked out to resolve the conflict.
    - "Take incoming", which applies the changes from the incoming branch to resolve the conflict.


### Bug Fixes 🐛

_Bugs…You will never find a more wretched hive of scum and villainy._

- GitKraken Client will now open as expected for users on OpenSSL 3 Linux distributions such as Ubuntu 22.04 and Fedora 36.
- Users will see increased performance when opening a commit diff for very large images. Large images will now display as a binary file Instead of producing an error.
    - For large files, such as images and other media, we recommend using [Git LFS](https://support.gitkraken.com/git-workflows-and-extensions/git-lfs/). 
- Dotted graph lines will no longer take precedence when overlapping with solid lines in graph views.
- Users can now type in the GitKraken Terminal as expected on a wider range of OS versions.
- When un-hiding a remote, users can continue hiding or un-hiding remotes without waiting for the triggered automatic fetch to resolve.
- Azure DevOps integrations and all self hosted integrations will now work properly on our new Teams license tier.
- Users with hundreds or thousands of Azure DevOps Projects will see improved performance when integrating Azure DevOps.
- Users can now use quotation marks when naming Workspaces.
- All Organization and Team actions will remain available after using the login screen.
- The scrollbar in the GitKraken Terminal will now remain clickable in all situations.
- When a user pushes many files up at once to GitHub, they will no longer experience an OAuth infinite loop.
- Opening repositories via `gitkraken --path <path>` when GitKraken is already open will now work as expected.




***
<a id="v8-4-0"></a>
## Version 8.4.0

### Tuesday, April 12th, 2022

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/CqyP-y5zWf4?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>


_We want to help teams cut out all the jibber-jabber when working with pull requests across multiple repos. Get ready for GitKraken Client v8.4, a release that will have you saying "I love it when a pull request comes together."_

### New ✨
_I pity the tool that does not have Workspaces or the GitKraken CLI._


- GitKraken Workspaces:
    - Workspaces now include a Pull Requests view!
        - Users can filter PRs to see items "Assigned to me".
        - At-risk pull requests are highlighted through a label and filterable.
        - Selecting any GitHub pull request now shows the user a new Pull Request view that presents users options to quickly manage PRs across a whole Workspace.
    - Clicking on any repo in a Workspace now shows see more info and options. Users will see the repository's README, as well as quick access buttons to open the repository in a Repo Tab, Terminal Tab, or on the remote repository's hosting provider.


- GitKraken CLI:
    - The <kbd>Terminal</kbd> button in a Repo Tab’s toolbar will now open the GitKraken CLI inside a Terminal Panel, instead of opening a new Terminal Tab. Users can still open new Terminal Tabs through a New Tab, the Command Palette, or through any Terminal’s context menu.
    - Users can toggle the Terminal Panel on and off by pressing the Terminal button in Repo Tab toolbar, through keyboard shortcut <kbd>Ctrl+`</kbd>, the Command Palette, the Terminal Panel’s context menu, or options in the GitKraken Client's View menu. Toggling the Terminal Panel will turn it on or off across all Repo Tabs.
    - A Terminal Panel session can also be terminated by executing the `exit` command. This will only close the Terminal Panel and not the Repo Tab. Toggling the Terminal Panel back on will initialize a new terminal session. 
    - Unlike with the Terminal Tabs, navigating to a different working directory in a Terminal Panel will not change the repository opened in the Repo Tab.
    - The following `gk` commands are available in the Terminal Panel:
	    - `gk blame`
	    - `gk diff`
	    - `gk history`
	    - `gk help`

### Improvements 🙌
_Making GitKraken Client a mean, clean Git managing machine._

- Users will now see helpful icons when shown GitKraken CLI Autocomplete suggestions, helping clarify to which command the suggestion is related.
- Git LFS users will see improved performance checkouts. 

### Bug Fixes 🐛
_Shut up, bugs!_

- Filtering Autocomplete suggestions by name will work as expected.
- After selecting between multiple Autocomplete suggestions that have the same prefix, further suggestions will disappear as expected.
- Users will no longer be allowed to create Workspaces for repositories on unsupported versions of GitLab Self-Managed services.
- Bitbucket Server users will now see the branches correctly populated when creating Pull Requests.



***

<a id="v8-3-3"></a>
## Version 8.3.3

### Wednesday, March 16th, 2022

_The improvements to GitKraken Client keep Marching forward._

### Improvements 🙌

- Users creating an account or signing in will see an improved user experience

***

<a id="v8-3-2"></a>
## Version 8.3.2

### Monday, March 7, 2022

_What is Keif's favorite kind of bug? The fixed ones!_

### Bug Fixes 🐛
- GitKraken Client now supports GitHub’s new GraphQL query types. GitHub users will now see creating, commenting and reviewing pull requests work as expected.

***

<a id="v8-3-1"></a>
## Version 8.3.1

### Monday, February 28, 2022

_Spring is almost here, but we couldn't wait to bring you these improvements in GitKraken Client v8.3.1._
### Improvements 🙌

_Though short, February is filled with lots of love and sweet improvements._

- GitKraken CLI:
    - Users who want to use the GitKraken Terminal when opening repositories in external terminals, <kbd>alt/⌥ + T</kbd>, can now set this as the default by navigating to <kbd>Preferences</kbd> → <kbd>General</kbd> → <kbd>Default External Terminal</kbd> and selecting "GitKraken Terminal" from the dropdown menu. 
    - When hiding the visualization panel orientated to the top of the window, the toolbar will remain in place at the top.
- Themes:
    - Users can customize the terminal colors together with the rest of their custom themes. This update removes the <kbd>Terminal Theme</kbd> setting from the <kbd>Preferences</kbd> → <kbd>Terminal</kbd> menu.

### Bug Fixes 🐛

_The early birds of spring get the bugs._

- GitKraken Client will remain responsive when adding an [issue tracker integration](https://support.gitkraken.com/start-here/integrations/) supporting a large number of assignable users.



***

<a id="v8-3-0"></a>
## Version 8.3.0

### Monday, February 14, 2022

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Nh9aQ8RUyP4?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>

_The GitKraken team is going for the gold medal in speed and usability! Sharpen your blades and get ready for the release of GitKraken Client v8.3!_


### New ✨
_I got a need…a need for speed._


GitKraken Client v8.3 introduces a new ARM64 compatible version, offering native support for Apple Silicon architectures, as used in Macs with M1 chips.

GitKraken Workspaces are now available for repositories hosted on GitHub Enterprise and GitLab Self-Managed.

### Improvements 🙌

_There are no speed limits on the road to success._

- Mac users will get optimal performance without needing to run the ['Big Sur workaround'](https://www.gitkraken.com/blog/workaround-gitkraken-big-sur-issues) from a terminal, which had been required to fix the partial signature issue introduced in macOS Big Sur. 
- Fedora 35 users will no longer need to pass the `--no-sandbox` flag to launch GitKraken Client.
- GitKraken CLI:
    - New Terminal settings added under <kbd>Preferences</kbd> → <kbd>Terminal</kbd>.  
		- Default Directory - Users can now set the default directory where new Terminal Tabs will open when initiated from the "New CLI Tab" button in the Repo Management Tab or from the Comand Palette. 
        - Line Height - Users can set how much space appears between each line printed to the terminal.  

    - Autocomplete suggestions have been added for `git flow`commands.
    - Any user created global or local [Git aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases) will be shown as  autocomplete suggestions. 
    - The `git reset` command will now suggest staged files too.
    - Autocomplete suggestions for `git add` will show relative paths when called from inside a subfolder.
    - The visualization panel will automatically open after making the initial commit in a new repo.
    - Right mouse clicking in a Terminal Tab will open a new context menu allowing users to open new Terminal Tabs, paste into the terminal, and close the terminal, among other actions.

- Themes:
    - Users can customize the commit graph colors in their custom themes.  Examples of `// graph colors` have been added to the default theme files.  Users can refer to  <kbd>Preferences</kbd> → <kbd>UI Customization</kbd> -> <kbd>Theme</kbd> to locate the GitKraken Client theme folder on their computer.  


### Bug Fixes 🐛

_You take a crash, you get back up, and next time you succeed. That’s a great feeling._

- Pull requests filtering in the left panel is no longer case sensitive.
- Users on GitLab Self-managed +13.8 will no longer get directed to a 404 page when selecting `Generate a token on GitLab`.
- When using the Pull Request panel for forks using Azure DevOps based repositories, users will no longer see a `no options` error on the form.
- GitKraken CLI:
    - Using reverse search (<kbd>ctl+r</kbd>) will no longer cause unintended autocomplete suggestions.
    - Updated autocomplete suggestions for `git gc`, fixing spelling issues.
    - Autocomplete suggestions for paths with spaces in them have been improved.

***

<a id="v8-2-1"></a>
## Version 8.2.1

### Tuesday, December 21, 2021

_Everyone needs elbow room._

### Improvements 🙌

- The Workspaces tab can now be closed to save space in the tabs bar while not in use. A small icon has been added to quickly reopen the tab when needed.


***

<a id="v8-2-0"></a>
## Version 8.2.0

### Monday, December 13th, 2021

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/eEPoQLv52W0?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>


_Get ready for a multiverse bending reveal!  We are unleashing the cosmic power of GitKraken Workspaces with the release of GitKraken Client v8.2!_

### New ✨
_We have helped users progress and seen them accomplish wonders._

#### Introducing GitKraken Workspaces

GitKraken Workspaces save teams time by providing an easy way to group repositories, take actions against multiple repositories at once, and quickly onboard new team members. 

GitKraken Workspaces allow you to gather and access all the required repos for your project in a single tab in GitKraken Client. The new GitKraken Workspaces tab shows you the status for the last branch that you checked out, how far ahead and/or behind in commits you are, and if there is an active WIP for each included repository. 

GitKraken Workspaces can be created as Personal, only visible to you, or Shared, visible to all members of your Organization.  

 - Users can access GitKraken Workspaces from the new “Workspaces” tab in the tabs bar, from the New Tab view, from the command palette, which can be opened with the keyboard shortcut <kbd>cmd/ctrl + p</kbd>, or from the newly added repository breadcrumb in any Repo Tab.

- Users can view details and trigger the following actions on any or all of the repositories in a workspace at once:
    - Clone multiple repositories at once. This will help teams quickly onboard a new team member or get a new computer up and running.
    - View the last checked out branch for all repositories and see if a branch is ahead/behind a remote.
    - View work in progress for all repositories, including the number of files modified, added, renamed, or deleted. 
    - Perform a fetch for all or a selection of repositories.
    - Open multiple repos in GitKraken Client, or in an external editor, such as VS Code, IntelliJ, Atom, or Sublime Text.
    - Open any repository in the associated hosting service website.

- GitKraken Workspaces can currently contain repositories hosted on GitHub.com, GitLab.com, or Bitbucket.org.

#### Themes:

- Users may now create their own custom GitKraken Client themes. 
    - For more information about creating a new custom theme, checkout our [Themes documentation](/start-here/themes/) or navigate to `gitkraken/themes/README.md`.

- Users will find two new themes when navigating to <kbd>Preferences</kbd> → <kbd>UI Customization</kbd> menu.

- Users can now sync their GitKraken theme with their system theme, if their OS supports it.

#### Activity status:

- An activity status will now display on the avatars of members in your GitKraken Organization or Team, indicating if they are actively using GitKraken Client. This activity status icon is visible in the Team View section in the Left Panel, or in the Organization view in Preferences.

- Users can manually set their status to “Active” or “Away” by selecting the circle icon in the top right corner, or by opening the <kbd>Profile/Account</kbd> dropdown menu.

GitKraken Workspaces and Activity status are currently unavailable for Self-Hosted and Stand-Alone customers. 

### Improvements 🙌
_When you love something, you improve it._

- GitKraken CLI:
    - Users can now customize the behavior of the <kbd> ↹ Tab</kbd> key when using auto-complete in a Terminal Tab. This setting can be found under <kbd> Preferences </kbd> → <kbd>Terminal</kbd>  → <kbd> Tab Behavior</kbd>.
    - Users can customize the cursor used in a Terminal Tab. This can be configured in <kbd> Preferences </kbd> → <kbd>Terminal</kbd>  → <kbd>Cursor Style</kbd>. Users can select either Block, Underline or Bar for their cursor.
    - Auto-complete suggestions will now show branches and tags as options when running `git diff` or `git reset` commands.
    - The `gk diff` command now supports tags and branches as options.
    - Auto-complete suggestions have been added for `npm` and `yarn`.

- When users open the pull request panel and click on a pull request while the left panel is minimized, GitKraken Client will now open the pull request view.

### Bug Fixes 🐛
_We came here years ago to protect users from these bugs._

- When using the GitKraken CLI, suggestions will disappear as expected after auto-completing a command with escaped characters in the path.

- After using GitKraken Client to execute a cherry-pick and resolving any arising conflicts, the Git CLI will no longer report that a cherry-pick is currently active.

- When creating a pull request in a repository with a large number of forks, users will no longer have to wait as all forks are being fetched before opening the dropdown menu.

***
<a id="v8-1-1"></a>
## Version 8.1.1

### Tuesday, November 9th, 2021

_Get ready to celebrate the release of GitKraken Client v8.1.1 with these puns you can tell next time you are hanging out at the ol' foo bar. If you don't get these jokes, `whoami` to judge?_

### Improvements 🙌
_`Sudon't` want to miss out on these new improvements._

- GitKraken CLI Preview:
    - GitKraken CLI users can now use `git help` to display help information about using Git.
    - Windows users will now see an auto-suggest option for the `cd` command.
    - Users changing directories in a Terminal Tab will see auto-suggest options showing the end of the folder path rather than just the beginning. This is useful when long directory names are present.

- Users can choose from more [Keif options](https://www.gitkraken.com/keif-gallery) for their avatars when creating or editing their Profiles. 

### Bug Fixes 🐛
_There are only 10 kinds of bugs: the ones we have fixed and the ones that we have not identified yet._

- GitKraken CLI Preview:
    - Improved Terminal Tab support for custom fonts, such as Nerd Fonts and Powerline fonts.
    - Users leveraging oh-my-posh in Powershell using custom themes will now see and be able to select auto-suggest options.
    - Users can now resize the commit panel in a Terminal Tab.
    - All Mac users are now able to use the `gk` commands.
    - Windows users leveraging “Constrained” language mode in Powershell can now execute `gk` commands.
    - Users can now resize the merge editor tool as expected when the visualization panel is positioned to the left or right in a Terminal tab.

- When working with GitHub and GitLab wiki repos, GitKraken Client will no longer throw an error message about being unable to fetch pull requests.
- If a user checks out a commit while in [Solo mode](/working-with-repositories/hiding-and-soloing/), they will now see the `HEAD` reference displayed.
- Users fetching GitHub pull requests will no longer see timeouts.

### Stand-Alone & Self-Hosted 🏢
_There is no place like `~`_

- The GitKraken CLI Preview is now available for Self-Hosted and Stand-Alone customers.

***

<a id="v8-1-0"></a>
## Version 8.1.0

### Thursday, October 14th, 2021

_Autumn brings sweaters, pumpkin spice, and apple picking. It is also bringing some awesome updates to GitKraken Client as we release v8.1.0!_

### New ✨
_The seasons continue to change and so does GitKraken Client...for the better!_

- GitKraken Client can now identify weak SSH keys and provide an easy way to remove and replace them. Read more on [the GitKraken blog](https://gitkraken.com/blog/weak-ssh-key-issue-fix).

### Improvements 🙌
_It's the time of year to reap the harvest of new improvements to the GitKraken Git client._

- GitKraken CLI:
    - GitKraken CLI users can now use reverse search as expected by typing <kbd>Ctrl+R`</kbd> in the terminal.
    - Mac users will now see the `LANG` environment variable pass automatically to the shell process.
    - When selecting an auto-suggest option with the mouse, GitKraken Client will now refocus on the terminal prompt.
    - The GitKraken CLI now supports 256 colors.
    - Mac and Linux users will now see auto-complete suggestions for the `cd` command.
    - When running `gk blame`  or `gk history`, users will now see suggestions when navigating from inside a repository's subdirectory after typing `../`.  
    - Users will now see auto-suggest options for the `git gc` command.
    - In addition to showing or hiding the visualization panel, users can now orient it to the top, bottom, left, or right, as well as toggle the right-side commit panel using the visualization panel toolbar.
 
- The user interface for user profile settings under the [Preferences] menu has been improved.
- Users can now open specific comments on GitHub.com from the comments inside GitKraken Client's pull request or issue views.
- Users who are not using [GitKraken Integrations](https://support.gitkraken.com/start-here/integrations/) will no longer be repeatedly prompted for credentials for each remote when connected to repositories with multiple remotes sharing the same hostname.  

### Bug Fixes 🐛
_As the leaves fall, so do these bugs._

- The overall reliability of notification delivery has been improved.
- Auto-complete for Windows users leveraging the GitKraken CLI has been improved.
- Windows users will no longer see a Named Pipes error when running `gk` commands in a terminal tab.
- Using `gk diff` in the GitKraken CLI will produce properly parsed numerical SHAs.
- When discarding a large number of files in a repository, the repo will fully load as expected. 

***

<a id="v8-0-1"></a>
## Version 8.0.1

### Tuesday, September 28th, 2021

_Everyone: “I am loving v8.”_<br>
_GitKraken: “Let’s make the experience even better!”_

### Improvements 🙌

- GitKraken Client users can now search for a particular tab and navigate the menu using the keyboard when using the tab dropdown menu.

### Bug Fixes 🐛

- Replaced the SSH key generation library with one that generates stronger keys. Read more on [the GitKraken blog](https://gitkraken.com/blog/weak-ssh-key-issue-fix).
- Gitflow branch folders and tag folders collapse and expand as expected when selected in the left panel in GitKraken Client.
- Layout and options have been optimized in the Organization panel in GitKraken Client's Preference view.

***

<a id="v8-0-0"></a>
## Version 8.0.0

### Tuesday, September 21st, 2021

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/PrjLwxsivLg?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>

_"It began with the forging of the Great <del>Rings</del> Kraken."_

The true power of the Fellowship of developer collaboration is unleashed in GitKraken Client's v8.0!
### New ✨

_“One tool to rule them all,_ <br>
_One tool to find them,_ <br>
_One tool to bring them all_ <br>
_and in the Git log bind them.”_

#### Introducing the GitKraken CLI Preview

The GitKraken CLI adds a Git-enhanced, keyboard-driven, terminal experience to GitKraken Client. Get the powerful Git visualizations GitKraken Client is known for—like the commit graph—in the context of a Terminal Tab. Plus auto-suggest and auto-complete for Git commands to help you drive (and learn) Git faster, with fewer mistakes.

Dive deeper into file changes with the `gk` commands. Use the command `gk history` to see File History and `gk blame` to see what has changed in a file or commit and who made those changes. 

During the GitKraken CLI Preview we are looking for feedback to help improve this feature. Please use the `Feedback` form linked in the bottom right corner of your GitKraken Client app, or email us at feedback@gitkraken.com.


- Users can open Terminal Tabs in a number of ways:
    - Clicking the "New Terminal Tab" button after opening a New tab in GitKraken Client.
    - From the "Terminal" button in the toolbar of a Repo tab (opens the current repo in a Terminal Tab).
    - From the Command Palette (<kbd>Ctrl/Cmd + P</kbd>).
    - When working in a Terminal Tab, you can open a new Terminal Tab with the key combination <kbd>Ctrl/Cmd + T</kbd>. The new Terminal Tab will open in the same working directory. 

- Auto-complete and auto-suggest make building Git commands easier than ever before in the GitKraken CLI. This feature works for users of PowerShell for Windows, ZSH and Bash for Mac/Linux. 
    - Auto-complete and auto-suggest are configured for the most common Git commands, but we are continuing to build out this feature and would love feedback on which commands and parameters you want added. 
    -  Please be aware that other auto-complete programs could potentially cause the GitKraken CLI auto-complete to stop working. You may need to uninstall or disable those other programs to use this feature.
    - Note: If you switch shells, you'll need to set the new shell as default in your operating system settings and restart your computer for auto-complete to continue working as expected.

- Some of the legendary Git visualizations that GitKraken Client is known for are also accessible within Terminal Tabs. To quickly view the commit graph, file diff, history, and blame view, simply type these commands:
    - `gk panel`: toggles the visualization panel on or off. You can also reposition the panel to the top, bottom, left, or right by adding those parameters to the command.  For example `gk panel right` moves the panel to the right of the screen. 
    - `gk graph`: shows the graph view. While this command has similar behavior to `gk panel`, even allowing repositioning of the graph with the same top, bottom, left, or right parameters, this command also returns to the graph if you're in a different view and has subcommands for toggling the graph columns with the keyboard.
    - `gk history` and `gk blame`: open the history or blame panel for a specified file.
    - `gk diff`: shows changes between commits. If no commit SHAs are provided, it will use your WIP and HEAD. If only one commit SHA is provided, it will be compared with HEAD.
    - `gk --help`: shows the list of available `gk` commands. You can also use --help on a specific `gk` command to see its arguments.
    - A toolbar above the panel will display the current repository name, branch, tag, and the number of changes pending to be pulled and/or pushed. Clicking this toolbar will toggle the panel on or off.
    - For Free accounts, this visualization panel will only be accessible within publicly-hosted repositories.

- A Terminal section has been added to the Preferences menu that allows Terminal Tab customization:
    - Font choice. Changes to this setting will only apply to new Terminal Tabs.
    - Font size.
    - Enable auto-complete & auto-suggest.
    - Default the visualization panel position when opening a new panel: top, right, bottom, or left.
    - Show the visualization panel by default. This will apply only when opening new tabs.
    - Terminal theme.

The GitKraken CLI Preview is currently unavailable for Self-Hosted and Stand-Alone customers. 
<br>
<br>
#### Deep Linking

_"Oh, it’s quite simple. If you are a friend, you speak the password, click the link, and the doors will open."_

We've added the ability to share deep links to specific remote repositories, commits, branches, and tags in GitKraken Client. This allows users to more easily collaborate and save time when working in issue queues or Git pull requests.  

- When shared, these links will both open and focus GitKraken Client to the linked repository. The links will focus GitKraken Client on the commit, branch, or tag specified. When specifying a branch, the latest commit of that branch will be focused.
- The links can be found in GitKraken Client's context menus under `Copy link to remote/commit/branch/tag`.
<br>
<br>

#### Jira App Integration - Git Integration for Jira
_"It’s the Jira ticket that’s never started that takes the longest to finish."_

GitKraken Client now works with the Git Integration for Jira app to allow quick navigation between the client and Jira when viewing commits and file diffs related to Jira issues.

- In GitKraken Client, you’ll find buttons and links to open the following in Git Integration for Jira:
    - File diffs - within the file diff view and in file context menus.
    - Commits - context menu when right-clicking commits in the graph.

- In the Git Integration for Jira, anywhere you view commits and diffs will automatically  have links to open them in GitKraken Client.

- To leverage GitKraken’s Git Integration for Jira integration you will need to:
    - Connect Jira Cloud Integration in the GitKraken Git Client.
    - Select Jira Cloud as the Issue Tracker for a repository.
    - Select a Jira Project.
    - Install Git Integration for Jira on the same Jira Cloud instance as the Jira Project.
### Improvements 🙌
_"Even the smallest update can change the course of history."_


- The Fuzzy Finder is now the Command Palette! 
    - We've renamed the Fuzzy Finder to the Command Palette. You can still open the command palette through the keyboard shortcut <kbd>Ctrl/Cmd + P</kbd>, or through the new magic wand icon in the toolbar.
- Tab navigation has been significantly improved when many tabs are open at once.
    - We have improved the tooltips to provide both tab title and repo information.
    - Tooltips will now instantly appear when hovering the entire tab, not just the title.
    - A new dropdown list has been added to the tabs bar to help with tab navigation.
- Reopening tabs after a “close all tabs to the right”, a “reopen closed tab” will now reopen only one tab at a time, instead of all that were closed at once.
-   An option to “Quote Reply” has been added for comments in the PR view.
- The profile menu now shows the Organization associated with the current profile.
- A “Cancel Rebase” button has been added at the top right of the Interactive Rebase panel for easier access.
- We have improved form, prompt, and modal keyboard navigation and submission.
- Improved user experience for the login form.

### Bug Fixes 🐛
_"You (bugs) shall not pass!"_

- Styling of long branch names in the right panel has been improved.
- Users will no longer see issues for remotes without access to a repo, as happens when users leave an organization or when forks are deleted. 
- When using the delete key to erase spaces in a URL, the cursor will behave as expected. 
- The Pull Request icon has been added back to branch labels in the graph.
- The bottom of Diff views are no longer cut off when the file mode changes.
- Relative paths are now allowed in hooksPath.
- All users are now able to select a project for GitLab and GitLab-Self-Managed issues on the left panel.
- If Sublime Text 4 is installed, it will now be detected and appear in the external editor dropdown. 
- Debouncing has been added in the left panel search. Searches will be executed when you stop typing, instead of on each letter, making it easier to find what you’re looking for.
