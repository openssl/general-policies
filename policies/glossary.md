# Glossary of OpenSSL terms

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

## CCLA

_Corporate Contributor Licence Agreement_

The [CCLA] is a legal document that grants certain rights to code
contributed as part of the employment of the contributor.  All non-trivial
contributions on behalf of an employer must be submitted under a CCLA.

Also see: [ICLA](#icla)

## CHANGES

Significant modifications for the OpenSSL library or commands are
documented in the [CHANGES.md] file.

## CLA

_Contributor Licence Agreement_

This is a legal document that grants certain rights to your contributed
code.  All non-trivial contributions must be submitted under a CLA,
either an ICLA for personal contributions or both an ICLA and a CCLA
for work related contributions.

Also see: [Contributor Agreements], [ICLA](#icla), [CCLA](#ccla)

## Committer

OpenSSL committers are contributors who have commit access to the OpenSSL
source code repository.

## End-user documentation

End-user documentation is documentation intended for users of the OpenSSL
libraries and commandline utilities.

## ICLA

_Individual Contributor Licence Agreement_

The [ICLA] is a legal document that grants certain rights to your
contributed code.  All non-trivial contributions must be submitted under
an ICLA.

Also see: [CCLA](#ccla)

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

This group oversees all managerial and administrative aspects of the project.
The OMC is the final authority for the OpenSSL project.
The OMC is governed by the [OpenSSL Bylaws] and the various policy documents.

## OTC

_OpenSSL Technical Committee_

This group oversees all technical aspects of the project.
The OTC is governed by the [OpenSSL Bylaws] and the various policy documents.

## Patch release

A [patch release] is one where API and ABI breaking changes are **not** permitted
and no additional functionality can be added.
Refer to the [versioning policy] for specific details.

## Public interface

A public interface is any function, global variable, structure or macro
declared in a public header file.
Refer to the [API compatibility policy] for specific details.

## Stable release

A stable release is one where the permitted changes are minimised.
Refer to the [stable release updates policy] for specific details.


[alpha release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#alpha-release
[beta release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#beta-release
[Long term support]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#long-term-stable-release
[major release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#major-release
[minor release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#minor-release
[patch release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#patch-release
[versioning policy]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md
[stable release updates policy]: https://github.com/openssl/technical-policies/blob/master/policies/stable-release-updates.md
[API compatibility policy]: https://github.com/openssl/technical-policies/blob/master/policies/api-compat.md
[ICLA]: https://www.openssl.org/policies/openssl_icla.pdf
[CCLA]: https://www.openssl.org/policies/openssl_ccla.pdf
[Contributor Agreements]: https://www.openssl.org/policies/cla.html
[OpenSSL Bylaws]: https://www.openssl.org/policies/omc-bylaws.html
[CHANGES.md]: https://github.com/openssl/openssl/blob/master/CHANGES.md
[NEWS.md]: https://github.com/openssl/openssl/blob/master/NEWS.md
