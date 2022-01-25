# OpenSSL terms and definitions

## ABI

Application binary interface.

An ABI compatible release allows applications to
be relinked against the new library with the expectation that everything will
continue to function.

## API

Application programming interface.

An API compatible release allows application to be recompiled against the new
library with the expectation that everything will continue to function.

## LTS

Long term stable.  These releases are supported for longer than normal releases.
Refer to the [versioning policy] for specific details.

[versioning policy]: [patch]: https://github.com/openssl/general-policies/blob/master/policies/versioning-policy.md#long-term-sable-releases

## Major release

A major release is one where API and ABI breaking changes are permitted.

## Minor release

A minor release is one where API and ABI breaking changes are **not** permitted
and additional functionality can be added.

## OMC

_OpenSSL Management Committee_.
This group oversees all managerial and administrative aspects of the project.
The OMC is the final authority for the OpenSSL project.

## OTC

_OpenSSL Technical Committee_.
This group oversees all technical aspects of the project.

## Patch release

A patch release is one where API and ABI breaking changes are **not** permitted
and no additional functional can be added.

## Public interfaces

A public interface is any function, global variable, structure or macro
declared in a public header file.
