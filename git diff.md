    $ git merge alternate
    Auto-merged file
    CONFLICT (content): Merge conflict in file
    Automatic merge failed; fix conflicts and then commit the result.

When a merge conflict like this occurs, you should almost invariably investigate the extent of the conflict using the git diff command. Here, the single file named file has a conflict in its content:

    $ git diff
    diff --cc file
    index 4d77dd1,802acf8..0000000
    --- a/file
    +++ b/file
    @@@ -2,5 -2,5 +2,10 @@@ Line 1 stuff
      Line 2 stuff
      Line 3 stuff
      Line 4 alternate stuff
    ++<<<<<<< HEAD:file
     +Line 5 stuff
     +Line 6 stuff
    ++=======
    + Line 5 alternate stuff
    + Line 6 alternate stuff
    ++>>>>>>> alternate:file

The git diff command shows the differences between the file in your working directory and the index. In the traditional diff command output style, the changed content is presented between <<<<<<< and =======, with an alternate between ======= and >>>>>>>. However, additional plus and minus signs are used in the combined diff format to indicate changes from multiple sources relative to the final resulting version.

The previous output shows that the conflict covers lines 5 and 6, where deliberately different changes were made in the two branches. It’s then up to you to resolve the conflict. For now, simply edit the file to mirror this content:

    $ cat file
    Line 1 stuff
    Line 2 stuff
    Line 3 stuff
    Line 4 alternate stuff
    Line 5 stuff
    Line 6 alternate stuff