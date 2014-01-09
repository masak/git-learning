## Which commands?

**Q: Exactly which commands allow (a) single commit, (b) a range of commits, or
(c) both? For (a) to qualify, the semantics has to be different from that of a
range of commits, i.e. `git log HEAD` is (c), not (a).**

Reason for asking: I just found out that `git revert` accepts a range of
commits, and that intrigues me. Maybe I missed other instances where commands
are more useful by accepting ranges of commits.
