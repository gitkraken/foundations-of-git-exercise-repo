---

title: Interface Basics
fescription: Learn the basics of working with the interface.

---

GitKraken Client's UI helps make sense of Git. Below we cover the layout and what the icons represent.


***

From left to right, GitKraken Client displays a left reference panel, center graph, and the Commit Panel when working with a repository.

<img src="/img/documentation/getting-started/interface.png" class="img-responsive center">

## Toolbar
In addition to Undo and Redo, the main toolbar houses common repo actions.

<dl class='horizontal'>
    <dt class='img'><img src='/img/documentation/icons/gk-new-undo-icon.svg' class='img-responsive' style="padding: 0.5rem"></dt>
    <dd>
        <h3>Undo</h3>
        <p>Many actions performed in GitKraken Client can be undone. If an action is undoable, the <kbd>Undo</kbd> button will be a solid color ready for action.</p>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-redo-icon.svg' class='img-responsive' style="padding: 0.5rem"></dt>
    <dd>
        <h3>Redo</h3>
        <p>What if you undid something, only to realize that you didn't want to undo it? GitKraken Client also has a </kbd>Redo</kbd> button so you can undo your undos.</p>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-pull-icon.svg' class='img-responsive' style="width: 100px"></dt>
    <dd>
        <h3>Pull</h3>
        <p>Pull changes from your remote repos with this button. See the <kbd><i class='fa fa-caret-down'></i></kbd> button next to the icon? Click that to customize the type of pull you want to perform:</p>
        <ul class='list'>
            <li>Fetch All</li>
            <li>Pull (fast-forward if possible)</li>
            <li>Pull (fast-forward only): equivalent of `git fetch git merge --ff-only` in the CLI</li>
            <li>Pull (rebase): equivalent of `git fetch git rebase` in the CLI</li>
        </ul>
        <div class='callout callout--basic'>
            <p><strong>Tip:</strong> If you find yourself repeatedly performing the same pull actions, set the default pull type by clicking the <span class='sr-only'>circle </span><kbd><i class="far fa-circle"></i></i></kbd> icon to the pull type's left. The default selection will appear as a <span class='sr-only'>green circle </span><kbd><i class="far fa-dot-circle"></i></kbd> icon.</p>
        </div>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-push-icon.svg' class='img-responsive' style="padding: 0.4rem"></dt>
    <dd>
        <h3>Push</h3>
        <p>Push changes to the remote repo as set in your upstream.</p>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-branch-icon.svg' class='img-responsive' style="padding: 0.5rem"></dt>
    <dd>
        <h3>Branch</h3>
        <p>Create a branch on your current local repo.</p>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-stash-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Stash</h3>
        <p>Stash your work-in-process (<code>// WIP</code>) changes.</p>
    </dd>
    <dt class='img'><img src='/img/documentation/icons/gk-new-pop-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Pop Stash</h3>
        <p>Ready to restore your <code>// WIP</code>? Pop that stash and carry on as you were.</p>
    </dd>
     <dt class='img'><img src='/img/documentation/icons/gk-lfs-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>LFS</h3>
        <p> Have large files in your repo? This button will appear when you have <a href="/git-workflows-and-extensions/intro-and-requirements/">LFS</a> enabled on the repository.</p>
    </dd>
         <dt class='img'><img src='/img/documentation/icons/gk-glo-board-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Boards</h3>
        <p>Track your tasks and issues with <a href="/glo/start-glo-ing/">GitKraken Boards</a>.</p>
    </dd>
        <dt class='img'><img src='/img/documentation/icons/gk-timelines-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Timelines</h3>
        <p>Visualize your milestones with <a href="/timelines/overview/">Timelines</a>.</p>
    </dd>
</dl>

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Toggle the toolbar labels by navigating to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> UI Preferences</em> and toggling the <code>Show toolbar icon labels</code> checkbox.</p>
</div>

***

## Left reference panel

Referred to as the left "ref" panel, GitKraken Client shows the properties below specific to your repository.  The panel and each pane can be collapsed or expanded as needed.

<dl class='horizontal'>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-local-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Local</h3>
        <p>References to local branches &mdash; pointers to specific commits allowing work to be separated.</p>
        <p>If you need help with branches, visit our <a href="/working-with-repositories/branching-and-merging">Branching and Merging</a> page.</p>
    </dd>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-remote-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Remote</h3>
        <p>References to remote branches.</p>
        <p>Set sail into <a href="/working-with-repositories/pushing-and-pulling">pushing and pulling remotes</a> for more.</p>
    </dd>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-pull-requests-icon.svg' class='img-responsive' style="padding: 0.3rem"></dt>
    <dd>
        <h3>Pull Requests</h3>
        <p>This shows active requests for merging one branch into another. With the GitHub or Bitbucket integration, new PRs can be created directly from GitKraken Client.</p>
        <p>Create your <a href="/working-with-repositories/pull-requests">Pull Request</a> to get your contribution merged.</p>
    </dd>
    <dt>
        <i class="fa fa-list-ul fa-3x" aria-hidden="true"></i>
    </dt>
    <dd>
        <h3>Issues</h3>
        <p>Lets you see and work with your issues in GitKraken Client</p>
        <p>Hook up to your remote issue tracker of choice - such as <a href="/integrations/jira/">Jira</a>, <a href="/integrations/boards/">Boards</a>, <a href="/integrations/github-issues/">GitHub</a>, <a href="/integrations/gitlab-issues/">GitLab</a>, or <a href="/integrations/trello/">Trello</a>.</p>
    </dd> 
    <dt>
        <i class="fa fa-users fa-3x" aria-hidden="true"></i>
    </dt>
    <dd>
        <h3>Teams</h3>
        <p>Easily see what your <a href="/working-with-repositories/team-view/">Team</a> members are working on.</p>
    </dd>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-tags-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Tags</h3>
        <p>These represent active pointers to commits but never move. <a href="/working-with-repositories/tags">Tag</a>, you're it!</p>
    </dd>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-stash-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Stashes</h3>
        <p>Stored file changes in the working copy.</p>
        <p>For saving your loot to play with later, here's more on <a href="/working-with-commits/stashing">stashes</a>.</p>
    </dd>
    <dt class='img center'><img src='/img/documentation/icons/gk-new-submodules-icon.svg' class='img-responsive'></dt>
    <dd>
        <h3>Submodules</h3>
        <p>A Git repository in a subdirectory of the current repository.</p>
        <p>Git-inception with <a href="/working-with-repositories/submodules">submodules</a> anyone?</p>
    </dd>
</dl>

***

## Commit Panel
The Commit Panel is where files and changes from your working directory are staged and committed.

<img src='/img/documentation/getting-started/commit-panel.png' srcset='/img/documentation/getting-started/commit-panel@2x.png 2x' class='img-bordered img-responsive center'>

The three parts in order of operations on the staging panel are:

1. _Unstaged Files_ &mdash; Watched files in your working directory that have changed since the last commit.
 *  Renamed, deleted, new, or modified files appear here.
2. _Staged Files_ &mdash; Files manually added to the index that are ready to commit.
 * Individual lines, hunks, or all of the changes can be added
3. _Commit Message_ &mdash; recording staged changes to the repository
 * Summary: The brief but meaningful message supporting your commit.  This text will appear in the graph.
 * Description: The extended message to provide more details behind the changes.

 Also, here is a quick color guide for the file symbols:

<img src='/img/documentation/getting-started/symbol-guide.png' srcset='/img/documentation/getting-started/symbol-guide@2x.png 2x' class='img-bordered img-responsive center'>

<div class='callout callout--basic'>
    <p>This panel can also be fixed on the bottom of the client. Just click the <i class="far fa-caret-square-down"></i> icon in the upper right corner of the Commit Panel.</p>
</div>

For deeper waters on staging, dive into [committing work](/working-with-commits/commits).

***
## The Graph
Oooo <span style='color: #0669f7;'>c</span><span style='color: #8e00c2;'>o</span><span style='color: #c517b6;'>l</span><span style='color: #d90171;'>o</span><span style='color: #f25d2e;'>r</span><span style='color: #7bd938;'>s</span>!

<img src='/img/documentation/getting-started/graph.gif' class='figure img-floated img-floated--right'>

The **graph** in GitKraken Client is the core of your repo and a representation of the [Directed Acyclic Graph](https://en.wikipedia.org/wiki/Directed_acyclic_graph) (DAG).  Your commits are displayed here, along with commits from other contributors.

Each row of the graph represents one commit, and the top is always for the latest changes. An interactive _//WIP_ (Work-In-Progress) node will show if the working directory has changed since the last commit.

Branches and tag labels on the left side of the graph are pointers to specific commits, and each vertical column represents a branch currently available on the repository.

Columns can intersect through merge commits as shown in the graph legend. As also shown, multiple branches can be at the same place of a single commit and can be both local and remote.

<img src='/img/documentation/getting-started/graph-elements.png' class='img-bordered img-responsive center'>

For a given vertical track, you can read from bottom to top, and right to left to see how changes are introduced into a focused branch.

***

## Tabs

Quickly switch between multiple repositories.

<img src='/img/documentation/getting-started/tabs.gif' class='figure img-floated img-floated--right'>

You can  add new tabs, drag & drop to rearrange, and remove tabs from the top bar. You can also use the corresponding shortcut keys <kbd>cmd</kbd>+<kbd>1-9</kbd> on Windows/Linux and <kbd>cmd</kbd>+<kbd>1-9</kbd> on mac to quickly switch between repositories.

<div class='callout callout--success'>
    <p><b>Tip:</b> You can <b>open</b> a new tab with the <kbd>+</kbd> icon (shortcut: <kbd>cmd/ctrl</kbd>+<kbd>T</kbd>) and you can <b>close</b> a tab with middle-click (shortcut: <kbd>cmd/ctrl</kbd>+<kbd>W</kbd>)  </a></p>
</div>


Tabs are saved for each profile, so you can have multiple sets of tabs that will open when you switch [profiles](/start-here/profiles/)!

<img src='/img/documentation/getting-started/switchprofilestabs.gif' class='figure img-floated img-floated--right'>

Access a list of all open repositories from the arrow drop-down.

<img src='/img/documentation/getting-started/tab-drop-down.png' class='img-bordered img-responsive center'>

Hover over an open tab to quickly see the end portion of the file path.

<img src='/img/documentation/getting-started/tab-hover.png' class='img-bordered img-responsive center'>

***

## Columns

GitKraken Client will show 3 columns in the header by default: <kbd>Branch/Tag</kbd>, <kbd>Graph</kbd>, and <kbd>Commit Message</kbd>. These 3 columns are static and cannot be rearranged or removed.

<img src='/img/documentation/getting-started/columns.png' srcset='/img/documentation/getting-started/columns@2x.png 2x' class='img-bordered img-responsive center'>

Optionally users may right-click to add <kbd>Commit Author</kbd>, <kbd>Commit Date/Time</kbd>, or <kbd>Sha</kbd>. 

<img src='/img/documentation/getting-started/right-click.png' srcset='/img/documentation/getting-started/right-click@2x.png 2x' class='img-bordered img-responsive center'>

Users may also left-click the <i class="fas fa-cog"></i> icon to enable or disable <kbd>Commit Author</kbd>, <kbd>Commit Date/Time</kbd>, or <kbd>Sha</kbd> (commit ID). 

<img src='/img/documentation/getting-started/gear.png' srcset='/img/documentation/getting-started/gear@2x.png 2x' class='img-bordered img-responsive center'>

In addition to using <kbd>cmd/ctrl</kbd>+<kbd>F</kbd> to search commits, users may also filter by commit author. Click the <i class='fa fa-filter'></i>  icon in the AUTHOR column and you can:

- Select one or more users from the drop-down
- Select one or more teams which will filter by all users in that team
- Search for teams or users in the search field

<img src='/img/documentation/getting-started/filter-author.png' srcset='/img/documentation/getting-started/filter-author@2x.png 2x' class='img-bordered img-responsive center'>

Columns may also be toggled from <em class="context-menu">Preferences  <i class="fa fa-caret-right"></i> UI Customization</em>, GitKraken Client will remember which columns you have selected, column size, and orientation for each repo. 

***

For more details on the interface, like soloing remotes, visit [Hiding and Soloing](/working-with-repositories/hiding-and-soloing).
