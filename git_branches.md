# My Git Branching Model

This is almost completely based on [this post](http://nvie.com/posts/a-successful-git-branching-model/).

## Main Branches

### master Branch

* Must be named "master". This is the default branch when creating a new repository.
* This branch is the branch of stable releases for the major version in active development.
* Work must never be done on this branch.
* All commits on this must be tagged with a new version number.

### develop Branch

* Must be named "develop".
* This branch is where active development takes place.
* Work should not be done directly in this branch.
* This branch should be created from the master branch and should run parallel
    to the master branch for the duration of the project.

## Supporting Branches

### Hotfix branches

* Must be named with a prefix of "hotfix-". The bug number in your tracking system can be the second
    part of the name.
* This branch is where immediate fixes take place.
* This branch should be created from the master branch and have a short life.
* After the work is complete, this branch will be merged back into its source.
* It will likely need merged into other branches as well - develop and posibly feature branches.
    It is up to the developer's discression to determine if it will affect a feature branch
    and should be merged.
* Don't forget to bump the master branch's version!

### Feature branches

* Can have any name that isn't reserved (e.g. develop, hotfix-*).
* This branch is where features will live during development.
* This branch should be created from the develop branch.
* This branch will run in parallel with the develop branch and can have either
    a short or long life.
* This branch will be merged back into its source; this should occur after the feature is complete.

### Release branches

* Must be named "release-" followed by the new version number (e.g. release release-2.1).
* This branch is a proxy between develop and master. After the develop branch becomes release ready, it
    moves to this branch to be finalized before merging into master.
* This branch is created from the develop branch and lives until it's determined stable for production.
* Any feature branches that have not been merged back into develop at this time will have to wait
    until a future release occurs.
* This branch will merge into master.
* Don't forget to bump the master branch's version!