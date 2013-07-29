## renames with content changed

**Q: Git can trivially recognize the same blob anywhere, and quickly recognize
and flag moves. But how the heck does it track a moved file *whose contents
also changed*? This seems very magical.**

Guess: I suppose diffing is involved somehow. But it still feels like it would
be expensive &mdash; as in O(files**2) &mdash; to diff all removed files
against all added files, just to check if they're alike enough.

Answer: A partial answer can be found
[here](http://blogs.atlassian.com/2011/10/confluence_git_rename_merge_oh_my/):

> By default, git does not attempt to do rename detection even if the
> `diff.renameLimit` is sufficient.Instead to show renames, commands like `git
> show` or `git log` can be used with the `-M[]` option that turns rename detection
> on. Git uses a similarity index and considers a delete/add pair to be a
> rename if more than x % of the file hasn’t changed. By default the threshold
> is *50%*.
>
> Set `git config diff.renames true` to always do rename detection when using
> `git diff/show/log`.
