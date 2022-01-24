# OpenSSL release versioning policy

This document describes the release versioning scheme used by the OpenSSL
project from version 3.0.0 onwards.  It also details the level of [ABI] and
[API] compatibility each version represents.

The version scheme consists a triple of numbers:
**[major]**.**[minor]**.**[patch]**.

> For example, the version _3.0.1_ has a _major_ version of _3_, a _minor_
> version of _0_ and a _patch_ version of _1_.

This closely aligns with the expectations of users who are familiar
with _semantic versioning_.  However, it is not quite _semantic versioning_
because adopting _semantic versioning_ would mean changing our current
Long Term Support ([LTS]) policies and practices.

## Major release: changing the first digit

A major release can, and generally will, introduce API and ABI breaking
changes.

> For example, a program that runs with OpenSSL 3.0.1 should not expect to run
> with OpenSSL 4.0.0 without modifications.  If it does run, it might not be
> as efficient as it was.

In order to maintain stability and limit rework across major versions:

- No existing public interface can be modified except where changes
  are unlikely to break source compatibility or where structures are being
  made opaque.
- No existing public interface can be removed until its replacement
  has been in place in an LTS stable release. The original interface
  must also have been documented as _deprecated_ for at least 5 years. A
  public interface is any function, global variable, structure or macro
  declared in a public header file.
- When structures are made opaque, any newly required accessor macros
  or functions are added in a feature release of the extant LTS release
  and all supported intermediate successor releases.

Exceptions to these rules require a vote by the [OMC].  See also the
[stable release update policy].

## Minor release: changing the second digit

A minor release can, and generally will, introduce new features.  However both
the API and ABI will be preserved.

> For example, a program built with OpenSSL release 3.0.1 will be able to
> run with OpenSSL 3.1.0 but might not be able to take advantage of new
> features without modification.

Exceptions to these rules require a vote by the OMC.

## Patch release: changing the third digit

A patch release will only contain bug fixes.  Both the API and ABI will remain
compatible across patch releases.

> For example, a program linked with OpenSSL release 3.0.0 can
> run with OpenSSL 3.0.1 without changes.

Exceptions to these rules require a vote by the OMC.

## Long term sable releases

A release can be designated as a release.  LTS releases will be supported
for at least five years and the project will specify a LTS release at
least every four years.  Non-LTS releases will be supported for at least
two years.

During the final year of support, we do not commit to anything other
than security fixes.  Before that, bug and security fixes will be applied
as appropriate.

The addition of new platforms to LTS branches is acceptable so long as
the required changes consist solely of additions to configuration.

## Prerelease versions

Before a major release the project will generally make a number of pre-releases.
These are labelled _alpha_ and _beta_ releases.

### Alpha releases

An _alpha_ release is one that is:

- not necessarily feature complete and
- not necessarily includes all new APIs.

### Beta releases

A _beta_ release is one that:

- is feature complete;
- indicates a feature freeze and
- only bug fixes are permitted.

## Release criteria

For a major or minor release, the following release criteria apply:

- all open GitHub issues and pull requests older than 2 weeks at the time of
  release need to be assessed for relevance to the version being released.
  Any flagged with the a milestone for the version to be released must
  be closed (see below);
- clean builds in GitHub Actions for two days and
- no open Coverity issues (not flagged as _False Positive_ or _Ignore_).

Valid reasons for closing an issue/PR with a milestone for the version
include:

- we have just now or sometime in the past fixed the issue;
- unable to reproduce (following discussion with original reporter
  if possible);
- working as intended;
- deliberate decision not to fix this issue until a later release (this
  wouldn't actually close the issue/PR but change the milestone instead) and
- not enough information and unable to contact reporter.

Exceptions require a vote by the [OTC].

## History

From release 1.0.0, but prior to release 3.0.0, the OpenSSL versioning scheme
was different and it is detailed here for historic purposes.

- Letter releases, such as 1.0.2a, exclusively contain bug and security
  fixes and no new features.
- Releases that change the last digit, e.g. 1.1.0 vs. 1.1.1, can and
  are likely to contain new features, but in a way that does not break
  binary compatibility.  This means that an application compiled and
  dynamically linked with 1.1.0 does not need to be recompiled when the
  shared library is updated to 1.1.1.
- Releases that change the second digit, e.g. 1.0.0 vs 1.1.0, break
  both ABI and API compatibility.  The primary instance of this was
  the transition to opaque internal structures occurred with OpenSSL
  release 1.1.0.

It should be noted that some features are transparent to the application
such as the maximum negotiated TLS version and cipher suites, performance
improvements and so on.  There is no need to recompile applications to
benefit from these features.

[ABI]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#abi
[API]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#api
[LTS]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#lts
[OMC]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#omc
[OTC]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#otc
[major]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#major-release
[minor]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#minor-release
[patch]: https://github.com/openssl/general-policies/blob/master/policies/definitions.md#patch-release
[stable release update policy]: https://github.com/openssl/technical-policies/blob/master/policies/stable-release-updates.md
