# michaKFromParis/syncfork

Keep your git forks in sync with upstream remotes without headaches 

![](www/img/syncfork.jpg)

# Why ?

- You start forking a project and hack into it, commit, push, **happy**.
- The original project developped a cool feature you want to sync into your fork
- **headache**


## Usage

Edit syncfork.conf at the root of your repository

``` bash
source <(curl -s curl https://raw.github.com/michaKFromParis/syncfork/syncfork)
```

## Configuration

Edit **syncfork.conf** at the root of your repository to define the following variables:

``` bash
upstreamUrl='https://github.com/[UPSTREAM_USERNAME]/[UPSTREAM_REPOSITORY]'
upstreamBranch='master'
forkUrl='https://github.com/[FORK_USERNAME]/[FORK_REPOSITORY]'
forkBranch='master'
squashCommits=true
conflictEditor='tower'
```
**upstreamUrl**: The original url of the repo you forked and want to sync

**upstreamBranch**: The branch you want to merge into your repo

**forkUrl**: The url of your forked repo

**forkBranch**: The branch you want new changes to be synced into

**conflictEditor**: The editor you want to call in case of a merge conflict

--

**Warning!!** Do not add spaces around the **=** sign or the script won't work!

The urls used point to github but there's nothing specific to github.

Any valid remote url will work

# Contributing

If you find this script useful here's how you can help:

- Send a Pull Request with your awesome new features and bug fixes
- Help new users with [Issues](https://github.com/michaKFromParis/syncfork/issues) they may encounter

# Licence

MIT Licence. See [Licence](LICENCE)

# Reference

github [official instructions](https://help.github.com/articles/syncing-a-fork/)
