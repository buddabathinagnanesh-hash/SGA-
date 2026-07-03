# Question 5 Explanation

- lsblk: Listed block devices and their mount points to identify available storage hardware.
- mount | head -5: Showed mounted filesystems, including overlay, proc, tmpfs, devpts, and sysfs.
- df -h: Reported disk usage for mounted filesystems in human-readable format.
- df -i: Reported inode usage to check for potential inode exhaustion.
- Observed that `/dev/root` is at 81% usage and overlay is at 33%, while inode utilization remains low.
- Recommended monitoring root filesystem usage and cleaning unused files to improve storage health.
