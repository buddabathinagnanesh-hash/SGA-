# Question 3 Explanation

- rm -f original.txt hardlink.txt symlink.txt: Cleaned up any existing test files to start fresh.
- echo "Linux link test file" > original.txt: Created the original file used for link testing.
- ln original.txt hardlink.txt: Created a hard link and observed it shares the same inode as the original file.
- ln -s original.txt symlink.txt: Created a symbolic link that references the original file path.
- ls -li: Checked inode numbers and link details for the original file, hard link, and symbolic link.
- stat original.txt hardlink.txt symlink.txt: Collected metadata to compare permissions, inode numbers, and link counts.
- cat original.txt, cat hardlink.txt, cat symlink.txt: Verified all three paths returned the same file content.
- rm original.txt: Deleted the original file name and tested the impact on hard and symbolic links.
- ls -li after deletion: Confirmed the hard link still existed and the symbolic link became broken.
- cat hardlink.txt and cat symlink.txt after deletion: Verified the hard link preserved file access while the symlink failed.
