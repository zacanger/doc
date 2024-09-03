# security

Sec is important, but hard. How do you keep your stuff in the clear?

## Pass

Pass is the unix password manager. Even though files are not stored as a binary
blob (ergo service names are retrievable), it's pretty much the best thing out
there. It's built on gpg and other unix tools, providing a neat interface for
local passwords. Use it.

## Hardware pgp management

The yubikey NEO is a hardware device to store your pgp keys. Unless it's
physically retrieved it cannot be read. Combine it with pass for maximum
security.

