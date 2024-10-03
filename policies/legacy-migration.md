# Legacy Provider Policy

## Purpose
The Legacy Provider exists to create an opt-in availability mechanism for
algorithms that, for various reasons, should have their use discouraged.  These
reasons include, but are not limited to:

* Discovered security issues leaving the algorithm in question unsafe for
  general use

* Lack of popular use (i.e. balancing code size vs consumption frequency)

OpenSSL recognizes that consumption of these algorithms may continue to be
required by consuming applications after the conditions above have been
recognized.  The Legacy provider exists to provide a mechanism for such
applications to continue having access to these algorithms while preventing
applications that don't require them from inadvertently using them.

## Constraints on moving an algorithm to the legacy provider

1) Migration of an algorithm to the legacy provider must occur on a semantically
versioned major release boundary.  Once a major release includes a given
algorithm in a given provider, it must remain there for every minor release in
that major stream.

2) Prior to migration, the migration must be announced for at least 1
semantically versioned minor release (see announcement mechanism below).

3) Coincidental to the announcement above, the algorithm in question may be made
available in both the source provider and the legacy provider.

## Promotion of algorithms in the legacy provider to the default provider

Should the need arise, legacy provider algorithms may be promoted to the default
provider at any time.  Removal from the Legacy provider should occur only on
semantically versioned major release boundaries.

## Migration announcement mechanism
Announcements of migrations from the default provider to the Legacy provider is
made  via the DEPRECATIONS.md file in the source code root directory for
OpenSSL.  This file will list the algorithm SN, NID, the version in  which the
deprecation was announced, and the version in which the algorithm is to be
removed from the default provider.
