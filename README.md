
# Node Modules Cleanup Script
Delete all node_modules found in a Directory:
NOTE: Use caution here, and make sure that you are in a directory where you’re comfortable removing all the instances of node_modules.

This script takes a minute to run as it deletes the directories.

WARNING: This process is irreversible!

Mac / Linux:
```shell
cd documents
```
```shell
find . -name "node_modules" -type d -prune -exec rm -rf '{}' +
```

Windows:
```shell
 cd documents
```
```shell
$ FOR /d /r . %d in (node_modules) DO @IF EXIST "%d" rm -rf "%d"
```
