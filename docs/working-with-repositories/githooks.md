---

title: Git hooks
description: Compare your changes with diffs in GitKraken Client. Learn about where to access diffs, file blame, and more.

---

Git hooks are shell scripts that execute after an event such as a commit or push.

In the following video, we will take you through the basics of what a Git hook is and demonstrate how to use one in GitKraken Client.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZZgyILr-TjA?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>


***

## Where are Git hooks?

Hooks are stored in the `hooks` subdirectory of the `.git` directory. This folder is automatically created when you initialize a new repository in GitKraken Client and is located in `.git\hooks` in your project directory.

Hooks are unique to your local repository and will not be copied over if you create a new repository. Feel free to add, change, or remove scripts from this folder as necessary.

<img src='/img/documentation/repositories/githooks/hook_location.png' srcset='/img/documentation/repositories/githooks/hook_location@2x.png 2x' class='img-responsive center img-bordered' />

If running OSX or Linux, GitKraken Client will seamlessly detect any Git hooks in your repository if your scripts are set to be executable. If you forgot to set your files to executables, GitKraken Client will throw an error as a heads up.

And if running Windows, GitKraken Client will detect your Git hooks automatically.

***

## Define a custom hook path  

Users can define a custom path for git hooks by going to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Git Hooks</em>. <button class="button button--primary button--ui button--nolink">Browse</button> to the location or enter the path to your git hook folder.

This custom git hook path is defined on a per-repository basis. 

<img src='/img/documentation/repositories/githooks/hook_preferences.png' srcset='/img/documentation/repositories/githooks/hook_preferences@2x.png 2x' class='img-responsive center img-bordered' />

***

## What hooks are supported by GitKraken Client?

Here are the hooks supported by GitKraken Client. Where appropriate, beneath each hook are the actions during which GitKraken Client calls that hook:

<table class='table table--bordered table--shortcuts'>
  <tbody>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-commit</code></h3> </td>
          <td style="width: 65%;">
            - Commit
            <br>
            - Amend
            <br>
            - Merge Resolve
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3><code>prepare-commit-msg</code></h3> </td>
          <td style="width: 65%;">
            - Commit
            <br>
            - Amend
            <br>
            - Cherrypick
            <br>
            - Merge
            <br>
            - Squash
            <br>
            - Revert
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>commit-msg</code></h3> </td>
          <td style="width: 65%;">
          - Commit
          <br>
          - Amend
          <br>
          - Merge Resolve
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-commit</code></h3> </td>
          <td style="width: 65%;">
          - Commit
          <br>
          - Amend
          <br>
          - Cherrypick
          <br>
          - Merge Resolve
          <br>
          - Revert
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-rebase</code></h3> </td>
          <td style="width: 65%;">
          - Rebase
          <br>
          - Squash
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-checkout</code></h3> </td>
          <td style="width: 65%;">
          - Checkout
          <br>
          - Discard Changes (selectively)
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-merge</code></h3> </td>
          <td style="width: 65%;">
          - Merge (Without Conflicts)
          <br>
          - Fast-Forward
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-rewrite</code></h3> </td>
          <td style="width: 65%;">
          - Amend
          <br>
          - Squash
          <br>
          - Rebase
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-push</code></h3> </td>
          <td style="width: 65%;">
          - Push Branch
          <br>
          - Push Tag
          <br>
          - Delete Remote Branch
          <br>
          - Delete Remote Tag
          </td>
      </tr>
  </tbody>
</table>
