letsrenew
=========

A set of very small shell scripts for Certbot renewals.

Usage:

1. Install [Certbot][], register some certificates
2. Clone this repository, add hook scripts
3. Run `letsrenew`

  [Certbot]: https://github.com/certbot/certbot

Running letsrenew
-----------------

With `letsrenew` installed in `/opt/letsrenew` and Certbot installed in
`/opt/certbot` (for example):

    /opt/letsrenew/letsrenew foo@example.com /opt/certbot/certbot-auto

The Certbot executable may be followed by additional Certbot options.

The output of all scripts will be mailed to `foo@example.com` using `sendmail`.
If you leave out the email address, the output will be printed on the console.

Hook scripts
------------

Executable files in `pre-scripts` and `post-scripts` will be executed by
their respective hook.

Executable files in `renew-scripts` will be executed if their name matches a
domain that has been renewed.
