# Question 4 Explanation

- rm -f app.log stdout.txt stderr.txt combined.txt: Removed stale files from the working directory.
- echo "sample log line" > app.log: Created a sample log file for I/O testing.
- lsof | head -n 20: Listed currently open files on the system to observe active file handles.
- exec 3<app.log: Opened `app.log` on file descriptor 3 to demonstrate file descriptor usage.
- lsof -p $$ | grep app.log: Confirmed the shell process had `app.log` open on descriptor 3.
- ls -l /proc/$$/fd | grep app.log: Checked the process file descriptor directory for the opened log file.
- ls -l /proc/$$/fd: Listed all open file descriptors for the current shell.
- ls -l > stdout.txt: Redirected standard output to a file.
- ls /not_a_real_path 2> stderr.txt: Redirected error output to a separate file when the command failed.
- (ls -l && ls /not_a_real_path) > combined.txt 2>&1: Redirected both standard output and error output together.
- ulimit -a: Displayed current shell resource limits including open file limits.
- exec 3<&-: Closed file descriptor 3 to release the open file handle.
