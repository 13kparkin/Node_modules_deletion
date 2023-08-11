
# Node Modules Cleanup Script
Delete all node_modules found in a Directory:
NOTE: Use caution here, and make sure that you are in a directory where you’re comfortable removing all the instances of node_modules, run the script above to see a full list of them all before deleting.

This script is actually very similar to the one above, but we’re going to be utilizing rm -rf to completely delete them.

WARNING: This process is irreversible!

Mac / Linux:
$ cd documents 
$ find . -name "node_modules" -type d -prune -exec rm -rf '{}' +
Windows:
$ cd documents 
$ FOR /d /r . %d in (node_modules) DO @IF EXIST "%d" rm -rf "%d"
