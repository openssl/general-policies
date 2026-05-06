# Release Artifacts Signing Policy

This policy covers the cryptographic signing of release artifacts produced by OpenSSL Library
release automation, the keys and certificates used to produce those signatures, their lifecycle,
and the response to a suspected compromise.

## Scope

This policy applies to:

- Detached OpenPGP signature files for source distributions published as part of an OpenSSL Library
  release.  
- Authenticode signatures on Windows binaries and installers published as part of an OpenSSL Library
  release.  
- Any future signing scheme added to the release process by amendment to this policy.

This policy does not apply to signatures produced by individual contributors on their own commits,
tags, or correspondence, which are governed by the
[committer policy](/policies/general/committer-policy/) and the git workflow.

Release announcements and mailing-list messages are not release artifacts under this policy and are
not required to be signed.

This policy concerns the authenticity of release artifacts. The integrity of the build process that
produces those artifacts is governed separately.

## OpenPGP signing certificate

### Structure

The OpenPGP signing certificate is identified by its primary key fingerprint. The primary key is
long-term and certification-capable. At any given time exactly one signing subkey on the certificate
is the current signing subkey, used by the release automation to produce signatures. Predecessor
signing subkeys remain bound to the certificate so that signatures they produced continue to verify.
The certificate must not bind any subkey for purposes other than signing.

The primary key defines the identity of the certificate. It is used solely to certify the signing
subkey. The primary key is not used to sign release artifacts directly.

The signing subkey is used to sign release artifacts. The signing subkey is operated by the OpenSSL
Library release automation and is not used interactively.

### Algorithm and parameters

The primary key and the signing subkey are RSA keys with a modulus length of 4096 bits. OpenPGP
signatures produced under this policy use SHA-512 as the digest algorithm.

Post-quantum signature algorithms are not used for release artifact signing under this policy. The
algorithm requirements of this policy should be reviewed when post-quantum signature algorithms are
supported by the applicable release-signing formats, release tooling, hardware security modules, and
publicly trusted code-signing ecosystem.

### Validity

The primary key is generated with a validity period of 5 years.

The signing subkey is generated with a validity period of 1 year. Before expiry, a new signing
subkey is generated and certified by the primary key. The previous signing subkey is allowed to
expire without revocation provided it has not been compromised; signatures it has produced remain
valid for verification.

