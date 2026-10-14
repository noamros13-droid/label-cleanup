Security Incident Response — Label Cleanup

Last reviewed: 14 October 2026

Label Cleanup is a Jira Cloud app published by Noam Rosen, a sole developer. It runs entirely on Atlassian Forge, operates no external infrastructure, and makes no network requests outside Atlassian. This plan is sized to that reality rather than to a company with a security team.

Scope

This plan covers a security vulnerability or incident affecting the Label Cleanup app, its Forge storage, or the developer accounts used to build and publish it.

1. How an incident reaches us

An incident may arrive by any of these routes, all of which are monitored:

The public support portal: https://noam-dev-1.atlassian.net/servicedesk/customer/portals
The Atlassian Ecosystem support ticket system, including Marketplace security notifications
The Atlassian Marketplace Security Bug Bounty programme, if and when the app is enrolled
Direct observation: a Forge platform alert, an unexpected result in the app's own verification step, or a pattern of failed jobs

The security contact is the developer, who holds an account on ecosystem.atlassian.net and receives notifications from the routes above.

2. Triage, within one business day of becoming aware

On receiving a report, the developer:

Acknowledges receipt to the reporter.
Reproduces the issue on a development Jira site, never on a customer site.
Assigns a severity using Atlassian's severity definitions for Marketplace apps.
Records the report, the reproduction steps, the severity and the date.

If the report concerns customer data, the developer does not access any customer site to investigate. Forge gives the app no standing access to customer data outside a user-initiated action, and that boundary is not crossed during an investigation.

3. Containment

In order of preference:

Ship a fix. For most defects in a Forge app this is the fastest route, since a new version deploys without customer action.
Disable the affected capability. The app's single destructive operation is gated behind a preview and a typed confirmation; the removal step can be disabled in a patch release while a fix is prepared.
Withdraw the version. Make the affected version private on the Marketplace so that no new installations occur.

Because the app runs on Forge with no external servers, there is no infrastructure to isolate, no hosting credentials to rotate, and no logs held outside Atlassian.

4. Remediation timeframes

Fixes are delivered within the timeframes set out in Atlassian's Marketplace security bug fix policy for the assigned severity.

That policy, not this document, is the authority on those deadlines. This plan deliberately does not restate them, so that it cannot drift out of date against the policy it is meant to follow.

5. Notification
Atlassian is notified through the Ecosystem support portal as soon as a security issue is confirmed, and before any public disclosure.
Affected customers are notified using Atlassian's app vulnerability notification template.
Notification states what happened, which versions are affected, what a customer must do, and what has already been done.

If customer data may have been exposed, notification happens regardless of whether exposure is confirmed, and before the investigation is complete rather than after.

6. Verification and closure

A fix is not complete until:

The original reproduction no longer reproduces
An automated test covering the defect exists and has been seen to fail against the unfixed code
The released version is confirmed installed and working on a test site
7. After the incident

Within one week of closure, the developer records what happened and when, how it was detected and how it should have been detected, and what changed in the code, the tests, or this plan.

8. Review

This plan is reviewed, and its last-reviewed date updated, whenever an incident occurs and at least every six months. A plan whose review date is stale is treated as unverified rather than as current.

Contact

Security reports: through the support portal above, or the Atlassian Ecosystem support ticket system.

Email: noamrosen93@gmail.com
