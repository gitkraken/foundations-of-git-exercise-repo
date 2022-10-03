---

title: Activity Logs 
description: Learn where to find feedback Activity Logs in GitKraken Client.

---

Learn how to view all Git actions made to repositories and all application actions made in GitKraken Client through Activity Logs.

***

## Activity Logs 

Looking to increase your project scope?

Pop open the hood of your project and check out the <kbd>Activity Logs</kbd> located in the footer toolbar of GitKraken Client.

<kbd>Activity Logs</kbd> provide real time feedback of application and repository-level interactions that occured in GitKraken Client.

<img src='/img/documentation/repositories/activity.gif' class='img-bordered img-responsive center'>

<kbd>Activity Logs</kbd> files are plain text in a standard log file format. Each line displays time of action, action feedback, and performance data measured in milliseconds.

<img src='/img/documentation/repositories/data-line.png' srcset='/img/documentation/repositories/data-line@2x.png 2x' class='img-bordered img-responsive center'>

<kbd>Activity Logs</kbd> collate Git actions, outputs information chronologically, and displays activity history indefinitely.

### Application Log

The *Applications* tab in <kbd>Activity Logs</kbd> contains messages about actions made in GitKraken Client application. Discover events from your GitKraken Client instance such as: project creation, clearing SSH, setting global gitconfig, etc.

<img src='/img/documentation/repositories/app-level.png' srcset='/img/documentation/repositories/app-level@2x.png 2x' class='img-bordered img-responsive center'>

This tab information remains consistent regardless of the repository currently in focus: switching repositories will not alter the Application system log files. 

### Repository Log 

The *Repository* tab in <kbd>Activity Logs</kbd> contains logged messages of Git operations taken while working with your repository. 

Refer to your *Repository* log to increase your project scope as a greater source of truth of your Git activity such as: fetch, push, merge, etc.

<img src='/img/documentation/repositories/repository-level.png' srcset='/img/documentation/repositories/repository-level@2x.png 2x' class='img-bordered img-responsive center'>

*Repository* activity reflects action taken in the repository currently open in focus. 

<div class='callout callout--warning'>
    <p><strong>Note:</strong> 
    For more verbose logging, navigate to <em>Preferences > General > Use extended logging in activity log</em>.
 </p>
</div>

Enabling extended logging provides even greater scope into repository-level Git actions, including Auto-fetch feedback. 

<img src='/img/documentation/repositories/extended.png' srcset='/img/documentation/repositories/extended@2x.png 2x' class='img-bordered img-responsive center'>

### Git Hook Log

Do you automate your workflow with <a href= "/working-with-repositories/githooks/"> Git hooks</a>? 

<kbd>Activity Logs</kbd> log all hook activity - successes, warnings, failures, errors, etc.

The *Repository* tab populates a new tab in <kbd>Activity Logs</kbd> to provide active insight on feedback of your Git hook activity. View your error log in context to find how an event caused the change for faster troubleshooting. 

<img src='/img/documentation/repositories/githook-log.gif' class='img-bordered img-responsive center'>

You can also access a hook log from the snackbox notification that populates near the footer toolbar when an error is thrown.

<img src='/img/documentation/repositories/snackbox-error.png' srcset='/img/documentation/repositories/snackbox-error@2x.png 2x' class='img-bordered img-responsive center'>

