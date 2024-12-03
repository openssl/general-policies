# Security Policy

## Reporting security issues

If you wish to report a possible security issue in OpenSSL please
[notify us](/community/#reporting-security-bugssecurityreports).

## Issue triage

Notifications are received by the OMC and OTC. We engage resources within
OpenSSL to start the investigation and prioritisation. We may work in
private with individuals who are not on the OMC or OTC as well as other
organisations and our [employers](/community/thanks/)
where we believe this can help with the issue investigation, resolution, or
testing.

## Threat Model

Certain threats are currently considered outside of the scope of the
OpenSSL threat model. Accordingly, we do not consider OpenSSL secure
against the following classes of attacks:

 - same physical system side channel
 - CPU/hardware flaws
 - physical fault injection
 - physical observation side channels (e.g. power consumption,
   EM emissions, etc)

Mitigations for security issues outside of our threat scope may still be
addressed, however we do not class these as OpenSSL vulnerabilities and
will therefore not issue CVEs for any mitigations to address these issues.

We are working towards making the same physical system side channel attacks
very hard.

Prior to the threat model being included in this policy, CVEs were sometimes
issued for these classes of attacks. The existence of a previous CVE does
not override this policy going forward.

## Issue severity

We will determine the risk of each issue, taking into account our experience
dealing with past issues, versions affected, common defaults, and use cases.
We use the following severity categories:

 - <a name="critical">**CRITICAL**</a> Severity. This affects common
   configurations and which are also likely to be exploitable. Examples
   include significant disclosure of the contents of server memory
   (potentially revealing user details), vulnerabilities which can be easily
   exploited remotely to compromise server private keys or where remote code
   execution is considered likely in common situations. These issues will be
   kept private and will trigger a new release of all supported versions. We
   will attempt to address these as soon as possible.
 - <a name="high">**HIGH**</a> Severity. This includes issues that are of a
   lower risk than critical, perhaps due to affecting less common
   configurations, or which are less likely to be exploitable. These issues
   will be kept private and will trigger a new release of all supported
   versions. We will attempt to keep the time these issues are private to a
   minimum; our aim would be no longer than a month where this is something
   under our control.
 - <a name="moderate">**MODERATE**</a> Severity. This includes issues like
   crashes in client applications, flaws in protocols that are less commonly
   used (such as DTLS), and local flaws. These will in general be kept
   private until the next release, and that release will be scheduled so
   that it can roll up several such flaws at one time.
 - <a name="low">**LOW**</a> Severity. This includes issues such as those
   that only affect the openssl command line utility, or unlikely
   configurations. These will in general be fixed immediately in latest
   development versions, and may be backported to older versions that are
   still getting updates. We will update the vulnerabilities page and note
   the issue CVE in the changelog and commit message, but they may not
   trigger new releases.

## Prenotification policy

 - Where we are planning an update that fixes security issues we will notify
   the [openssl-announce list](https://groups.google.com/a/openssl.org/g/openssl-announce/)
   and update the OpenSSL website to give our scheduled update release date
   and time and the severity of issues being fixed by the update. No further
   information about the issues will be given.
 - Where we are planning an update that include CRITICAL, HIGH, or MODERATE severity
   issues we will also prenotify certain organisations with more details
   and patches.
   - The organisations we prenotify include those that produce a general
     purpose OS that uses OpenSSL as included on [this list of Operating
     System distribution security contacts](http://oss-security.openwall.org/wiki/mailing-lists/distros).
   - We also include other open source projects that are derived from OpenSSL
     which have a significant user base and a reciprocal arrangement.
   - We may also include other organisations that are not listed but would
     otherwise qualify for list membership.
   - We may also include organisations with which we have a commercial
     relationship.
   - We may withdraw notifying certain organisations from future
     prenotifications if they leak issues before they are public or over time
     do not add value.

Note: researchers or intermediaries who notify us of issues may have their
own prenotification policy in addition to ours.

## Principles

The policy above is guided by our security principles:

 - It's in the best interests of the Internet as a whole to get fixes for
   OpenSSL security issues out quickly. OpenSSL embargoes should be measured
   in days and weeks, not months or years.
 - Many sites affected by OpenSSL issues will be running a version of OpenSSL
   they got from some vendor (and likely bundled with an operating system).
   The most effective way for these sites to get protected is to get an
   updated version from that vendor.
