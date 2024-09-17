https://myopswork.com/how-remove-files-completely-from-git-repository-history-47ed3e0c4c35?gi=3e7e5af69d2d

## Undo a git add before a commit

Run `git reset <file>` or `git reset` to unstage all changes.

In older versions of git, the commands were git reset HEAD <file> and git reset HEAD respectively. This was changed in Git 1.8.2

## Removing a file/directory from git without deleting it.
A file/directory (e.g. tmp) has been added to .gitignore but still shows in `git status`

`git rm -r --cached tmp`

## Dealing with a diverging branch and re-syncing

fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    `git push origin HEAD:ref/heads/main`

To push to the branch of the same name on the remote, use

    `git push origin HEAD`

To choose either option permanently, see push.default in 'git help config'.

`$ git push origin HEAD`

## ECSA key error connecting to github.com

Remove the key:

`sed -i -e '/AAAAB3NzaC1yc2EAAAABIwAAAQEAq2A7hRGmdnm9tUDbO9IDSwBK6TbQa+PXYPCPy6rbTrTtw7PHkccKrpp0yVhp5HdEIcKr6pLlVDBfOLX9QUsyCOV0wzfjIJNlGEYsdlLJizHhbn2mUjvSAHQqZETYP81eFzLQNnPHt4EVVUh7VfDESU84KezmD5QlWpXLmvU31\/yMf+Se8xhHTvKSCZIFImWwoG6mbUoWf9nzpIoaSjB+weqqUUmpaaasXVal72J+UX2B+2RPW3RcT0eOzQgqlJL3RKrTJvdsjE3JEAvGq3lGHSZXy28G3skua2SmVi\/w4yCE6gbODqnTWlg7+wC604ydGXA8VJiS5ap43JXiUFFAaQ==/d' ~/.ssh/known_hosts`
