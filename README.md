## Git 

Core concepts to understand: 

1. The basic workflow of adding files to a repository
    - new file ->  add to *staging index*  ->  commit to repository (-> push to remote)
    - adding and removing files from the index, resetting and reverting commits
    
2. Branching and merging
    - Fast-forward and three-way merges, resolving conflicts, rebasing

3. Working with remotes
    - Pushing, fetching and pulling 

4. Git internals 
    - A commit is a hash over metadata of the commit (author, message etc) and a hash of the file tree object 
    - Branches are just pointers to individual commits 
    (Dave Liddament from Bristol PHP training has a good talk on that)

5. Working with Git in a Team 
    - Different branching and deploy strategies (Git Flow)
    (Read Git for Teams by Emma Jane Hogbin Westby!)

6. Forensics and advanced commands and config
    - There are a lot of flags you can use with *git diff* and *git log* to examine the history of a repository 
    - You can use aliases to configure git to display a graph-like history in your terminal
    - Interactive rebase can help keep a concise and linear history
    - *git bisect* can help find the point where a bug was introduced
    (check out Jeff Schomay's presentation for Bristech)


Also mention configuration, ssh keys, aliases


Git-in-a-small-team scenarios:

I work for a small agency whith two other developers, most sites are Wordpress based, and we don't write tests or do code reviews prior to committing and deploying. We do use Git Flow though, but not always!

 


















This repository was set up for a Git workshop for CodeHub Bristol in October 2016 and then modified for another workshop in February 2017. It is based on the idea from the [OpenTechSchool Git workshop](http://opentechschool.github.io/social-coding/) to add Cafes and Pubs to a directory. You can see the resulting website here: https://codehuborg.github.io/gitworkshop/

Here are the [exercises](docs/workshop/README.md) for the February 2017 workshop.

And these are some slides illustrating some of the concepts: https://slides.com/katjadurrani/git-2017/live#/



