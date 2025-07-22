# Release Announcement

This workflow sends a Slack notification when a new GitHub release is published.

## Workflow File
Path: `.github/workflows/release_announcement.yml`

## Slack Setup

**In Slack:**  
Slack app →  
More (…) →  
Automations →  
Workflows →  
Create a workflow →  
Choose event → 
From a webhook →  
Set up variable names and types *(based on the payload from your GitHub Action set in yml file, e.g., `release_version`, `release_notes`: any variables you would like to use in Slack workflow notification)* →  
Name and Save the workflow →  
Open the workflow again →  
Copy Web request URL

Set up next step → 
Send a message to channel (select channel) →
Draft a message template that will be sent in the channel (use variables to populate data).

**In GitHub:**  
Go to Settings → 
Secrets and variables → 
Actions →  
Add a new secret named **`SLACK_WEBHOOK_URL`** with the URL copied from Slack.

## Result
When a release is published, a Slack message like the one below is sent:

![Slack Notification](https://github.com/sakalova/github-actions-lab/images/release-announcement.png)

