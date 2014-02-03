## Orphaned branches

**Q: When checking out an orphaned branch, how does the branch "remember" to
make the next commit with no parents?**

    <masak> ooh, `git checkout --orphan`
    <masak> "The first commit made on this new branch will have no parents and it will be the root of a new history totally 
            disconnected from all the other branches and commits."
    <masak> waitwait... so, where is that information stored between the checkout and the subsequent commit?
    * masak adds that to his growing list of questions in git-learning

**Guess:** I found something in `builtin/merge.c` called "empty head". I
strongly suspect that has something to do with it.

## Sparse checkout

**Q: What is a sparse checkout?**

**Hint:** Sparse checkout can be used to restrict which files/folders are
updated with all checkout and status operations. It cannot change the tree the
checkout is rooted from. See man git-read-tree.
