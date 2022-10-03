---

title: GitKraken Client Beta
description: View a history of the new features and fixes in GitKraken Client's Beta Versions.
og_image: /img/GitKrakenClient-Hero.png

---


***
## 0.9.2

<h3>Thursday, Mar 17, 2016</h3>

**Begone ye devil white screen!** 

<h3>Fixed</h3>

*   Got rid of the constant white-screening while opening a repo that some of you folks were experiencing.

***
## 0.9.0

<h3>Wednesday, Mar 16, 2016</h3>

**Fully submerse with submodules** 

<h3>New</h3>

*   We heard you and **submodules** are now supported! Say hello to the new section in the left panel to initialize an existing submodule or add one to track. Let GitKraken Client [Submodule-ception](https://twitter.com/GitKraken/status/710240612948254720) begin.

<h3>Improved</h3>

*   Welcome the **resizable graph**, a valuable addition on the interface side! Drag the vertical bar to obtain precisely how much of the graph you want to see. This also allows you to have a completely collapsed and minified graph at will!
*   New buttons for _Mark Resolved_, _Mark Conflicted_, and _Open Merge Tool_ for improvements in the _Merge Conflict_ panel to get you in the flow and resolving conflicts faster and more efficiently.
*   The _Amend_ checkbox for commits looked bad at one point and should not look bad. We adjusted the style to give our seal of quality.
*   In File View, the styling of the preview when hovering over commit in condensed graph has been updated to be up to spec, including font and colors.

<h3>Fixed</h3>

*   With the new resizable graph, now getting two honorable mentions here, when there are a large number of branches on the repository we have the ability to show an accurate graph, and you can always control how much you want to see.
*   Failing on _Open Merge Tool_? Not anymore it's not. We made some changes when the merge tool is not found and when there is no common ancestor of the commits.
*   The merge conflict panel will open accordingly when applying a stash which conflicts with changes.
*   We'll present a message when there are failures on remote actions.
*   The client will not crash when there are unicode characters in the file path name of the repository to be opened.
*   Fixed a small leak with fetching from prolonged use.

***
## 0.8.3

<h3>Monday, Mar 7, 2016</h3>

**White screen on repo open fix**

<h3>Fixed</h3>

*   Fixed an error that some people were seeing the app white screen after opening a repo.

***
## 0.8.2

<h3>Monday, Mar 7, 2016</h3>

**Bitbucket fix!**

<h3>Fixed</h3>

*   Fixed an error that would break fetching/pushing with Bitbucket.

***
## 0.8.1

<h3>Friday, Mar 4, 2016</h3>

**Search by Field, OAuth & More!** 

<h3>New</h3>

*   **Level Up!** SEARCH INDEX grew to Level 2!  
    SEARCH INDEX has learned a new skill: **Search by Field**.  
    Use one or combination of the following when searching:
*   `sha:` full hash of commit
*   `message:` commit message description
*   `author:` author of changes
*   `email:` email of author

<h3>Improved</h3>

*   **OAuth** will now properly flow through your external browser and communicate on authorization success or failure.
*   Also in Authentication, relevant configuration for SSH will only be shown when _Use local SSH agent_ is disabled.
*   Make a best effort to set defaults on creating a new pull request if unable to authenticate when fetching the origin.
*   The order of colors has been updated in the graph for a more optimized contrast resulting in a prime exhibition of the work you've done. The colors of the rainbow so pretty in the sky~~

<h3>Fixed</h3>

*   Successfully loading merge tools to resolve merge conflicts. Common locations on Mac for merge tool defaults will be located accordingly.
*   Perform a revert on a merge commit rather than producing an error.
*   We won't allow spaces when naming a branch.
*   Present a nice error message and refresh the graph if there is a merge conflict when finishing a branch through gitflow.

***
## 0.8.0

<h3>Friday, Feb 26, 2016</h3>

**File History Class, Blame Game, and Pull Requests!** 

<h3>New</h3>

*   **File History** is now available through the context menu of a file in the diff panel. This will bring up an evolved Diff View showing the timeline of commits. Use keyboard shortcuts to navigate or click the short commit SHA to quickly jump and show diffs.
    *   <kbd>⌘</kbd>+<kbd>↑</kbd> on Mac / <kbd>Ctrl</kbd>+<kbd>Home</kbd> on Windows/Linux to switch to the first commit entry
    *   <kbd>⌘</kbd>+<kbd>↓</kbd> on Mac / <kbd>Ctrl</kbd>+<kbd>End</kbd> on Windows/Linux to switch to the last commit entry
*   _Blame_ revisions in the new File View tab also present in the history section to see how and when the file changed, and by whom. Select a commit entry by author to display changes at that point in time and toggle _Show blame details_ to see more or less annotation for the change.
*   Looking to get your contributions reviewed and merged in asap without leaving GK? There's no more wait as **Pull Requests** are now accessible in the left panel on repositories. Fetch from the open list and quickly create PRs for GitHub or Bitbucket!

<h3>Improved</h3>

*   Ridin’ spinners! For _Remotes_ in the left panel, there is now a spinning icon for indicating when there is an active fetch in progress. They'll stop when the operation completes.
*   In _Add Remote_ the Select list has evolved to allow pulling the list or typing to find a desired repository from both GitHub and Bitbucket.
*   _Add Remote_ is also case insensitive now, disallowing adding remotes of the same name but different casing.
*   Updated ability cross-platform to locate merge tools in _Preferences_.
*   Accurate messaging for when Bitbucket authentication fails or has expired.

<h3>Fixed</h3>

*   Many crash issues eradicated. So many. The elusive fatal error in white screen of death when opening a repo has been addressed.
*   If you happened to commit in the future like us or had a different method of birthing a child commit before its parent, it was possible for a commit appearing unusually orphaned in a merge on the graph. This is not a problem anymore as we've adjusted the sort for it to display correctly.
*   Updated references for the possibility of removing a remote during an active fetch, preventing a repo from being reopened.
*   Autofetch interval will work for remotes when switching from one repo to another.
*   We'll gracefully recover on the chance a commit search index becomes corrupt and loads forever. Seek and ye shall find.

***
## 0.7.2

<h3>Thursday, Feb 25, 2016</h3>

**Bug fixes!**

<h3>Fixed</h3>

*   No more crashing when viewing a very small diff in Linux.
*   Fixed an error when opening up certain repos with submodules.
*   Fetching will now result in more fetching and less crashing.

***
## 0.7.0

<h3>Tuesday, Feb 16, 2016</h3>

**More functionality. More stability.**

<h3>New</h3>

*   Right-click a ref label in the graph to change the upstream through **Set upstream**
*   Push a local branch directly to remote via drag-and-drop even when the target remote is not the set upstream.
*   As an alternative to the left panel, in the graph quickly _checkout_ through double-click on a ref label.
*   Questioning previous commitments? Now you can right-click on a commit entry in the graph to **revert commit** and reverse unwanted changes—you know, for those times you want to take back the engagement ring.

<h3>Improved</h3>

*   Windows builds were updated and now run smoothly on both 32- and 64-bit Windows.
*   Looking for more information about us and the current GitKraken Client version you're running? We thought you were and that's why GitKraken Client _About_ menu received a brand new update to contain more detail.

<h3>Fixed</h3>

*   The improved file view mode for the diff panel has horizontal scrolling again! Scroll right 80 characters and beyond, no matter how much real estate the display has. You'll see line numbers too!
*   **Bitbucket** team-owned repositories are now accessible through the service.
*   Validating credentials to improve error messaging and also prompting for login only when necessary.
*   There's no more file lock issue in specific cases and saving modified files while running GK at the same time is allowed, and encouraged!

***
## 0.6.2

<h3>Monday, Feb 1, 2016</h3>

**More Bugfixes!**

<h3>Fixed</h3>

*   Fixed search index loading.
*   Fixed app getting into an unresolveable merge state.

***
## 0.6.1

<h3>Friday, Jan 29, 2016</h3>

**Bugfixes!** 

<h3>Fixed</h3>

*   Disconnecting from GitHub now removes any SSH keys added via the application.
*   Searching through Bitbucket repositories now shows all of them, instead of just 10.

***
## 0.6.0

<h3>Wednesday, Jan 27, 2016</h3>

**Open Beta and Bitbuckets of Love** 

No more waiting for invites! The time has come and now everyone can be a part of the beta for testing. The steps are simple:

Step 1: Download  
Step 2: **GitKraken Client!**

<h3>New</h3>

*   **Bitbucket** is now supported in GK for direct interaction with your public and private repositories! Bitbucket can be configured for _Services_ in your Preferences and utilized when cloning repos and adding remotes.
*   The existing GitHub integration in _Services_ now conveniently generates SSH key pairs and adds the public key to GitHub. Or, optionally, an existing key can be added to your user profile.
*   A new file view mode has been introduced for the diff panel. This automatically triggers the tiny graph for commits and loads file changes in an expanded panel for a pleasant viewing experience and comparison. This includes revamped styling for staging which has optimal contrast for the light or dark side.
*   One more time: closed beta testing is complete! Instantly get started with GitKraken Client following download and install during the new open beta!

<h3>Fixed</h3>

*   _Please login to continue:_ We'll only ask if we need to and we'll check your configured authentication first. As a result, using connections to several hosting providers such as **GitLab** are now available! We've also included other SSH fixes with this for services.
*   Searching in _Open Repo_ will correctly show repositories with `.` periods in the name.
*   Gitflow and its settings will continue to hang out in the left panel following the slight chance master and develop branches have been deleted.
*   `\n` newlines will correctly display in the diff panel for a change.
*   No more crashing on aborting a merge or rebase, _Discard all changes_, or stash, when working with a bajillion files.
*   Further improved performance with staging along with focusing commits with a enormous number of files in the changes.

***
## 0.5.1

<h3>Friday, Jan 15, 2016</h3>

**More flow with Gitflow** 

<h3>New</h3>

*   For **Gitflow**, we'll remember your preferences for start, delete, and rebase on branches. An alert will appear when a merge fails as well.
*   The left panel will now display a count and visual identifier for a section when the panel is open.
*   Clear out your search input using the <kbd>ESC</kbd> shortcut.

<h3>Fixed</h3>

*   Rebasing… Rebasing… Initiating a rebase when there's an active stash should no longer hang due to file changes.
*   We've clarified some labels on **Gitflow** along with a few quick additional fixes.
*   Any prompt overlay (like with Gitflow!) will automatically close when the left panel is expanded from minified view.
*   Search no longer overlaps in narrow windows!
*   *nix users: We'll notify you when _inotify_ limit is hit which can cause the client to crash.
*   Lastly, no more…  
    line breaks. We'll handle unicode characters and newlines appropriately in a diff.

***

## 0.5.0

<h3>Thursday, Jan 14, 2016</h3>

**Let the Gitflow through you** 

<h3>New</h3>

*   Setup **Gitflow** in preferences. Initialize a workflow per repository then, in the left panel, quickly initiate and work on _Feature_, _Release_, and _Hotfix_ branches.
*   Fully expanding the right diff panel will now show a new linear, single-column view of commits in something that has been referred to here as a “tiny” graph. Try hovering over the graph to quickly see commit messages while having maximum room for changes!
*   Why fetch from all remotes all of the time? You can now fetch to update refs for individual remotes through the context menu of Remotes in the left panel.
*   *nix users: we'll now let you know when there's an update available!
*   Nothing else new… just kidding! We've made _tons_ of improvements. We'll also notify you of big new features in the app after updating and where to find them!

<h3>Fixed</h3>

*   Selecting _Generate_ for a new key pair in _SSH Config_ on certain platforms will now work as expected and not abruptly crash the app. We don't want any buttons with the crash feature.
*   Speaking of SSH, on *nix you should now be able to push/pull without getting an error saying things are unsupported. It's supported!
*   We'll now tell you an error for _Rebase Failed_ when there's a known conflict on rebasing.
*   Stashing should now display your work in progress stashed after performing the action.
*   We're once again fully retina resolution compatible when soloing… The show/hide eye button transparency or lack-there-of was addressed.
*   Scroll of command! Automatic scrolling to a graph location now works flawlessly when selecting a ref based on where there is existing focus.
*   Longer commit message summaries now won't be slashed at a predefined limit per line. Now your primary message up to 80 characters can go on and on, kind of similar to this line and everyone can see in the grid! Awesome!
*   Also for `feature/ridiculously-long-branch-names`, the context option on the left panel will now be spaced and not overlapped visually!

***

## 0.4.1

<h3>Thursday, Dec 17, 2015</h3>

**So quick!** 

We've introduced all of this list to Git you an improved experience on the Kraken!

<h3>New</h3>

*   Ellipsis interface features! …right on! It should now be more obvious to access the context menu when working with branches in the left panel. It's now more clear and so easy to quickly hover and left-click to initiate whichever command you need…
*   Your `HEAD`, the current branch, should now be more recognizable in the left panel as well.

<h3>Improved</h3>

*   Hiding remotes in the left panel now toggles auto-fetch off, and back on when showing remotes. This is may be impactful to improving your performance if you have a large number of remotes.
*   Diffs will only be updated when you're looking at them! Better checks are in place for when working with the diff panel. We'll only make updates if there are new changes and we'll recognize when they're being viewed.

<h3>Fixed</h3>

*   Fixed support in OAuth / GitHub for `ssh://` protocol format in URLs.
*   We also improved verifying your SSH creds and provide a meaningful error message if unsuccessful.
*   We're once again retina resolution compatible when soloing… The show/hide branch button will remain visible and not overlapped and faded when in Han Solo mode.
*   Discard this, not that! We won't discard all changes anymore when discarding a change on a partially staged file.
*   Feedback styling on our dark theme has been updated for readability. Thanks again, a lot for submissions so far. Keep it coming!

***
## 0.4.0

<h3>Tuesday, Dec 8, 201</h3>

**Stabilizer placed!**

<h3>New</h3>

*   Image diffing, so hot right now… You can now compare two image files through an overlay as it appears from a special hunk. Images display in staging, commits, and conflict panels.

<h3>Improved</h3>

*   Fetch after adding a remote automatically adds associated branches.
*   You may have been looking for it like we were—the master branch is now discoverable after adding a remote fork.
*   Set your upstream branches after creating a local branch! We'll now prompt for your push/pull remote URL and publish.
*   Gone is the issue on Linux with push/pull due to SSL.
*   Updated index for commits from which you should see some big performance improvements on search. This has potential to substantially free up some beloved %CPU we've been borrowing, reducing the jet fan noise coming out of your machine as if it was ready to fly.

We also fixed an issue with perf for our activation process. Thanks to all that are now finally in and have been testing! You should now be able to add your friends without any roadblocks from the invite count.

***
## 0.3.2

<h3>Wednesday, Nov 25, 2015</h3>

**Set to stabilize!** 

<h3>Fixed</h3>

*   It's no longer a problem to switch a remote URL between SSH and HTTPS!
*   Fixed an issue with not being able to resolve conflicts in-app in specific situations like uniquely modifying a file of a change which was deleted on a branch of the attempted merge.
*   Rebase all the things! You'll no longer see empty rebase information.
*   Edit remote is now from the bottom of context menu on right-click. It's a usability thing.
*   Progress bars from the last release have improved not only in size, but color as well.
*   Error messages when present for an appropriate amount of time disappear into the void…

***
## x.x.x

<h3>Beginning of time</h3>

Hey, we don't have any release notes published prior to this!

If you couldn't find what you were looking for, maybe [contact us](https://gitkraken.com/contact)?

Or check out our [frequently asked questions](/faq).
