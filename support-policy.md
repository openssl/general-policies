Support and Stability policy
============================

With regards to current and future releases the OpenSSL project has adopted the
following policy:

* Version 3.0 will be supported until 2023-09-07.
* Version 1.1.1 will be supported until 2023-09-11 (LTS).
* Version 1.0.2 is no longer supported. Extended support for 1.0.2 to gain
access to security fixes for that version is
[available](https://www.openssl.org/support/contracts.html).
* Versions 1.1.0, 1.0.1, 1.0.0 and 0.9.8 are no longer supported.

We may designate a release as a Long Term Support (LTS) release. LTS releases
will be supported for at least five years and we will specify one at least every
four years. Non-LTS releases will be supported for at least two years.

During the final year of support, we do not commit to anything other than
security fixes. Before that, bug and security fixes will be applied as
appropriate.

Stability
---------

No API or ABI breaking changes are allowed in a minor or patch release.

No existing public interface can be removed until its replacement has been in
place in an LTS stable release. The original interface must also have been
documented as deprecated for at least 5 years. A public interface is any
function, structure or macro declared in a public header file.

Refer to the OTC's
[Stable Release Updates Policy](https://github.com/openssl/technical-policies/blob/master/policies/stable-release-updates.md)
for further details.
