---

title: Tips
description: Find out all the things users should know to boost their GitKraken Client experience.

---

Here's the TLDR of the best features in GitKraken Client.

***

### 1. Set up Profiles

If you have personal projects you wish to separate from work repos–or if you need to connect to multiple instances of GitHub, GitLab, Bitbucket, etc.–then set up [Profiles](/start-here/profiles).

<img src="/img/documentation/getting-started/profile-example.png" srcset="/img/documentation/getting-started/profile-example@2x.png 2x" class="img-responsive center img-bordered">

Each profile stores different app preferences and Git config information, which makes it easier to switch context.

<div class='callout callout--success'>
    <p>Multiple Profiles is a <a href="https://www.gitkraken.com/git-client" target="_blank">GitKraken Pro</a> only feature.</p>
</div>

***

### 2. Use the Command Palette

Work like the pros, and use the [Command Palette](/start-here/command-palette) to quickly access GitKraken Client actions.

<img src="/img/documentation/tips/advanced-interface/FFcommands.gif" srcset="/img/documentation/tips/advanced-interface/FFcommands.gif" class="img-responsive center img-bordered">

As you type, the Command Palette will find the most relevant commands, allowing you to perform many actions without clicking. Here are a few examples:

<h3>Core:</h3>

 * `Redo`
 * `Undo`

<h3>File:</h3>

* `Create File` + `filename`
* `Delete File` + `filename`
* `Open File` + `filename`
* `View File` + `filename`
* `Edit File` + `filename`
* `Discard all changes`
* `Stage all changes`
* `Unstage all changes`



***

### 3. Keyboard Shortcuts

For fast fingers, check out our [keyboard shortcuts](/start-here/keyboard-shortcuts). These will help you blitz through the app.

<table class='table table--bordered table--shortcuts'>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Open keyboard shortcuts</td>
            <td><kbd>&#8984;</kbd><kbd>/</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>/</kbd></td>
        </tr>
    </tbody>
</table>

***

### 4. Create, Open and Edit Files in the Built-In Code Editor

To create a file directly in GitKraken Client, use the keyboard shortcut  <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd> to open the Command Palette, type `Create File`, and then type the name of your file before hitting <kbd>Enter</kbd>.

The code editor will automatically open so you can jump right in and start working on your project. 

<img src='/img/documentation/working-with-files/adding-and-removing/Editor-gif.gif' class='img-bordered img-responsive center'>

You can also right click the empty space in the Commit Panel and click the `Create File` context menu option.

To open an existing file to the built-in code editor, select a branch and navigate to the file you'd like to edit in the Commit Panel.

Double click the file to bring it to File View. From File View, you can click to edit a file and make changes directly. You'll notice syntax highlighting, code hinting, a file minimap, and the ability to search your file.

<img src='/img/documentation/working-with-files/adding-and-removing/Updated-editor.gif' class='img-bordered img-responsive center'>

Learn more about [editing files](/working-with-files/editing-files) in GitKraken Client.

To delete a file, right-click on the file from the Commit Panel to access the delete option. 


***

### 5. Favorite Repos

Favorite the repos you work on most so they show up at the top of your list.

<img src="/img/documentation/working-with-files/favorites/list.png" srcset="/img/documentation/working-with-files/favorites/list.png" class="img-bordered img-responsive center">

You can favorite a repository by right-cliking a recently opened repository in the drop down list, or you can click the heart from the repository management window.

<img src="/img/documentation/working-with-files/favorites/star-repos.png" srcset="/img/documentation/working-with-files/favorites/star-repos@2x.png" class="img-bordered img-responsive center">

***

### 6. Integrate with GitHub, GitLab, Bitbucket, and Azure DevOps

GitKraken Client allows you to authenticate with GitHub, GitLab, Bitbucket, and Azure DevOps (previously VSTS), which will help you find repos when cloning or adding your remotes.

<img src="/img/documentation/integrations/vsts/authentication.png" srcset="/img/documentation/integrations/vsts/authentication@2x.png" class="img-bordered img-responsive center">

### Benefits

- Create repositories on GitHub/GitLab/Bitbucket/Azure DevOps including .gitignore and license
- Save authentication into profiles
- Clone from remote repo list
- Add remotes 
- Create and view pull requests

***

### 7. Build Status, Assignees, and Reviewers in PRs

If you are using the GitLab or GitHub integration, you may also add a pull request assignee and label(s) to your pull request. GitKraken Client will then pass these values onto GitLab or GitHub when the pull request is created. 

<img src='/img/documentation/repositories/gitlab-assignee.png' srcset='/img/documentation/repositories/gitlab-assignee@2x.png' class='img-bordered img-responsive center'>

If you are using the GitHub integration, you may also add reviewers and multiple assignees to a pull request. 

<img src='/img/documentation/repositories/github-assignee.png' srcset='/img/documentation/repositories/github-assignee@2x.png' class='img-bordered img-responsive center'>

Additionally for GitHub pull requests, this tooltip will show assignees, labels, reviewers, and build status.

<img src='/img/documentation/repositories/tooltip-github.png' srcset='/img/documentation/repositories/tooltip-github@2x.png' class='img-bordered img-responsive center'>

Learn more about [pull requests](/working-with-repositories/pull-requests).

***

### 8. File History and File Blame

File History and File Blame information display in the same view.

To access either option, first click on a commit in the graph. Then right click a file to access File History or File Blame.

<img src='/img/documentation/working-with-files/diff/file-history.png' srcset='/img/documentation/working-with-files/diff/file-history@2x.png 2x' class='img-bordered img-responsive center'>

File History shows that file's commit history on the left.

<img src='/img/documentation/working-with-files/diff/file-diff.png' srcset='/img/documentation/working-with-files/diff/file-diff.png 2x' class='img-bordered img-responsive center'>

Use the top toggle button to switch between Diff View, which shows the selected commit's changes to the file, and the File View, which shows the file's state at that commit, including the blame info.

***

### 9. Open Terminal 

You can open the terminal or CLI from GitKraken Client!

To open the current repo folder in terminal, go to <em class="context-menu">File <i class='fa fa-caret-right'></i> Open Terminal</em> or use the keyboard shortcuts <kbd>opt</kbd> + <kbd>T</kbd> (Mac) / <kbd>alt</kbd> + <kbd>T</kbd> (Windows + Linux). 

You can set your default terminal from <em class="context-menu">Preferences <i class='fa fa-caret-right'></i> General</em>.

***

### 10. Resize the Graph

It's simple, but easy to miss. Hover over any of the colored lines to drag and drop the graph.

<img src='/img/documentation/getting-started/graph.gif' class='figure img-floated img-floated--right'>


Resize and marvel at the colors of the rainbow.



