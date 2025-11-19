# Glossary of OpenSSL terms

This is a _glossary of terms_, it does not include any _formal definitions_ of
the included terms.  It does, however, link to the _formal definition_ where
appropriate.  In the event in a conflict between this glossary and the
_formal definition_, the _formal definition_ is **always** canonical.

## ABI

_Application binary interface_

An ABI compatible release allows a shared library to be replaced with a
new version or for applications to be relinked against the new library
with the expectation that everything will run.

ABI compatible releases are also [API](#api) compatible.

## Alpha release

An [alpha release] is an early pre-release version.
Refer to the [versioning policy] for specific details.

## API

_Application programming interface_

An API compatible release, that is not [ABI](#abi) compatible, allows
application to be recompiled against the new library with the expectation
that everything will run.

Refer to the [API compatibility policy] for specific details.

## Beta release

A [beta release] is a late pre-release version.
Refer to the [versioning policy] for specific details.

## Bug fix

A bug fix is a fix of functionality of the libraries, modules, applications
or the build system.
Refer to the [stable release updates policy] for specific details.

## Bylaws

The [OpenSSL Bylaws] provide the rules under which the OpenSSL project operates.

## CCLA

_Corporate Contributor Licence Agreement_

The [CCLA] is a legal document that grants certain rights to code
contributed as part of the employment of the contributor.  All non-trivial
contributions on behalf of an employer must be submitted under a CCLA.

Also see: [ICLA](#icla)

## CHANGES

Significant modifications for the OpenSSL library or commands are
documented in the [CHANGES.md] file.

## CI

_Continuous Integration_

A suite of tests and checks that are run on every pull request, commit or on a daily basis.

## CLA

_Contributor Licence Agreement_

This is a legal document that grants certain rights to your contributed
code.  All non-trivial contributions must be submitted under a CLA,
either an ICLA for personal contributions or both an ICLA and a CCLA
for work related contributions.

Also see: [Contributor Agreements], [ICLA](#icla), [CCLA](#ccla)

## Committer

OpenSSL [committers] are contributors who have commit access to the OpenSSL
source code repository.

## End-user documentation

End-user documentation is documentation intended for users of the OpenSSL
libraries and commandline utilities.

## Functional behaviour

What the system does, rather than how it does it.
Refer to the [testing policy] for specific details.

## ICLA

_Individual Contributor Licence Agreement_

The [ICLA] is a legal document that grants certain rights to your
contributed code.  All non-trivial contributions must be submitted under
an ICLA.

Also see: [CCLA](#ccla)

## LDP

_Linux Documentation Project_

Our documentation aims to broadly conform with [The Linux Documentation
Project]'s guidelines.
Refer to the [documentation policy] for specific details.

## LTS

_[Long term support]_

These releases are supported for longer than normal releases.
Refer to the [versioning policy] for specific details.

## Major release

A [major release] is one where API and ABI breaking changes are permitted.
Refer to the [versioning policy] for specific details.

## Minor release

A [minor release] is one where API and ABI breaking changes are **not** permitted
and additional functionality can be added.
Refer to the [versioning policy] for specific details.

## NEWS

Very significant modifications for the OpenSSL library or commands are
documented in the [NEWS.md] file.

## OMC

_OpenSSL Management Committee_

In the past this group was overseeing all managerial and administrative aspects
of the OpenSSL project. It was replaced by the OpenSSL Foundation Board of
Directors and the OpenSSL Corporation Board of Directors.

## OTC

_OpenSSL Technical Committee_

In the past this group was overseeing all technical aspects of the project.
The responsibilities of OTC have been replaced by the changes noted in various
policies between the OpenSSL Foundation and OpenSSL Corporation directors and
the engineering managers of the OpenSSL Foundation and the OpenSSL Corporation.

## Patch release

A [patch release] is one where API and ABI breaking changes are **not** permitted
and no additional functionality can be added.
Refer to the [versioning policy] for specific details.

## perlasm

Assembly code wrapper written in Perl.  This is done to ease compatibility
problems across assemblers, platforms and processor revisions.
For further details see the [perlasm README].

## Public interface

A public interface is any function, global variable, structure or macro
declared in a public header file.
Refer to the [API compatibility policy] for specific details.

## SRT

_Security Response Team_

A selected group of [committers], engineering managers and other team members
that handles all incoming security reports including the CVE id and
severity assignment.

## Stable release

A stable release is one where the permitted changes are minimised.
Refer to the [stable release updates policy] for specific details.


[alpha release]: /policies/general/versioning-policy/#alpha-release
[beta release]: /policies/general/versioning-policy/#beta-release
[committers]: /policies/general/committer-policy/
[Long term support]: /policies/general/versioning-policy/#long-term-stable-release
[major release]: /policies/general/versioning-policy/#major-release
[minor release]: /policies/general/versioning-policy/#minor-release
[patch release]: /policies/general/versioning-policy/#patch-release
[versioning policy]: /policies/general/versioning-policy/
[stable release updates policy]: /policies/technical/stable-release-updates/
[testing policy]: /policies/technical/testing/
[documentation policy]: /policies/technical/documentation-policy/#language
[API compatibility policy]: /policies/technical/api-compat/
[perlasm README]: https://github.com/openssl/openssl/blob/master/crypto/perlasm/README.md
[ICLA]: /policies/openssl_icla.pdf
[CCLA]: /policies/openssl_ccla.pdf
[Contributor Agreements]: /policies/cla/
[OpenSSL Bylaws]: https://www.openssl-library.org/about/bylaws/
[CHANGES.md]: https://github.com/openssl/openssl/blob/master/CHANGES.md
[NEWS.md]: https://github.com/openssl/openssl/blob/master/NEWS.md
[The Linux Documentation Project]: https://tldp.org/
