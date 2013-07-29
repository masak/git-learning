Created on 2005-04-14. Quickly removed again on 2005-04-16, apparently
superseded by the better staging area merging.

Revived as a complete rewrite on 2006-02-14, with no apparent connection to the
old command, except for the name. See 492e0759bfe4ff238b80ab80c27291ab99e4512b
with an interesting commit comment. This seems to be the origins of "recursive
merge".

Bumped up to a builtin on 2010-01-21.

Outputs the result of three-way merge between three tree objects. Note,
"outputs" as in standard output; higher-level tools are meant to take this
result and stuff it back into the staging area.
