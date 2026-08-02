# OpenSSL Library FIPS Module Support Policy

## 1. Principle

FIPS validated cryptography is delivered by the OpenSSL Library FIPS provider
(the "module"), which is validated independently of the OpenSSL Library.
A validated module is built from the source of the release it was validated
against. It may be used, unchanged, together with a library built from any
supported OpenSSL Library release from version 3.0 onwards:
provider compatibility is maintained backward and forward across these
releases, including future major release series, for as long as the module
remains supported under this policy. The support status of an OpenSSL
Library release version and the support status of an OpenSSL Library FIPS
module are therefore distinct: a module can remain supported after its
OpenSSL Library release version has reached end of life.

See the FIPS module guide,
[fips_module(7)](https://docs.openssl.org/master/man7/fips_module/), and
[README-FIPS.md](https://github.com/openssl/openssl/blob/master/README-FIPS.md),
which is included in every OpenSSL Library source distribution.

## 2. Commitment

Every OpenSSL Library FIPS module holding an active NIST CMVP certificate is
supported for the lifetime of that certificate, up to the certificate's end
date, regardless of the support status of the OpenSSL Library release version
it was built from.

For each such module, the OpenSSL Project will:

1. **Assess** every OpenSSL Library security issue (CVE) for impact within
   the module's validated boundary.
2. **Disclose** that assessment publicly (Section 3).
3. **Produce maintenance source releases** containing the relevant fixes.
   The decision to produce a maintenance release, including its timing and
   which accumulated fixes it carries, is made at the discretion of the
   OpenSSL Project.
4. **Pursue certificate updates** via the CMVP CVE re-validation path, at
   the discretion of the OpenSSL Project, adding the fixed module version
   to the existing certificate while keeping previously validated versions
   valid wherever possible.

Support for a module ends on its certificate's end date. This is a fixed
calendar date, not subject to extension under this policy. For certificate
#4985 (FIPS provider 3.1.2), the end date is 10 March 2030. The currently
validated modules and their certificate end dates are published on the
[FIPS and CVEs page](https://openssl-library.org/news/fips-cve/) and in the
NIST CMVP database.

## 3. Disclosure

- Security advisories state OpenSSL Library FIPS module impact explicitly,
  affected or not affected with the reason, for every module version holding
  an active NIST CMVP validation, including modules whose OpenSSL Library
  release version has reached end of life.
- The [FIPS and CVEs page](https://openssl-library.org/news/fips-cve/) lists
  every CVE affecting a validated module, including those on end-of-life
  OpenSSL Library versions, whether or not a fixed release exists at the time
  of publication.

## 4. Availability

- OpenSSL Library release versions that have reached end of life are not
  maintained in the public source trees, and maintenance releases for them
  are not published publicly. These versions are not recommended for use
  beyond the end of life date.
- Maintenance source releases for FIPS modules on end-of-life OpenSSL Library
  versions (for example, OpenSSL 3.1.9 for the 3.1.2 module) are distributed
  through [OpenSSL Corporation](https://openssl-corporation.org/)
  [FIPS module support
  services](https://openssl-corporation.org/solutions-fips-policy.html),
  which also cover updates to certificates derived from OpenSSL Library FIPS
  base certificates by rebranding.
- Version numbering continues the upstream sequence, and the FIPS module
  version matches the release it is built from. The OpenSSL Library does not
  have separate FIPS-only branches: the FIPS module is contained within the
  main OpenSSL Library release.

## 5. The base library

This policy covers only code within the OpenSSL Library FIPS module boundary.
The base OpenSSL library (code outside the boundary) must be built from a
supported release train, publicly supported or covered by a
[support agreement](https://openssl-corporation.org/support/), to receive
security fixes and other improvements. Use of an
end-of-life OpenSSL Library version is not covered by this policy;
availability of a module maintenance release does not constitute extended
support.

## 6. Going forward

The OpenSSL Project is moving to validate every OpenSSL Library minor
release, including non-LTS releases, with the goal of keeping at least two
validated modules overlapping at all times, so customers always have a
validated target to move to. The 3.1.2 module is governed by this policy
until certificate #4985 reaches its end date on 10 March 2030.
