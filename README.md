# Dropbox Certificate Pins

This repository contains the complete list of Dropbox's certificate pins,
which are used inside Dropbox's file sync & share clients
to restrict which certificate authorities are trusted.

Dropbox does not recommend that application developers use certificate
pinning inside their third-party applications, as it is difficult
to maintain updates to the pinset and because end-users can experience
outages if their applications are not updated to the latest pinsets.
Instead, developers should rely on their operating system or programming
language's built-in certificate validation mechanisms.

Nevertheless, we continue to provide our pinset for reference, for
application developers who have users with particularly sensitive security
needs.

## Pinsets

There are two sets of pinsets provided:

* `pinned_roots` contains each individual root certificate pin, in PEM
   format
* `trust_stores` contains compiled pinsets, in various formats
  * `pinned_roots.pem` contains the pinset in concatenated PEM format
  * `pinned_roots.pfx` contains the pinset in PKCS #12 format
  * `pinned_roots.bks` contains the pinset in Bouncy Castle's BKS format