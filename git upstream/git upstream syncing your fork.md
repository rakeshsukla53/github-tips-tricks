forking does not automatically stay sync up, you have to do manually. See the diagram

![link](https://github.com/rakeshsukla53/github-tips-tricks/blob/master/git%20upstream/git%20upstream%20view.png)

`upstream`  is basically the repository which we have forked 

Now see this picture
![link](https://github.com/rakeshsukla53/github-tips-tricks/blob/master/git%20upstream/fetch%20and%20merge%20upstream%20example.png)
you can fetch from the upstream repository and then merge on your local computer. Then push to `github repo`

== COMMAND LIST ==

    show your remotes: git remote -v
    add an upstream remote: git remote add upstream [URL]
    fetch changes from the upstream: git fetch upstream
    merge those changes into your repo: git merge upstream/master
    push those changes to the origin: git push origin master

