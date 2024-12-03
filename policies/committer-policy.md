# Policy for OpenSSL Committers

## Who is a committer?

OpenSSL committers are contributors who have commit access to the OpenSSL
source code repository.  Committers review and commit their own patches
as well as those of other contributors.

## How to become a committer?

Commit access is granted by a vote of the [OMC] typically on the
recommendation of the [OTC] (see the [OpenSSL Bylaws]).

We welcome contributors who become domain experts in some part of
the library (for example, low-level crypto) as well as generalists
who contribute to all areas of the codebase.  All committers share
the responsibility for the overall health of the project: aside from
contributing quality features, committers are team players who fix bugs,
address open issues, review community contributions, and improve tests
and documentation.  Committers are also shepherds of the OpenSSL community
and its code of conduct.

To become a committer, start by contributing code.  Read our coding style,
and get to know our build and test system.  Then, use the Github issue
tracker, and our mailing lists to find impactful ideas to work on.

## How to maintain committer status?

To maintain committer status, you must stay active in the project.  Refer
to the OpenSSL Bylaws for details.

In the unlikely and unfortunate event that your actions conflict with
the project objectives or are otherwise disruptive, committer status
may also be revoked by the OMC.

## Approvals and code reviews

All submissions must be reviewed and approved by at least two committers.
Neither of the reviewers can be the author of the submission.

The sole exception to this is during the release process where the
author's review does count towards the two needed for the automated
release process and [NEWS] and [CHANGES] file updates.

In the case where two committers make a joint submission, they can review
each other's code but not their own.  A third reviewer will be required.

An OMC member may apply a _hold: needs OMC decision_ label to a submission.
An OTC member may apply a _hold: needs OTC decision_ to a submission.
A _hold: needs OMC decision_ label may be removed by the member that put
in place the hold or by a decision of the OMC.
A _hold: needs OTC decision_ label may be removed by the member that put
in place the hold or by a decision of the OTC.

Approved submissions (outside of the automated release process and
NEWS and CHANGES file updates) shall only be applied after a 24-hour
delay from the approval.  An exception to the delay exists for build and
test breakage fix approvals which should be flagged with the _severity:
urgent_ label.

The use of the _severity: urgent_ label should be limited to contexts where the
breakage of the CI builds and tests (including buildbot) happened within the
last 72 hours and the change is straightforward.

Contributors without commit rights cannot formally approve patches but
are nevertheless welcome to comment on submissions and do technical
reviews.  We always value another pair of eyes, and volunteering for
reviews counts favourably towards becoming a committer.  As an author,
we ask that you address all comments, even if you already have the
necessary approvals.

If you have trouble finding consensus on a difficult review, reach out to
the OTC at `otc@openssl.org` (private, moderated) or the project
at `openssl-project@openssl.org` (public, moderated).  On GitHub, you can
reach the OMC members with `@openssl/omc`, OTC members with `@openssl/otc`,
or committers with `@openssl/committers`.

## Commit workflow

Code changes are submitted on Github as pull requests, which are subject to
peer review.  The OpenSSL GitHub repository is a mirror, so we do not merge
on GitHub.  When you become a committer, we'll send you instructions to get
commit access to the main repository.  To have handy links to review
history, we record the reviewers and GitHub pull request IDs in commit
headers.  We have some helper scripts in the tools repo to add these headers
automatically.

Some commits, created and signed by OpenSSL designated bots, may be reviewed
by other means, and do not receive review records as described above.

We don't use merge commits.

If at any point during development or review you discover a potential
security issue, we ask that you report it to `openssl-security@openssl.org`
and don't discuss it further in public.  We review security issues
privately, however acceptance of a submission for a security issue does
not bypass the review process that applies to all submissions.

## CLAs

All authors, including committers, must have current [CLAs] on file.
Refer to the [Contributor Agreements] page for further details.

## Trivial submissions

A CLA is not required for trivial contributions (e.g. the fix of a
spelling mistake).  All reviewers and the submission author need to
agree that a submission is trivial and the _cla: trivial_ label should
be applied to indicate this.

[Contributor Agreements]: /policies/cla/
[OpenSSL Bylaws]: https://www.openssl.org/policies/omc-bylaws.html
[OMC]: /policies/general/glossary/#omc
[OTC]: /policies/general/glossary/#otc
[CLAs]: /policies/general/glossary/#cla
[NEWS]: /policies/general/glossary/#news
[CHANGES]: /policies/general/glossary/#changes
[OpenSSL Bylaws]: /policies/general/glossary/#bylaws
