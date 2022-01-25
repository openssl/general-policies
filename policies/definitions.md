# OpenSSL terms and definitions

## ABI

Application binary interface.

An ABI compatible release allows applications to
be relinked against the new library with the expectation that everything will
continue to function.

## Alpha release

An [alpha release] is an early pre-release version.
Refer to the [versioning policy] for specific details.

## API

Application programming interface.

An API compatible release allows application to be recompiled against the new
library with the expectation that everything will continue to function.

Refer to the [API compatibility policy] for specific details.

## Beta release

A [beta release] is a late pre-release version.
Refer to the [versioning policy] for specific details.

## Bug fix

A bug fix is a fix of functionality of the libraries, modules, applications
or the build system.
Refer to the [stable release update policy] for specific details.

## End-user documentation

End-user documentation is documentation intended for users of the OpenSSL
libraries and commandline utilities.
Refer to the [stable release update policy] for specific details.

## LTS

[Long term support].  These releases are supported for longer than normal
releases.  Refer to the [versioning policy] for specific details.

## Major release

A [major release] is one where API and ABI breaking changes are permitted.
Refer to the [versioning policy] for specific details.

## Minor release

A [minor release] is one where API and ABI breaking changes are **not** permitted
and additional functionality can be added.
Refer to the [versioning policy] for specific details.

## OMC

_OpenSSL Management Committee_.
This group oversees all managerial and administrative aspects of the project.
The OMC is the final authority for the OpenSSL project.

## OTC

_OpenSSL Technical Committee_.
This group oversees all technical aspects of the project.

## Patch release

A [patch release] is one where API and ABI breaking changes are **not** permitted
and no additional functionality can be added.
Refer to the [versioning policy] for specific details.

## Public interface

A public interface is any function, global variable, structure or macro
declared in a public header file.
Refer to the [API compatibility policy] for specific details.

## Stable release

A stable release is a patch release from an existing supported minor
release branch.


[alpha release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#alpha-release
[beta release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#beta-release
[Long term support]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#long-term-stable-release
[major release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#major-release
[minor release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#minor-release
[patch release]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#patch-release
[versioning policy]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md
[stable release update policy]: https://github.com/openssl/technical-policies/blob/master/policies/stable-release-updates.md
[API compatibility policy]: https://github.com/openssl/technical-policies/blob/master/policies/api-compat.md
