A very early command. Created on 2005-04-11. Retired by Junio on 2005-09-16.

It "calculates the revision tree graph", basically performing a depth-first
search of the complete commit history starting from some given commit. It
prints each commit it finds along with all its parents.

Crucially, the `tree` part of the name of this tool has nothing to do with tree
objects. It refers to the DAG structure commits form through their parent
links.

This was the command that first introduced the syntax `^<sha1>` to mean
"exclude all commits reachable from `<sha1>`", in a patch by David Woodhouse.
