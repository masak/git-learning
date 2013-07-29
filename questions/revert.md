## merges

**Q: What does reverting a merge do? Does it work? Is it a good idea?**

Guess: It uses the first parent of the commit as its "base", just like ordinary
non-merge commits. All the other parents make up the diff of what should be
reverted.
