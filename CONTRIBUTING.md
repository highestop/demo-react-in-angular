## CONTRIBUTING

The origin remote codebase is in our internal GitLab, so first `git remote add github git@github.com:highestop/react-in-angular.git` to add the github remote.

Then `git checkout github:main && git switch -c main && git branch --set-upstream github main` to create a local branch `main` and set its upstream to `github:main`, or run `git push --set-upstream github main` when pushing the code.

If there are other code sources, `git remote add source **` and then `git fetch source && git rebase source/master` to update code from that source, then `git push`. Or checkout `main` and rebase in the same way and do `git push github main`.

```
  main                      // upstream to github/main
* master                    // upstream to origin/master
  remotes/github/main       // my mirror repo on github
  remotes/gitlab/master     // source repo on gitlab
  remotes/origin/HEAD -> origin/master
  remotes/origin/master     // my repo forked on gitlab
```

```
[remote "origin"]
        url = git@gitlab.**.com:chenyn01/react-in-angular.git
        fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
        remote = origin
        merge = refs/heads/master
[remote "gitlab"]
        url = git@gitlab.**.com:zhaojx01/react-in-angular.git
        fetch = +refs/heads/*:refs/remotes/gitlab/*
[remote "github"]
        url = git@github.com:highestop/demo-react-in-angular.git
        fetch = +refs/heads/*:refs/remotes/github/*
[branch "main"]
        remote = github
        merge = refs/heads/main
```

Noted that, this README file is only available on Github, so DO NOT rebase `github:main` on other branches and push them to their sources. That may cause some problems for other people.
