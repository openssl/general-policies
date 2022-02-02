
# Policy for OpenSSL Committers

## Who is a committer?

OpenSSL committers are contributors who have commit access to the OpenSSL
source code repository.  Committers review and commit their own patches
as well as those of other contributors.

## How to become a committer?

Commit access is granted by the OpenSSL Management Committee (OMC)
typically on the recommendation of the OpenSSL Technical Committee (OTC)
(see the OpenSSL Bylaws).

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
tracker, and our mailing lists find impactful ideas to work on.

## How to maintain committer status?

To maintain committer status, you must stay active in the project.  Refer
to the OpenSSL Bylaws for details.

In the unlikely and unfortunate event that your actions conflict with
the project objectives or are otherwise disruptive, committer status
may also be revoked by the OMC.

## Approvals and code reviews

All submissions must be reviewed and approved by at least two committers,
one of whom must also be an OTC member.  If the author is also a committer
then that counts as one of the reviews.  In other words:

* OTC members need one approval from any committer
* Committers need one approval from an OTC member
* Contributors without commit rights need two approvals, including
  one from an OTC member.

An OMC member may apply an OMC-hold to a submission.  An OTC member may
apply an OTC-hold to a submission.  An OMC-hold may be cleared by being
removed by the member that put in place the hold or by a vote of the
OMC.  An OTC-hold may be cleared by being removed by the member that put
in place the hold or by a vote of the OTC.

Approved submissions (outside of the automated release process and NEWS.md
and CHANGES.md file updates) shall only be applied after a 24-hour delay from
the approval (except for minor build and test breakage fix approvals).

Contributors without commit rights cannot formally approve patches but
are nevertheless welcome to comment on submissions and do technical
reviews.  We always value another pair of eyes, and volunteering for
reviews counts favourably towards becoming a committer.  As an author,
we ask that you address all comments, even if you already have the
necessary approvals.

If you have trouble finding consensus on a difficult review, reach out to
the OTC at otc@openssl.org (private, moderated) or the project
at openssl-project@openssl.org (public, moderated).  On GitHub, you can
target the OMC members with @openssl/omc, OTC members with @openssl/otc,
or committers with @openssl/committers.

## Commit workflow

We do code reviews on GitHub.  The OpenSSL GitHub repository is a mirror,
so we do not merge on GitHub.  When you become a committer, we'll send
you instructions to get commit access to the main repository.  To have
handy links to review history, we record the reviewers and GitHub pull
request IDs in commit headers.  We have some helper scripts in the tools
repo to add these headers automatically.

We don't use merge commits.

If at any point during development or review you discover a potential
security issue, we ask that you report it to openssl-security@openssl.org
and don't discuss it further in public.  We review security issues
privately, however acceptance of a submission for a security issue does
not bypass the review process that applies to all submissions.

## A note on CLAs

All authors, including committers, must have current CLAs on file.  A CLA
is not required for trivial contributions (e.g. the fix of a spelling
mistake).  Refer to the CLA page for further details.
