
Git core concepts to understand: 

1. The basic workflow of adding files to a repository
    - new file ->  add to *staging index*  ->  commit to repository (-> push to remote)
    - adding and removing files from the index, resetting and reverting commits
    
2. Branching and merging
    - Fast-forward and three-way merges, resolving conflicts, rebasing

3. Working with remotes
    - Pushing, fetching and pulling, adding remotes, pull requests

4. Git internals 
    - A commit is a hash over metadata of the commit (author, message, parent commits etc) and a hash of the file tree object 
    - Branches are just pointers to individual commits 
    (Dave Liddament from Bristol PHP training has a good talk on that)

5. Working with Git in a Team 
    - Different branching and deploy strategies (Git Flow)
    (Read Git for Teams by Emma Jane Hogbin Westby!)

6. Forensics and advanced commands and config
    - There are a lot of flags you can use with *git diff* and *git log* to examine the history of a repository 
    - You can use aliases that easily let you display a graph-like history in your terminal
    - Interactive rebase can help keep a concise and linear history
    - *git bisect* can help find the point where a bug was introduced
    (check out Jeff Schomay's presentation for Bristech)

 Also check your configuration, and set up ssh keys for deploying to remote repositories!
