# GitHub_Jira_KEY_integration
Hooks for inserting the JIRA Issue key into commits automatically from feature-branch name

Add these two hook files into the .git directory of your repository. Then, if you are working on a feature branch which contains the JIRA issue key (e.g: feature/JIRA-123, or JIRA-123, or JIRA-123/feature,...), they will prepend the issue key betwwen [] (i.e.: [JIRA-123]) to the message.

Example:

1) If you write:

git commit

The prepare-commit-msg hook will run, and the message editor that you use will already show you the issue key, and you can write your message there.
Then, the commit-msg hook will also run, and check again if the issue key is still there.


2) If you write:

git commit -m "YOUR MESSAGE"

The commit-msg hook will run, and it will prepend the issue key to you message, so the final message her would be: "[JIRA-123] YOUR MESSAGE"