The expiration date of the primary key or a signing subkey generated under this policy may not be
extended. When either is approaching expiry, a successor is generated in accordance with
[Primary key rotation](#primary-key-rotation) or [Subkey rotation](#subkey-rotation).

### Storage

The private material of the primary key must be stored in a hardware security module from which it
cannot be exported in plaintext. The hardware security module used for the primary key must be
validated to FIPS 140-3 Level 2 or higher, or to an equivalent or successor standard approved by the
OpenSSL Foundation and the OpenSSL Corporation directors. Use of the primary key must require a
2-of-4 quorum of human-held authorisation credentials, so that no single individual can use the
primary key and so that the release automation cannot use it in routine operation. The distribution
of the authorisation credentials among custodians and any escrow location is recorded in an
operational runbook outside of this policy.

The authorisation credentials for the primary key are distributed equally between persons designated
by the OpenSSL Foundation directors and persons designated by the OpenSSL Corporation directors. The
quorum is intended as an operational control to prevent any one person from using the primary key
alone and to provide resilience against the unavailability of a credential; it is not intended to
require participation by both organisations in each primary-key operation.

The private material of the signing subkey must be protected such that a party who gains read or
code-execution access to the release automation environment cannot extract the key in plaintext.
Storage in a hardware security module accessible to the release automation satisfies this
requirement. Any hardware security module used for the signing subkey must be validated to FIPS
140-3 Level 2 or higher, or to an equivalent or successor standard approved by the OpenSSL
Foundation and the OpenSSL Corporation directors. Use of the signing subkey by the release
automation does not require quorum authorisation.

Use of the signing subkey is authorised on a per-signing-operation basis under controls described
in an operational runbook. Every signing operation is recorded in an audit log retained by the
custodian. The production of release artifacts and the signing of release artifacts are separately
authorised steps.

Audit logs for release signing operations record the identity of the key or certificate used, the
artifact name, the artifact digest, the time of signing, the requester or authorising party, the
result of the signing operation, and any error condition. Audit logs are retained in tamper-evident
storage for at least 10 years.

### Publication

The fingerprint of the current primary key is published on the OpenSSL Library website at
[https://openssl-library.org/](https://openssl-library.org/). The current OpenPGP signing
certificate, including its current signing subkey, is published on the OpenSSL Library website, in a
Web Key Directory under https://openssl-library.org/, and on the keyserver at
[https://keys.openpgp.org/](https://keys.openpgp.org/).

The fingerprint as published on the OpenSSL Library website is the canonical trust anchor. Where the
keyserver and the website disagree, the website is authoritative.

Signing certificates that have been superseded or have expired remain available on the OpenSSL
Library website as a historical archive, so that signatures on previously released artifacts can
continue to be verified.

A guide describing how to verify OpenPGP and Authenticode signatures on OpenSSL Library release
artifacts is published on the OpenSSL Library website and maintained alongside this policy.

### Subkey rotation

A new signing subkey is generated and certified by the primary key before the expiry of the current
signing subkey. The new subkey is published as described in [Publication](#publication) before it is
used to sign release artifacts.

### Primary key rotation

No later than 12 months before the primary key expires, a successor primary key is generated and its
fingerprint published on the OpenSSL Library website. A signing subkey of the successor primary key
is generated and published as described in [Publication](#publication). From a cutover date
announced on the
[OpenSSL announce list](https://groups.google.com/a/openssl.org/g/openssl-announce/), release
artifacts are signed by the signing subkey of the successor primary key.

The previous primary key and its signing subkey are allowed to expire naturally; signatures they
produced before the cutover date remain valid for verification according to the verifier's policy.

The 12-month advance requirement of this section does not apply to the initial transition from a
signing key in use at the time of policy adoption to the first signing certificate generated under
this policy.

### Compromise and revocation

A revocation certificate for the primary key is generated at the same time as the primary key,
encrypted at rest, and stored offline in at least two physically separate locations.

A suspected compromise may be declared by the signing custodian, a deputy custodian, the OpenSSL
Foundation directors, or the OpenSSL Corporation directors. Declaration by any one of these parties
is sufficient to initiate the response procedures in this section. A suspected compromise is
declared when there is credible evidence of unauthorised use, unauthorised access to private key
material, loss of control of authorisation credentials, unexplained signing activity, or a failure
of key-protection controls. The response procedures in this section begin as soon as a suspected
compromise is declared and do not require forensic certainty.

Evidence preserved under this section is retained for at least 10 years and remains under the
custody of the signing custodian.

If the primary key is suspected of compromise:

- The revocation certificate is published to the keyserver and the OpenSSL Library website is
  updated to reflect the revocation.  
- A successor primary key is generated and published as described in
  [Primary key rotation](#primary-key-rotation), without the 12-month advance period.  
- A notification is sent to the
  [OpenSSL announce list](https://groups.google.com/a/openssl.org/g/openssl-announce/).  
- Releases are suspended until a successor primary key is in use.  
- An impact statement is published identifying the release artifacts signed by the compromised key
  and the window during which it was in use.  
- Relevant logs, audit records, release artifacts, and other evidence relating to the suspected
  compromise are preserved by the custodian for subsequent investigation.  
- Release artifacts that were signed by the compromised key and remain in distribution are
  re-signed using the signing subkey of the successor primary key, and the new signatures are
  published alongside the original artifacts.

If the signing subkey is suspected of compromise:

- The signing subkey is revoked using the primary key.  
- The revocation is published to the keyserver and a notification is sent to the
  [OpenSSL announce list](https://groups.google.com/a/openssl.org/g/openssl-announce/).  
- A new signing subkey is generated and certified by the primary key.  
- Releases are suspended until a new signing subkey is in use.  
- An impact statement is published identifying the release artifacts signed by the compromised
  subkey and the window during which it was in use.  
- Relevant logs, audit records, release artifacts, and other evidence relating to the suspected
  compromise are preserved by the custodian for subsequent investigation.  
- Release artifacts that were signed by the compromised key and remain in distribution are re-signed
  using the signing subkey of the successor primary key, and the new signatures are published
  alongside the original artifacts.

## Authenticode signing for Windows

When OpenSSL Library publishes Windows binaries or installers as part of a release, those artifacts
are signed using an Extended Validation (EV) Code Signing certificate issued by a publicly trusted
Certificate Authority.

The private key associated with the certificate is stored in a hardware security module that meets
the requirements of the CA/Browser Forum. The hardware security module used for the EV Code Signing
private key must be validated to FIPS 140-3 Level 2 or higher, or to an equivalent or successor
standard accepted under the CA/Browser Forum requirements.

A fallback EV Code Signing certificate may be retained for use when the primary hardware security
module is unavailable. The fallback certificate uses a separate non-exportable private key held in a
hardware token issued by the Certificate Authority. The fallback hardware token meets the same
CA/Browser Forum requirements as the hardware security module.

The validity period, public-key algorithm, public-key parameters, and certificate signature
algorithm of EV Code Signing certificates are governed by the CA/Browser Forum requirements and the
issuing Certificate Authority's certification practice statement.

Use of an EV Code Signing private key, whether held in the primary hardware security module or in
the fallback hardware token, is authorised on a per-signing-operation basis under controls described
in an operational runbook. Every signing operation is recorded in an audit log retained by the
custodian. The production of release artifacts and the signing of release artifacts are separately
authorised steps.

Every Authenticode signature is countersigned with a trusted RFC 3161 timestamp at the time of
signing, so that the signature supports verification after the signing certificate expires. The
timestamp digest algorithm is SHA-256 or stronger. Signing is not performed when no trusted
timestamping authority is available.

A successor certificate is obtained before the expiry of the current certificate. Signatures
produced by a previous certificate remain valid for verification of artifacts signed before the
certificate's expiry where supported by the verifying party.

If the private key is suspected of compromise:

- The certificate is revoked through the issuing Certificate Authority.  
- Where supported by the issuing Certificate Authority, revocation is requested with a reason of key
  compromise and an invalidity date corresponding to the earliest known or suspected compromise
  time.
- A replacement certificate is obtained.  
- A notification is sent to the
  [OpenSSL announce list](https://groups.google.com/a/openssl.org/g/openssl-announce/).  
- Releases of Windows artifacts are suspended until the replacement certificate is in use.  
- An impact statement is published identifying the Windows release artifacts signed by the
  compromised key and the window during which it was in use.  
- Relevant logs, audit records, release artifacts, and other evidence relating to the suspected
  compromise are preserved by the custodian for subsequent investigation.

## Custodianship

A signing custodian is designated by the OpenSSL Foundation and the OpenSSL Corporation directors.
The custodian is responsible for:

- Generation, storage, rotation, and revocation of the OpenPGP primary key and its signing subkey.  
- Custody of the EV Code Signing private key and renewal of the corresponding certificate.  
- Maintenance of the offline revocation certificate for the primary key.  
- Execution of the procedures defined in [Compromise and revocation](#compromise-and-revocation) and
  in the Authenticode section of this policy.

A deputy custodian should also be designated by the OpenSSL Foundation and the OpenSSL Corporation
directors. The deputy custodian holds an authorisation credential for the primary key, has access to
the offline revocation certificate, and is able to execute the procedures of this policy in the
absence of the custodian. Use of the primary key by the deputy custodian remains subject to the
authorisation requirements of [Storage](#storage).

The custodian and deputy custodian are subject to the vetting and conflict-of-interest requirements
applicable to their engagement with the OpenSSL Foundation or the OpenSSL Corporation.

If both the custodian and deputy custodian are unavailable, the OpenSSL Foundation and the OpenSSL
Corporation directors may designate an acting custodian or additional deputy custodian. Use of the
primary key remains subject to the authorisation requirements of [Storage](#storage).
