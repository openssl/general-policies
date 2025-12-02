# Feature Branch Approval Policy

The [Time-based Release Policy] defines a regular twice-a-year schedule for new
OpenSSL versions. In the case of large features that cannot reasonably be
implemented and reviewed within a single PR there is a risk that only an
incomplete or incorrect implementation of the feature will be merged to the
master branch by the time a feature freeze occurs for the next release.

To avoid this problem feature branches can be used. A feature branch is simply
a branch in the main git repository that can be used as a target branch for
PRs related to a single new feature.

A feature branch will be created based on the current state of master at the
time of its creation. If a feature branch exists for a protracted period of time
then it will need to be rebased on a regular basis. This process should be
performed by a committer on an as-needed basis and can be done without further
review.

The creation of a new feature branch implies some overhead for the project to
manage that feature branch (such as for example periodic rebases, and to review
PRs targeting it). Such a feature branch would typically only be created where
it has been agreed that the feature is desirable; exists on the [Project Board];
is of sufficiently high priority; and there are expected to be resources
available to work on the feature development and to review it. For this reason
the creation of new feature branches is controlled via an approval process.

Submitting a request for a new feature branch should be done by creating an
issue in the [openssl/project] repository. Such a request can be created by
anyone. The request should specify:

- The name of the feature branch requested in the form of `feature/<name>`
- A link to an issue describing the requested feature that will be developed on
  the branch
- An estimate of when the work on the feature is expected to be complete
- Whether there are any known resources being made available to work on the
  feature

The approval of a new feature branch is ultimately performed by the OpenSSL
Foundation or OpenSSL Corporation directors who might delegate this
responsibility to a designated person or committee.

Once approved a feature branch may be created. All PRs relevant to
that feature should target that branch and go through the normal code review
process.

Once the feature is complete and all relevant PRs have been merged to the branch,
a PR should be created containing all the commits from the branch. All of the
commits should already have been reviewed before they were pushed to the
feature branch. However this PR review stage enables a final check to confirm
the complete feature is sane. Once this PR is merged, the feature branch should
then be deleted from the repository.

[Time-based Release Policy]: /policies/general/release-policy/
[Project Board]: https://github.com/orgs/openssl/projects/2/views/28
[openssl/project]: https://github.com/openssl/project
