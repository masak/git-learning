## merges

**Q: What does reverting a merge do? Does it work? Is it a good idea?**

Guess: It uses the first parent of the commit as its "base", just like ordinary
non-merge commits. All the other parents make up the diff of what should be
reverted.

Answer: You must provide `-m 1` (for the first parent) for it to revert the
merge. Then it works as in the guess. But note that subsequent merges will
still consider the branch to have been merged, even though the changes have
since been reverted. (I.e. the *history* remains the same.) See
https://www.kernel.org/pub/software/scm/git/docs/howto/revert-a-faulty-merge.txt
for more detail.
