---

title: Tags
description: Designating important points of the Git history. Creating Tags in GitKraken Client on commits is easy with the graph.

---

Tags <em class='context-menu'><img style='translate:rotate(180deg);height:1em;' src='/img/documentation/icons/gk-tag-icon.svg'></em> are pointers to a commit.  Some examples of these are for marking versions of your product or important changes.

***
### Adding tags

To create a new tag in GitKraken Client, right click on the commit you'd like to tag, and select <kbd>Create tag here</kbd> at the bottom.  

<img src="/img/documentation/repositories/tags/add-tag.png" srcset="/img/documentation/repositories/tags/add-tag.png" class="img-bordered img-responsive center">


Tags are created locally, but available for remotes by right clicking the tag and selecting to push the tag to the remote.

<img src="/img/documentation/repositories/tags/tag-remote.png" srcset="/img/documentation/repositories/tags/tag-remote.png" class="img-bordered img-responsive center">

Double click a tag in the left panel to jump to when the tag was added.  Tags can also be hidden and soloed just like branches from the right click menu.

<img src="/img/documentation/repositories/tags/tag-right.png" srcset="/img/documentation/repositories/tags/tag-right.png" class="img-bordered img-responsive center">

***

### Checkout a tag

While you cannot directly checkout a tag, right-click on a tag and choose the <kbd>Create branch here</kbd> to create and then immediately checkout the commit tied with the tag.

<img src="/img/documentation/repositories/tags/tag-branch.png" srcset="/img/documentation/repositories/tags/tag-branch@2x.png" class="img-bordered img-responsive center">

Alternatively, consider using the [detached HEAD state](/working-with-commits/detached-head-state/) to checkout the commit directly.

***

### Moving tags
To move a tag to the branch HEAD, checkout the new branch, right click the tag, and select fast-forward.  

If a tag cannot be fast-forwarded, you can delete and then add a new one.  Be sure to delete the tag on remote as well.

***

### Tag messages
Create annotated tags by right clicking a branch or commit and selecting <kbd>Create annotated tag here</kbd>. You can annotate an existing tag by right clicking the tag and selecting <kbd>Annotate tag</kbd>. This message will be displayed when hovering over the tag in the left panel, or in the graph.

<img src="/img/documentation/repositories/tags/tag-annotation.png" srcset="/img/documentation/repositories/tags/tag-annotation.png" class="img-bordered img-responsive center">

### Search or filter tags

You may filter tags from the filter bar in the left panel. Use this to quickly find a tag.

<img src="/img/documentation/repositories/tags/filter-tags.png" srcset="/img/documentation/repositories/tags/filter-tags@2x.png" class="img-bordered img-responsive center">