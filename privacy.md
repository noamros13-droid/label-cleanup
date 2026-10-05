Privacy Policy — Label Cleanup

Last updated: 5 October 2026

Label Cleanup ("the app") is a Jira Cloud app published on the Atlassian Marketplace by Noam Rosen ("we", "us").

This policy explains what the app accesses, what it stores, and what it does not do.

What the app does

Label Cleanup finds Jira issues carrying a specific label and removes that label from them, after an explicit preview and typed confirmation by a Jira administrator.

Where the app runs

The app runs entirely on Atlassian's Forge platform, inside Atlassian's own cloud infrastructure. It does not operate any external servers.

Data the app accesses

To perform its function, the app reads:

Issue keys, labels and project keys for issues matching a label you specify
Your Jira permissions, to confirm you are an administrator before any change is made

All Jira requests are made as the signed-in user. The app can never access or change anything that user is not already permitted to access or change.

Data the app stores

The app stores the following in Atlassian Forge storage, within your Atlassian site:

Cleanup job records: the label searched, the issue keys matched, job status and results
Job locks, to prevent two cleanup jobs running at once
Anonymous usage counts and timings, used to operate and support the app
Data the app does not collect

The app does not collect, store or process:

Issue summaries, descriptions, comments or attachments
Names, email addresses or user profile information
Any personal data as defined under the Australian Privacy Act 1988, the GDPR or equivalent legislation
Data transfers

The app makes no network requests outside Atlassian. No external hosts are declared in its manifest and no data is transmitted to us, to any third party, or to any analytics, advertising or tracking service.

We do not have direct access to your Jira data.

Data retention

Job records are retained in your site's Forge storage so you can review past cleanup jobs. Uninstalling the app removes its Forge storage, subject to Atlassian's deletion timelines — Atlassian documents that physical deletion may lag the deletion request by up to 48 hours.

You may request deletion of job records at any time by contacting support.

Sub-processors

The app's only infrastructure provider is Atlassian, which hosts the Forge runtime and storage. We engage no other sub-processors.

Security

The app requests the minimum permission scopes required to function: read:jira-work, write:jira-work and storage:app. It requests no additional scopes. All operations verify administrator permission before executing, and every label removal is verified by a follow-up read.

Changes to this policy

Material changes will be reflected in the "Last updated" date above and, where appropriate, noted on the app's Marketplace listing.

Contact

Questions about this policy or about data handling:

[noamrosen93@gmail.com]
