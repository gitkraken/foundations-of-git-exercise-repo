---

title: Filter Syntax
description: Learn about pull request filter syntax in GitKraken Client.

---

You can create filters using the below syntax to pull requests shown.

***

## GitHub

### Parameters Available

|Filter             |Example                        |Description                                                                                            |
|:------------------|:------------------------------|:------------------------------------------------------------------------------------------------------|
|Title/body search  |`foo`                          |Will match pull requests containing the string `foo` in their title and description.                   |
|Title/body search  |`foo bar`                      |Will match the pull requests containing the string `foo bar` in their title and description.           |
|in:                |`foo in:title`                 |Will match the pull requests containing the string `foo` in only their title.                          |
|in:                |`foo in:body`                  |Will match the pull requests containing the string `foo` in only their description.                    |
|author:            |`author:keanu`                 |Will match pull requests created by the user `keanu`.                                                  |
|assignee:          |`assignee:keanu`               |Will match pull requests assigned to the user `keanu`.                                                 |
|review-requested:  |`review-requested:jerry`       |Will match pull requests that need to be reviewed by the user `jerry`.                                 |
|reviewed-by:       |`reviewed-by:keanu`            |Will match pull requests that have been reviewed by the user `keanu`.                                  |
|involves:          |`involves:jerry`               |Will match pull requests that the user `jerry` has reviewed, has been assigned to, or has commented on.|
|base:              |`base:main`                    |Will match pull requests that are merging into `main`.                                                 |
|head:              |`head:development`             |Will match pull requests that are merging from `development`.                                          |
|draft:             |`draft:true`                   |Will match pull requests that are marked as a draft.                                                   |
|label:             |`label:"Release Critical"`     |Will match pull requests that have the `Release Critical` label.                                       |
|milestone:         |`milestone:v1`                 |Will match pull requests that have the `v1` milestone.                                                 |

### Review State
The review filter can take multiple parameters, which are `approved`, `changes_requested`, or `none`.

|Filter             |Example                        |Description                                                                                            |
|:------------------|:------------------------------|:------------------------------------------------------------------------------------------------------|
|review:            |`review:approved`              |Will match pull requests that have been approved by at least one person.                               |
|review:            |`review:changes_requested`     |Will match pull requests that have at least one person requesting changes.                             |
|review:            |`review:none`                  |Will match pull requests that no reviews.                                                              |

### Status
The status filter can take multiple parameters, which are `success`, `pending`, or `failure`.

|Filter             |Example                        |Description                                                                                            |
|:------------------|:------------------------------|:------------------------------------------------------------------------------------------------------|
|status:            |`status:success`               |Will match pull requests with a success status.                                                        |
|status:            |`status:pending`               |Will match pull requests with a pending status.                                                        |
|status:            |`status:failure`               |Will match pull requests with a failed status.                                                         |

### No Value
The no value filter will include pull requests if the specified parameter does not exist on a pull request. The parameters available are `assignee`, `involves`, `label`, `milestone`, `review-requested`, and `status`.

|Filter             |Example                        |Description                                                                                            |
|:------------------|:------------------------------|:------------------------------------------------------------------------------------------------------|
|no:                |`no:assignee`                  |Will match pull requests that have no assignees.                                                       |
|no:                |`no:status`                    |Will match pull requests that have no status.                                                          |

### Dates
Date fields on a pull request can be tested in various forms using the `created` and `updated` filters.

|Filter             |Example                        |Description                                                                                            |
|:------------------|:------------------------------|:------------------------------------------------------------------------------------------------------|
|created:           |`created:2019-12-14T19:20:16Z` |Will match pull requests created after 2019-12-14T19:20:16Z.                                           |
|updated:           |`updated:2019-12-14T19:20:16Z` |Will match pull requests updated after 2019-12-14T19:20:16Z.                                           |
|created:           |`created:2020-12-31`           |The filter will also attempt to support the user's local format.                                       |

### OR Conditions
All filters support OR conditions if provided with comma separated values.

|Example                            |Description                                                                                            |
|:----------------------------------|:------------------------------------------------------------------------------------------------------|
|label:Bug,Feature                  |Will match pull requests that have either the label `Bug` or `Feature`.                                |
|assignee:jerry,keanu               |Will match pull requests that are assigned to either `jerry` or `keanu`.                               |
|label:Bug,Feature label:Important  |Will match pull requests that have either the label `Bug` or `Feature`, and have the label `Important`.|

### Excluding Results
Adding a `-` to the front of any of the above will cause pull requests matching that query to be excluded from results.

|Example&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Description                                                                                    |
|:----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
|-no:assignee                       |Will match pull requests that _have_ an assignee.                                                                                                      |
|-assignee:guy                      |Will match pull requests that _are not_ assigned to the user `guy`.                                                                                    |
|-label:Bug,Next                    |Will match pull requests that _do not_ have _either_ the `Bug` or `Next` label. This is effectively the same as using `-label:Bug -label:Feature`.     |

### Combining Parameters
All of the above can be used in any combination. Pull requests will be matched if they meet _all_ of the parameters in the query.

+ `foo bar label:feature -has:assignee`

***

## Other Integrations

We do not support all filters on other integrations, including GitLab, Bitbucket, and Azure DevOps.

|Integration          |updated:|review-requested:|assignee:|title/body search, in:, no:, created:, base:, head:|reviewed-by:, review:, involves:, label:, milestone:, draft:, status:|
|---------------------|:------:|:---------------:|:-------:|:-------------------------------------------------:|:-------------------------------------------------------------------:|
|GitLab + Self Managed|✔       |                 |✔        |✔                                                  |                                                                     |
|Bitbucket            |✔       |                 |✔        |✔                                                  |                                                                     |
|Bitbucket Server     |✔       |✔                |         |✔                                                  |                                                                     |
|Azure DevOps         |        |                 |✔        |✔                                                  |                                                                     |