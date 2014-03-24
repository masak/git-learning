## Overwriting rebase

**Q: What if I'm sure I want to resolve every conflict in a rebase with "prefer
my changes"?**

Use the `theirs` merge strategy option.

    $ git rebase -X theirs master

(Why `theirs`, not `ours`? Because the roles of working branch and upstream
branch are reversed in the rebase case compared to the merge case.)

**Q: Manual says commits are stored away in a "temporary area". Which temporary
area is that?**
