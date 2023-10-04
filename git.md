https://myopswork.com/how-remove-files-completely-from-git-repository-history-47ed3e0c4c35?gi=3e7e5af69d2d

## Undo a git add before a commit

Run `git reset <file>` or `git reset` to unstage all changes.

In older versions of git, the commands were git reset HEAD <file> and git reset HEAD respectively. This was changed in Git 1.8.2

## Dealing with a diverging branch and re-syncing

fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:ref/heads/main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.
FAIL: 128

`$ git push origin HEAD`
