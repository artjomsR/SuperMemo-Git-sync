# SuperMemo-Git-sync
A bat script to automatically sync your SuperMemo collection (across multiple devices)

**NB:** This script assumes you're using git to backup your SuperMemo collection, as outlined in https://supermemo.wiki/sma/#/qs-backup-setup?id=internet-backups-git-amp-github

Upon launching, this script will:
1. Get the latest copy of your SM collection from git
2. Prompt to Launch SM
3. Once SM is closed, it will prompt to save your collection to git

# Setup
1. Download the .bat script
2. Place the script in your git folder together with your SM collection
3. Right click on the .bat script and click Send to > Desktop
4. On your desktop, Right click on the newly created shortcut and click Properties
5. In the Target field, append the drive letter, where SM is currently installed. Make sure there's a space in-between the existing string and the newly added drive letter
5.1 E.g. for me, SM is installed on drive **E** 
5.2 So, I would change the value in the Target field: `"D:\SuperMemo_Collection\Start & sync SM.bat"` to `"D:\SuperMemo_Collection\Start & sync SM.bat" E`
6. Press OK on the Properties window
7. Optional: if you were using a shortcut to run SM, you can delete it

# How to use
- Use this script instead of the normal SuperMemo shortcut - it will ensure you have the latest copy of your collection before you start working on it and will update the latest copy when you're finished.
- This is especially true for multiple computers: if you setup this script on multiple PCs then you don't need to worry about having the latest copy of your collection. As long as you only run this script (and not SM directly) then you can always pick up where you left off at any of your workstations

# Notes
- This script is nothing too complicated - you can see that it's a few git commands to sync the collection, mixed in with a few readable prompts. I've used it myself for ~1.5 months+ as of the writing of this readme file. Still, I can't hold any responsibility if something goes horribly wrong - use at your own risk and all that.
- The script supports installation of SM on different drives, but non-default installation paths are not supported at the moment. E.g. SM must be installed at `X:\SuperMemo\` 
- Any questions - let me know, and I'll try to do a better write up/explain
