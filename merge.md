Merge Examples

To merge other_branch into branch, you should check out the target branch and merge the other branches into it, like this:

    $ git checkout branch
    $ git merge other_branch

Preparing for a Merge

Before you begin a merge, it’s best to tidy up your working directory. During a normal merge, Git creates new versions of files and places them in your working directory when it is finished. Furthermore, Git also uses the index to store temporary and intermediate versions of files during the operation.

If you have modified files in your working directory or if you’ve modified the index via git add or git rm, your repository has a dirty working directory or index. If you start a merge in a dirty state, Git may be unable to combine the changes from all the branches and those in your working directory or index in one pass.












