Label Cleanup for Jira Cloud

Remove one unwanted label from Jira issues safely. Preview first, confirm, then remove. Nothing else changes.

What it does

Jira label lists accumulate mistakes: typos, abandoned conventions, labels left over from a migration. Removing one of them across hundreds of issues normally means editing issues one at a time, or running a bulk change you cannot review first.

Label Cleanup does one job. It removes a single label from the issues that carry it, after showing you exactly what will change.

Requirements
Jira Cloud
Jira administrator permission (checked on every action)
How to use it
1. Open the app

Go to Jira settings → Apps → Label Cleanup.

2. Find the label

Enter the exact label, including capitalisation. Matching is exact, never partial or fuzzy — deprecated-2024 will not match Deprecated-2024.

Optionally enter a project key to limit the search to one project. Leave it blank to search every project you can browse.

Select Preview matches.

Nothing is modified in this step. The app reports how many issues carry the label and saves the matched list as a snapshot.

3. Review

Check the saved preview. Only issues captured in that snapshot can be changed — matches created after the preview are not included.

4. Remove

Tick the confirmation box and type the label name exactly to enable the remove button.

The app removes the label from each issue, then reads the issue back to confirm the label is gone. Each issue is reported as:

Result	Meaning
Removed	Jira accepted the change and a follow-up read confirmed the label is absent
Already absent	The label was no longer on the issue when the job ran
Needs review	The change could not be completed or could not be verified

Select Export CSV for the full result.

Limits
Up to 2,000 matching issues per job. Run several jobs for larger cleanups.
Jobs resume if interrupted.
One job runs at a time per site.
What it does not do
It does not modify other labels on the same issue
It does not modify any other field
It does not delete issues
It does not perform partial, fuzzy or case-insensitive matching
Important

Label removal is permanent. Jira provides no mechanism for this app to restore a removed label. This is why the preview and the typed confirmation exist — review the preview before confirming.

Removing a label may trigger Jira notifications, automation rules and issue history entries. These are Jira behaviours and are outside the app's control. If you have automation rules or filters that depend on the label, check them before running a cleanup.

Permissions and data

The app requests three scopes and no more:

Scope	Used for
read:jira-work	Searching issues, reading labels and project, checking admin rights
write:jira-work	Removing the label from an issue
storage:app	Saving jobs, locks and usage counts in Forge storage

All Jira requests run as the signed-in user, and every action verifies Jira administrator permission first. The app can never change more than that user is already permitted to change.

The app runs entirely on Atlassian Forge. It declares no external hosts and makes no calls outside Atlassian. No data is sent to the vendor or to any third party.

Privacy policy
Terms of service
Troubleshooting

No matches found. Check capitalisation — matching is exact. If you set a project key, confirm the label exists in that project.

Some issues show "Needs review". You may not have permission to edit those issues, or Jira rejected the change. The CSV export lists each one.

The job is taking a long time. Larger jobs take proportionally longer. The progress indicator shows issues processed. The job resumes if interrupted.

Support

Email: [noamrosen93@gmail.com]

Monday to Friday, 9:00am–5:00pm AEST (UTC+10). Response within 2 business days.
