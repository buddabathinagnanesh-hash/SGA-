# Question 2 Explanation

- mkdir -p secure_workspace/{docs,src,logs}: Created a secure project workspace structure with separate directories for documentation, code, and logs.
- touch secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log: Created the required files inside the new workspace.
- ls -ld secure_workspace secure_workspace/*: Verified the directories and their initial permissions.
- chmod 750 secure_workspace and chmod 750 secure_workspace/docs secure_workspace/src secure_workspace/logs: Adjusted directory permissions so only the owner has full access and the group can read/execute.
- chmod 640 secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log: Attempted to restrict file permissions, but the command failed for `activity.log` due to a filename typo.
- ls -l secure_workspace/*: Verified final permissions of each file and confirmed `plan.txt` and `app.txt` are protected.
- umask: Checked the default file creation mask of `0022` to understand how new file permissions are determined.
