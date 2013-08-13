## Comments

**Q: How can I enter lines in the editor so they get included in the commit
comment, even though they happen to start with an octothorpe (`#`)?**

Answer:

    <masak> is there a way to use $EDITOR, begin some lines with '#' and still have them be part of the commit message?
    <lb1a> masak, since the git commit tells you explicitly : "Lines starting with '#' will be ignored, and an empty message 
           aborts the commit." no, you can't
    <fdel> masak: see commit.cleanup configuration variable (or git commit --cleanup option)
    <masak> fdel: ooh
    <fdel> masak: but then don't forget to remove all the auto-generated # comments yoursef
    <masak> fdel: right.
    <masak> fdel++
    <fdel> masak: or set core.commentchar to another character
    <fdel> masak: available since 1.8.2, so maybe core.commentchar isn't available for you, depending on your git version
    <masak> fdel: awesome. thanks.
