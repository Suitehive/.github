# Security policy

Suitehive handles people's email, calendars and accounts, so we take security reports seriously.

## Reporting a vulnerability

**Please don't open a public issue for security problems.**

Report it privately through GitHub instead:

1. Go to the affected repository (if you're unsure, use [suitehive](https://github.com/Suitehive/suitehive)).
2. Open the **Security** tab and choose **Report a vulnerability**.
3. Describe the issue, how to reproduce it, and the impact you expect.

We'll acknowledge your report within **3 working days** and keep you updated until it's resolved.
Once a fix is released, we're happy to credit you unless you'd rather stay anonymous.

## Supported versions

Suitehive is in early development and has no stable release yet. Security fixes go to the `main`
branch of each repository.

## Scope

In scope: the Suitehive services (auth, mail, calendar), the shared libraries (kit, contracts, ui),
the installer and CLI, and the default deployment templates.

Out of scope: vulnerabilities in third-party software we depend on (please report those upstream),
issues that need physical access to a server, and denial-of-service through sheer traffic volume.
