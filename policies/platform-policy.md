# Platform Policy

Platforms are classified as "primary", "secondary", "community"
and "unadopted". Support for a new platform should only be added if it
is being adopted as a primary, secondary or community platform.

[Current platforms](../policy-supplemental/platforms.html)

## Primary

*Definition:* A platform that is regularly tested through project CI
on a project owned and managed system.
    
New Pull Requests (PRs) should not be merged unless the primary
platforms are showing as "green" in CI. If the CI breaks for a branch
(such as for a stable version or master) then it should be fixed as a
priority.

## Secondary

*Definition:* A platform that is regularly tested through project CI
on a system that is not owned or managed by the project. At least one
project committer must have access to the system and be able and
willing to support it.

New Pull Requests (PRs) should avoid introducing new breaks to CI in
secondary platforms where possible but may still be merged where a
resolution is not easily achievable without access to the platform. If
the CI for a branch (such as for a stable version or master) on a
secondary platform breaks, then a resolution should be sought as soon
as is practically possible and before a release is made from the
branch.

## Community

*Definition:* Platforms that one or more members of the OpenSSL
community have volunteered to support. May or may not be in project
CI. Members of the community providing support do not have to be
committers.
    
Where a community platform is in project CI then new Pull Requests
(PRs) should avoid introducing new breaks to CI on such platforms
where possible but may still be merged where a resolution is not
easily achievable without access to the platform. If the CI for a
branch (such as for a stable version or master) on a community
platform breaks, then an attempt should be made to contact the
community maintainer to request a fix. In the event that a community
platform is broken in CI for a protracted period then it may be
dropped from CI.\
If defects are raised that are specific to a community platform then
the community maintainer may be contacted to help find a
resolution. If a community maintainer is unresponsive, or unable to
provide fixes then the platform may be moved to "unadopted".

## Unadopted

*Definition:* Platforms that no one has volunteered to support.
    
Support may still be provided for such platforms where possible
without access to the platform itself. Platform specific issues may be
left unresolved where it is not feasible to find a suitable fix.
Support for such platforms may be removed entirely from the OpenSSL
code base in future releases.
