# Question 1 Explanation

- whoami: Verified the current user account is `codespace`.
- groups: Confirmed the groups associated with the account include development-related groups such as `docker` and `python`.
- echo "$SHELL": Checked that the current shell is `/bin/bash`.
- pwd: Confirmed the current working directory is `/workspaces/SGA-`.
- ls -ls: Listed the files and directories in the current workspace to verify contents.
- curl -s --max-time 10 https://facebook.com > /dev/null && echo "Network: facebook.com reachable": Tested network connectivity and confirmed external access was successful.
