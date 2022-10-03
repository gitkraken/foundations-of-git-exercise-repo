---

title: Diff, Blame, and History 
description: Compare your changes with diffs in GitKraken Client. Learn about where to access diffs, file blame, and more.

---


Compare changes within GitKraken Client _diffs_. Learn where to access _diffs_, and how to access _file history_ or _file blame_.

***

<a id="what-is-a-diff-in-gitkraken"></a>

## What is a diff in GitKraken Client?

A diff shows what was added or removed from a file. <span style='color: #d90171;'>Red</span> is for lines where content was removed whereas <span style='color: #7bd938;'>green</span> is for new lines added.

<img src='/img/documentation/working-with-files/diff/diff-1.png' srcset='/img/documentation/working-with-files/diff/diff-1@2x.png 2x' class='img-bordered img-responsive center' />

GitKraken Client's diff comes included with the following:

- Word diffing
- Syntax highlighting
- File mini-map
- Toggles between Hunk View, Inline View, and Split View
- Arrows to move between change sets

Most importantly, the <button class="button button--primary button--ui button--nolink"><span style="color:#141422;">Edit in working directory</span></button> button allows you to edit this file directly. Learn more about this feature in [Editing Files](/working-with-files/editing-files) section.

***
## Where can I access the diff?

Access the diff of a file from:

* **Staging**: Click on a file
* **Commit node**: With a commit node selected, click on any file

If you have two commits selected, GitKraken Client shows the difference between the two commits.

<img src='/img/documentation/working-with-files/diff/two-diffs.png' srcset='/img/documentation/working-with-files/diff/two-diffs@2x.png 2x' class='img-bordered img-responsive center'>

Additionally, select multiple commit rows in the graph using <kbd>Shift</kbd> <kbd>Click</kbd> to show its merged diff:

<img src='/img/documentation/working-with-files/diff/merged-diff.png' srcset='/img/documentation/working-with-files/diff/merged-diff@2x.png 2x' class='img-bordered img-responsive center'>

### Hunk view

Hunk view will show the diff as blocks, without the context of the rest of the file.

<img src='/img/documentation/working-with-files/diff/hunk.png' srcset='/img/documentation/working-with-files/diff/hunk@2x.png 2x' class='img-bordered img-responsive center' />

### Inline view

Inline view will show the diff within the context of the entire file.

<img src='/img/documentation/working-with-files/diff/inline.png' srcset='/img/documentation/working-with-files/diff/inline@2x.png 2x' class='img-bordered img-responsive center' />

### Split view

Split view will show a side by side diff comparing how the file looked before (left), and how it looks after the change (right). Note, you may select deleted lines with your mouse from split view. 

<img src='/img/documentation/working-with-files/diff/split.png' srcset='/img/documentation/working-with-files/diff/split@2x.png 2x' class='img-bordered img-responsive center' />

***

## External diff tools
Configure your preferred external diff tool from <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> General</em>:

<img src="/img/documentation/working-with-files/diff/externaldiff.png" srcset="/img/documentation/working-with-files/diff/externaldiff@2x.png" class="img-bordered img-responsive center">

GitKraken Client currently _only supports_ the following diff tools:

- Beyond Compare
- FileMerge
- Kaleidoscope
- KDiff
- Araxis
- P4Merge

If your diff tool from the list above is installed and is not showing up in the dropdown, then look for an option to install command line tools.

<img src='/img/documentation/working-with-files/diff/beyond-compare.png' srcset='/img/documentation/working-with-files/diff/beyond-compare@2x.png 2x' class='img-bordered img-responsive center' />

If you would like to use another diff tool, navigate to <em class="context-menu">Preferences <i class="fa fa-caret-right"></i> General</em> and set the <kbd>Diff Tool</kbd> to _Git Config Default_. Then open your global `.gitconfig` file and add these additional lines to use that diff tool. Here are some examples for each operating system:

#### Mac OS
```
[diff]
    tool = meld
[difftool "meld"]
    cmd = open -a Meld --args \"$LOCAL\" \"$REMOTE\"
```

#### Linux
```
[diff]
  tool = meld
[difftool "meld"]
  cmd = meld \"$LOCAL\" \"$REMOTE\"
```

#### Windows
```
[diff]
  tool = meld
[difftool "meld"]
  cmd = \"C:\\Program Files\\Meld\\Meld.exe\" "$LOCAL" "$REMOTE"
```

***
## Diff multiple commits

Use the <kbd>Shift</kbd> or <kbd>Cmd/Ctrl</kbd> key to select multiple commits in the graph.

<img src="/img/documentation/working-with-files/diff/select-commits.gif" srcset="/img/documentation/working-with-files/diff/select-commits.gif" class="img-bordered img-responsive center">

This will produced a combined diff, which lists all files that were added, modified, renamed or deleted between the selected commits in the Commit Panel.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Are you looking to diff branches? Consider using the <kbd>Cmd/Ctrl</kbd> key to select the head commits of each branch.</p>
</div>

***
## File Blame and History

_File History_ and _File Blame_ information display in the same view.

To access either option, click to view the file diff and the options will appear in the upper right.

<img src='/img/documentation/working-with-files/diff/access-blame.png' srcset='/img/documentation/working-with-files/diff/access-blame@2x.png 2x' class='img-bordered img-responsive center'>

You may also click on a commit in the graph and then right click a file to access _File History_ or _File Blame_. _File History_ shows that file's commit history on the left.

<img src='/img/documentation/working-with-files/diff/file-history.png' srcset='/img/documentation/working-with-files/diff/file-history@2x.png 2x' class='img-bordered img-responsive center'>

_File Blame_ will color code the commit author of each line or hunk.

<img src='/img/documentation/working-with-files/diff/blame.png' srcset='/img/documentation/working-with-files/diff/blame@2x.png 2x' class='img-bordered img-responsive center'>

Use the top toggle button to switch between <kbd>Diff View</kbd>, which shows the selected commit's changes to the file, and the <kbd>File View</kbd>, which shows the file's state at that commit, including the blame info.
