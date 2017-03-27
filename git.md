# Git commands 
---

* Adding a remote `git remote add origin protocl@repo`
* Listing remotes `git remote -v`
* Setting url of remote `git remote set-url remotename remoteuri`
* Setting email `git config user.email emailadd@domain.tld`
* Setting user `git config user.name username`
* Pull a specific branch: `git pull -b branch_name remote_uri`
* Delete a wrong commited tag, f.e. tag1: `git tag -d tag1` and `git push origin :refs/tags/tag1`
* Create a csv from git commit log: `git log --date=iso --pretty=format:"%h%x09%an%x09%ad%x09%s"`
