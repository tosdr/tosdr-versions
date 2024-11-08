New: nightly.link [now accepts donations!](#pricing)

nightly.link ![](logo.svg) for GitHub [![](https://img.shields.io/github/stars/oprypin/nightly.link?style=social)](https://github.com/oprypin/nightly.link)
===========================================================================================================================================================

This service lets you get a shareable link to download a [build artifact](https://docs.github.com/en/actions/guides/storing-workflow-data-as-artifacts#uploading-build-and-test-artifacts) from the latest successful [GitHub Actions](https://docs.github.com/en/actions/guides/about-continuous-integration#about-continuous-integration-using-github-actions) build of a repository.

Any public repository is accessible by default and **visitors don't need to log in**.

If you'll be publishing a link to your own repository's artifacts, please install [the GitHub App](https://github.com/apps/nightly-link) anyway, so that downloads for your repositories don't share the global API rate limit. The throttling will likely become very bad over time.

 (optional, other than for private repos; feel free to [revoke](https://github.com/settings/apps/authorizations) this anytime)

Paste a GitHub link, get a nightly.link!
----------------------------------------

 

Check out the following sections to see what you can do with this.

Link to a repository's latest artifact

Insert the GitHub URL of a workflow file that uses [actions/upload-artifact](https://github.com/actions/upload-artifact#readme).  
Example: [https://github.com/quassel/quassel/blob/master/.github/workflows/main.yml](https://github.com/quassel/quassel/blob/master/.github/workflows/main.yml)  
Note that the _branch_ which you're on also matters.

Following this form (and having selected the "Windows" artifact), you will end up at  
[https://nightly.link/quassel/quassel/workflows/main/master/Windows](https://nightly.link/quassel/quassel/workflows/main/master/Windows) \[[.zip](https://nightly.link/quassel/quassel/workflows/main/master/Windows.zip)\]  
which is a link that always downloads the latest artifact from a succeeding run on that repo+workflow+branch.

To allow any completed workflow runs, not only successful ones, append `?status=completed` to the URL.

If you have several workflows or branches, you can adapt the URL by hand in a predictable way.

Link to a particular artifact

If GitHub gave you a link such as [https://github.com/quassel/quassel/suites/27171785749/artifacts/1811635631](https://github.com/quassel/quassel/suites/27171785749/artifacts/1811635631),  
you can just change the prefix to [https://nightly.link/quassel/quassel/suites/27171785749/artifacts/1811635631](https://nightly.link/quassel/quassel/suites/27171785749/artifacts/1811635631),  
and you get a download URL that works the same but doesn't give a "404" error to users who aren't logged into GitHub.

Or, paste it into the field above.

Extra links for a particular run

A _run_ is basically a collection of _jobs_. Even though it's the job that produces artifacts, they get associated with the parent run.

Example run: [https://github.com/quassel/quassel/actions/runs/10388804461](https://github.com/quassel/quassel/actions/runs/10388804461).  
You _have to_ provide the _run_ to nightly.link if you want to find the artifacts.  
Again, you can just change the prefix like [https://nightly.link/quassel/quassel/actions/runs/10388804461](https://nightly.link/quassel/quassel/actions/runs/10388804461) to get there.  

If, instead, you click into a _job_, you can access its logs.  
Example job: [https://github.com/oprypin/nightly.link/runs/1849327325?check\_suite\_focus=true](https://github.com/oprypin/nightly.link/runs/1849327325?check_suite_focus=true)  
The raw log download link is in the same situation as artifacts: nightly.link is needed to make them work for anonymous users. It accepts both the job's URL itself, and the link that you can get from the "View raw logs" item.

Bot that comments on pull requests

For projects developing an application, it is useful to quickly try out the executable built from the code of an incoming [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests). You can do this normally by clicking into a finished GitHub Actions job, then into its parent run, then scrolling down to the list of artifacts.

Instead, you can opt into a much more convenient approach: add a "bot" that replies with links directly to the artifacts, as soon as the pull request finishes building.

[Here's how it looks](https://github.com/oprypin/nightly.link/pull/10). Apply it to your repository by copying [the sample workflow file](https://github.com/oprypin/nightly.link/blob/master/.github/workflows/pr-comment.yml). Note that it must be added to the main branch and be fully submitted/merged before it will do anything.

Another advantage that this gives is that users that aren't logged into GitHub can download the artifacts as well. If you don't care about that, you can adapt the sample workflow to link directly to github.com, without relying on this site.

Note that this ability is not actually part of nightly.link, just a creative way to apply it; the "bot" is executed entirely within GitHub Actions, isolated to your repository.

The issue
---------

GitHub has no direct way to directly link to the _latest_ build from GitHub actions of a given repository.

Even if you _do_ have a link to an artifact, using it requires the visitor to be logged into the GitHub website.

The discussion originates at [actions/upload-artifact "Artifact download URL only work for registered users"](https://github.com/actions/upload-artifact/issues/51).

So, this service is a solution to this omission.

Authorization
-------------

Because GitHub doesn't provide any permanent and public links to an artifact, this service redirects to time-limited links that GitHub can give to the application -- only on behalf of an authenticated user that has access to the repository. So, whenever someone downloads an artifact from a repository that you had added, this service uses a token that is associated with your installation of the GitHub App.

### [nightly.link](https://github.com/apps/nightly-link) as an [Installed GitHub App](https://github.com/settings/installations)

This GitHub App requests these permissions:

> * **Actions**: Workflows, workflow runs and artifacts.
>     * Access: **Read-only**
> * **Metadata** \[mandatory\]: Search repositories, list collaborators, and access repository metadata.
>     * Access: **Read-only**

### [nightly.link](https://github.com/apps/nightly-link) as an [Authorized GitHub App](https://github.com/settings/apps/authorizations)

Interestingly, the prompt that GitHub presents to you when authenticating to the service says something quite a bit scarier:

> **nightly.link by [Oleh Prypin](https://github.com/oprypin) would like permission to:**
> 
> * Verify your GitHub identity (_$username_)
> * Know which resources you can access
> * Act on your behalf

In reality, this blurb is _completely generic_ and will be shown for any GitHub App authorization regardless of its permissions. [This is discussed here.](https://github.community/t/why-does-this-forum-need-permission-to-act-on-my-behalf/120453)

Furthermore, the permissions that the app asks for are granted even if it's just "installed", without being "authorized".

Verifying your identity is needed so that only you can view links to private repositories and your organizations. Other things, well, the service is not even asking for.

Feel free to [revoke](https://github.com/settings/apps/authorizations) this part (but keep the [install](https://github.com/settings/installations)) when you're done with this website's UI.

Privacy policy
--------------

An exhaustive list of what this service stores:

* Server-side:
    * Full repository names that you gave access to.
* Client-side: nothing.

The server of the main instance also keeps access logs and application logs for up to 3 months.

This page will be updated if this changes.

Pricing
-------

nightly.link is provided totally free of charge, including the main instance that has been running at the author's own expense.

If you rely on the service, **please support its continued maintenance by donating to the author**.

**[GitHub sponsors page of @oprypin](https://github.com/sponsors/oprypin)**

No paid features are currently planned.

Author
------

This service is developed and run by [Oleh Prypin](http://pryp.in/).

It has no affiliation with my employer. No affiliation with GitHub either.

Contact
-------

Open an issue at [https://github.com/oprypin/nightly.link/issues](https://github.com/oprypin/nightly.link/issues)

Source code
-----------

The source code is available in a Git repository at [https://github.com/oprypin/nightly.link](https://github.com/oprypin/nightly.link)

### License

Copyright (C) 2020 Oleh Prypin

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see [https://www.gnu.org/licenses/](https://www.gnu.org/licenses/).