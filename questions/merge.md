## merge conflicts

**Q: How are unmerged files represented?**

Guess: They're stored in the staging area somehow.

Answer: Basically, two bits. The data structure `cache_entry` gets the new
flags in f5cabd13d814bb5c547a13af03bcc42122531141, then a new error message in
c347ea5d6fc6bae6b6ea3196013c4df7ec4406a8, and then decorating the staging area
with them in d99082e0e3436f5fcf259aa1a4189473f6bb5ce3.
