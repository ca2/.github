### Symbolic links maybe be broken...

A symbolic link may be broken when it's just a file containing a path to the original file/folder, instead of actually a symbolic link to it.

- Enable Developer Mode for Windows at Developer Settings (If you havent't done so yet).


To fix them in the git repository, at Git bash.
```bash
cd $HOME/code/simple
repair-git-symlinks
```

If you have Tortoise Git installed, you can use it for restoring symbolic links: [windows-repair-git-symlinks-with-tortoise-git.md](windows-repair-git-symlinks-with-tortoise-git.md)
