---

title: Profiles
description: Create multiple profiles in GitKraken Client to quickly switch between repository preferences. Manage different gitconfig settings, repositories, and more!

---

GitKraken Client uses profiles to store your app preferences, current [Tabs](/start-here/interface/#tabs), and Git config information.

<img src="/img/documentation/getting-started/profiles.png" srcset="/img/documentation/getting-started/profiles@2x.png 2x" class="img-responsive center img-bordered">

<div class='callout callout--success'>
    <p>Create and quickly switch between additional profiles for your different projects and work environments on <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken Pro</a></p>
</div>

***
## Profiles

<img src="/img/documentation/getting-started/profiles-preferences.png" srcset="/img/documentation/getting-started/profiles-preferences@2x.png 2x" class="img-responsive center img-bordered">

The _Keep my .gitconfig updated with my profile info_ option updates your global `.gitconfig` file with the name and email address of your current profile.


### What's saved in each profile?

The _General_, _Integrations_, and _UI Preferences_ settings configured under your <kbd>Preferences</kbd> are profile-specific.  

[Tabs](/start-here/interface/#tabs) are unique to each profile. When creating a new profile, GitKraken Client will use the same tabs that are open in your current profile.

<img src="/img/documentation/getting-started/switchprofilestabs.gif"  class="img-responsive center img-bordered">

Integrations are unique to each profile. If you need to connect to a second remote hosting account, create a second profile and connect the other account from the <kbd>Integrations</kbd> tab. You can do this for any of the integrations.

<img src="/img/documentation/getting-started/profile-example.png" srcset="/img/documentation/getting-started/profile-example@2x.png 2x" class="img-responsive center img-bordered">

### Changing Avatars
Your commit avatar is either a generated identicon, or the active [Gravatar](https://gravatar.com) image linked to your <code>.gitconfig</code> email address. If you change your Gravatar, your GitKraken Client avatar will update itself.

To change the image, click the profile icon in the top right corner then <kbd>Manage Profiles <i class='fa fa-caret-right'></i> <i class="fa fa-ellipsis-v" aria-hidden="true"></i></kbd>.

<img src="/img/documentation/getting-started/edit-profile.png" srcset="/img/documentation/getting-started/edit-profile.png" class="img-responsive center img-bordered">

<img src="/img/documentation/getting-started/edit-profile-2.png" srcset="/img/documentation/getting-started/edit-profile-2@2x.png 2x" class="img-responsive center img-bordered">

You can choose from the list of icons available on the left then click <button class='button button--success button--ui button--nolink'>Save changes</span></button>. Alternatively, you can set a different email address for this profile if the email address has a different Gravatar image associated to it.

<img src="/img/documentation/getting-started/gravatar.png" srcset="/img/documentation/getting-started/gravatar.png" class="img-responsive center img-bordered">

### Author initials in graph

GitKraken Client lets you replace all commit nodes with the commit author's initials. 

<img src="/img/documentation/getting-started/author-initials.png" srcset="/img/documentation/getting-started/author-initials@2x.png 2x" class="img-responsive center img-bordered">

Navigate to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> UI Preferences</em> to enable the setting.

#### What initials does GitKraken Client use?

If you are just enabling this UI setting, GitKraken Client will reference the original name associated with the commit.

If a commit was made in GitKraken Client, the app will list initials from the GitKraken user profile. If a commit was made in the CLI, the app will list initials from the user's `.git/config` or global `.gitconfig`.


### Do profiles allow different identity pictures?</p>

As long you have different email addresses with the profiles associated with Gravatar images, then yes! GitKraken Client at this time does not allow selection of custom images.

