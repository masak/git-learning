## renames with content changed

**Q: Git can trivially recognize the same blob anywhere, and quickly recognize
and flag moves. But how the heck does it track a moved file *whose contents
also changed*? This seems very magical.**

Guess: I suppose diffing is involved somehow. But it still feels like it would
be expensive &mdash; as in O(files**2) &mdash; to diff all removed files
against all added files, just to check if they're alike enough.
