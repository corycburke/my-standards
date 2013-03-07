# My Git Workflow

This is to define how I use git for my projects.

## Create an empty repository on the server.

If you are using github, there's plenty of documentation on that. If you are just
using a server, here's how to do that.

1. ssh into the sever and navigate to the directory you want to create your repository.
2. Create a new directory suffixed with .git. `mkdir my_project.git`
3. Change to that directory. `cd my_project.git`
4. Create your empty repository. `git init --bare --shared`