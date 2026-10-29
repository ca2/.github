### If symbolic links are broken...

A symbolic link may be broken when it is just a file containing a path to the original file/folder, instead of actually a symbolic link to it.

1. Enable Developer Mode for Windows at Developer Settings (If you havent't done so yet).
2. Install Tortoise Git

[https://tortoisegit.org/](https://tortoisegit.org/)

4. Delete folder <root-project-folder>\port\include
5. Right click <root-project-folder>\port folder in File Explorer and click Revert option in Tortoise Git Context Menu Sub Menu
6. At Tortoise Git Revert Screen, select check every item in the list (there is a Check all check box) and then click Revert.

When reverting using Tortoise Git, symbolic links are recreated and selected files are restored.

