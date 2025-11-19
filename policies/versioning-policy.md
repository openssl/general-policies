# OpenSSL release versioning policy

This document describes the release versioning scheme used by the OpenSSL
project from version 3.0.0 onwards.  It also details the level of [ABI] and
[API] compatibility each version represents.

> _Note: All examples herein are illustrative and do not constitute part of the
> versioning policy._

The version scheme consists a triple of numbers:
**[major]**.**[minor]**.**[patch]**.

> For example, the version _3.0.1_ has a _major_ version of _3_, a _minor_
> version of _0_ and a _patch_ version of _1_.

This closely aligns with the expectations of users who are familiar
with _semantic versioning_.  However, it is not quite _semantic versioning_
because adopting _semantic versioning_ would mean changing our current
Long Term Support ([LTS]) policies and practices.

## Major release

A major release is indicated by changing the _first number_ of the version.
A major release can, and generally will, introduce API and ABI breaking
changes.

> For example, a program that runs with OpenSSL 3.0.1 should not expect to run
> with OpenSSL 4.0.0 without modifications.  If it does run, it might not be
> as efficient as it was.

In order to maintain stability and limit rework across major versions:

- Existing [public interfaces] will remain unmodified except where changes
  are unlikely to break source compatibility or where structures are being
  made opaque.
- No existing public interface can be removed until its replacement has
  been in place in an LTS stable release. The original interface must
  remain in at least one supported release for at least 5 years after
  it is first documented as deprecated in any release.
- When structures are made opaque, any newly required accessor macros
  or functions are added in a feature release of the extant LTS release
  and all supported intermediate successor releases.

Exceptions to these rules can be granted by the OpenSSL Foundation and
the OpenSSL Corporation directors.  See also the [stable release update policy].

## Minor release

A minor release is indicated by changing the _second_ number of the version.
A minor release can, and generally will, introduce new features.  However both
the API and ABI will be preserved.

> For example, a program built with OpenSSL release 3.0.1 will be able to
> run with OpenSSL 3.1.0 but might not be able to take advantage of new
> features without modification.

Exceptions to these rules can be granted by the OpenSSL Foundation and
the OpenSSL Corporation directors.

## Patch release

A patch release is indicated by changing the _final_ number of the version.
A patch release will only contain bug and security fixes.
Both the API and ABI will remain compatible across patch releases.

> For example, a program linked with OpenSSL release 3.0.0 can
> run with OpenSSL 3.0.1 without changes.

Exceptions to these rules can be granted by the OpenSSL Foundation and
the OpenSSL Corporation directors.

## Long term stable release

A release can be designated as a long term stable (LTS) release.
LTS releases will be supported for at least five years and the project
will specify an LTS release every second year.

## Supported releases

Non-LTS releases will be supported for at least thirteen months.

The addition of new platforms to both LTS and non-LTS releases is
acceptable so long as the required changes consist solely of additions
to the build configuration.

## Pre-release versions

Before a major release the project will generally make a number of pre-releases.
These are labelled _alpha_ and _beta_ releases.

### Alpha release

An _alpha_ release is one that:

- is not necessarily feature complete and
- does not necessarily includes all new APIs.

### Beta release

A _beta_ release is one that:

- is feature complete;
- indicates a feature freeze and
- only bug fixes are permitted.

## History

From release 1.0.0, but prior to release 3.0.0, the OpenSSL versioning scheme
was different and it is detailed here for historic purposes.

- Letter releases, such as 1.0.2a, exclusively contain bug and security
  fixes and no new features.
- Releases that change the _final_ number, e.g. 1.1.0 vs. 1.1.1, can and
  are likely to contain new features, but in a way that does not break
  binary compatibility.  This means that an application compiled and
  dynamically linked with 1.1.0 does not need to be recompiled when the
  shared library is updated to 1.1.1.
- Releases that change the _second_ number, e.g. 1.0.0 vs 1.1.0, break
  both ABI and API compatibility.  The primary instance of this was the
  transition to opaque internal structures that occurred with OpenSSL
  release 1.1.0.

[ABI]: /policies/general/glossary/#abi
[API]: /policies/general/glossary/#api
[LTS]: /policies/general/glossary/#lts
[major]: /policies/general/glossary/#major-release
[minor]: /policies/general/glossary/#minor-release
[patch]: /policies/general/glossary/#patch-release
[public interfaces]: /policies/general/glossary/#public-interface
[stable release update policy]: /policies/technical/stable-release-updates/
