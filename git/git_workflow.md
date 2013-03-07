# My Git Workflow

This is to define how I use git for my projects.

## Create an empty repository on the server.

If you are using github, there's plenty of documentation on that. If you are just
using a Linux server, here's how to do that.

1. ssh into the sever and navigate to the directory you want to create your repository.
2. Create a new directory suffixed with .git. `mkdir my_project.git`
3. Change to that directory. `cd my_project.git`
4. Create your empty repository. `git init --bare --shared`

## Set up your repository on your local machine.

If you are starting out fresh, you can just clone the new empty repository to your
local machine:

1. Navigate to the directory where you want your new project to be.
2. Clone the empty repository. `git clone user@domain:path/to/repository.git local_dir`
    * Git will probably inform you that you've cloned an empty repository, which you
        already knew.
3. Get to work on your new project.

If you already have files that you want to add to the repository, follow these steps:

1. Navigate to the directory where your project lives.
2. Initiate a new git repository there. `git init`
3. If needed, create your .gitignore file at this time. You can use one of the samples included.
4. Add your files to the repository. `git add .`
5. You can run `git status` at this point to make sure everything looks good.
6. Make your first commit. `git commit -m "Initial commit"`
    * If you haven't committed anything using git yet, you will probably be asked to
        set your username and email at this time. Just follow the directions.
7. Add your remote. `git remote add origin user@domain:path/to/repository.git`
8. Push your new repository to the server. `git push`