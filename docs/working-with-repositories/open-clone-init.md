---

title: Open, Clone, and Init
description: Learn the basics of GitKraken Client, like initializing or cloning projects!

---

Whether you are a newborn or a wizened deep-ocean octopod, each user will need to open, clone, or initialize a repo in GitKraken Client.

***
## Setup
The essential setup process includes:

1. [Installing](/how-to-install) GitKraken Client
2. Creating an account and setting up your [profile](/start-here/profiles)

Once this is complete, you are ready for your oceanic journey!

***
## Projects in GitKraken Client
There are three ways to start a Git repository when working on a project:

1. **Open** - Open a local Git repository already initialized and available locally.
2. **Clone** - Clone a remote Git repository already initialized.
3. **Init** - Create an empty Git repository or reinitialize an existing one.

***

### Opening an existing project
GitKraken Client allows you to load your existing repositories and pick up where you left off. It's also useful for visualizing past work done.  

If you're coming from a Git project you already have locally, navigate to <em class='context-menu'>File <i class="fa fa-caret-right"></i> Open Repo</em> to get started immediately in GitKraken Client.

<img src='/img/documentation/getting-started/project.png' srcset='/img/documentation/getting-started/project@2x.png 2x' class='img-bordered img-responsive center'>

***
### Cloning an existing project
If your project is not on your local machine or you want a new copy, clone the project through <em class='context-menu'>File <i class="fa fa-caret-right"></i> Clone</em>.

<img src='/img/documentation/getting-started/clone.png' srcset='/img/documentation/getting-started/clone@2x.png 2x' class='img-bordered img-responsive center'>

This will then prompt you to open the newly copied project in GitKraken Client.

***
### Initialize a new project
Starting a project in GitKraken Client is easy through <em class='context-menu'>File <i class="fa fa-caret-right"></i> Init</em>

<img src='/img/documentation/getting-started/init.png' srcset='/img/documentation/getting-started/init@2x.png 2x' class='img-bordered img-responsive center'>

All you need to do is fill out the fields and select <button class='button button--success button--ui button--nolink'>Create Repository</span></button> for the magic to begin.

#### Input
* New repository path
* `.gitignore` template (**optional**)
 * Automatically creates a `.gitignore` file in your working copy.

* License (**optional**)
 * On init, GitKraken Client will create a `LICENSE` file in your repository.
 * Check out the [Open Source Initiative](https://opensource.org/licenses) or find out more about [Choosing a License](http://choosealicense.com/).

#### Output
* A new initialized Git project at the specified repository path by creating a `.git` folder.
* The project is opened in GitKraken Client
* An "Initial commit" on a `master` branch containing a blank `README.md` along with a `.gitignore` and `LICENSE.md` if applicable.

 <div class='callout callout--success'>
     <p>GitKraken Client also allows initializing a repository directly to a remote Git hosting provider such as GitHub and Bitbucket.</p>
 </div>


***

### Delete a repository

You may delete a repository by first navigating to the folder icon in the upper left corner of GitKraken Client UI.

<img src='/img/documentation/getting-started/click-folder.png' srcset='/img/documentation/getting-started/click-folder@2x.png 2x' class='img-bordered img-responsive center'>

Then browse through your repo list and right-click on the repository you wish to delete from your local machine. 

<img src='/img/documentation/getting-started/delete-repo.png' srcset='/img/documentation/getting-started/delete-repo@2x.png 2x' class='img-bordered img-responsive center'>

If you are unable to delete the repository, first make sure it is closed in GitKraken Client and then close any other applications which may be working with files in the repository. Restart GitKraken Client and try the delete again.

Deleting the repo from within GitKraken Client will only delete your local copy of the repository. If you wish to delete your remote repository, you will need to perform that action directly by logging into your remote hosting service (GitHub, GitLab, etc).
