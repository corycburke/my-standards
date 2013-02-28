# My Git Branching Model

This is almost completely based on [this post](http://nvie.com/posts/a-successful-git-branching-model/).

## master Branch

* This branch is the branch of stable releases for the major version in active development.
* Work must never be done on this branch.
* All commits on this must be tagged with a new version number.

## develop Branch

* This branch is where active development takes place.
* Work should not be done directly in this branch.
* This branch should be created from the master branch and should run parallel
    to the master branch for the duration of the project.