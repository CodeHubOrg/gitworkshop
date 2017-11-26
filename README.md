

## Git workshop 

Here are some exercises to work with this repository, best as a team

### 1. Clone and view the history
Start with cloning the directory: git clone.. 
Use git log `--oneline –graph` and `git branch -a` to investigate
Open the files in the editor. You can also look at the website by simply opening the index.html in a browser 

### 2. These are some tasks we've been told to work on:
- Two new features are to be added to the About page, by two different developers
- We need to fix a css bug
- Somebody started a feature branch which adds a nav to the homepage; it needs to be finished and merged so it can be deployed
( Optionally, additional cafes or pubs can be added as new features. Create an html file in the cafes or pubs directory, taking and existing file as template; then add the cafe or pub to the root index.html by copying an existing <li> element and modifying it. Don't be put off by the grid! )

If you are working in a team, make one person the manager of the central repo. This person should fork the repo to their own GitHub account and add the other team members as collaborators (ideally add their public keys under “deploy keys” in the repo settings)
The other members can then add the manager's repository as a remote:
git remote add upstream <github repo url>

Preparation done!

Now decide what branching and deployment strategies you want to employ as a team. Will features be merged directly into the master branch? Or do we need a development branch? Which branch do we want to deploy from? Can collaborators push directly to the repo, or should they make a pull request?

#### The tasks in more detail:

#### Features on About page (done by one developer each!)
- One feature that need to go on about/index.html is this div:
    <div id=”git-is-great”></div>
- The other feature is a paragraph that describes the group and the website, for example:
    <p>We are developers and this is a very small collection of cafes and pubs we like.</p>

#### CSS bug
The pagraph under the title ("On this site you can find some of our favourite cafes and pubs in Bristol") is meant to be centered. It seems the css declarations were accidentally deleted. They need to be added in again.
```
.centered {
    text-align: center;
}
.full {
     width: 100%;
}
```

#### Feature Nav on remote branch
There is a branch called **feature-nav** on the remote repository. Fetch this branch and check it out to your local repository. Play around with the styles for the navigation appearing in the top left corner. Then merge it into the appropriate branch, so it can be deployed. 


### 3. Notes on strategies that might be used above 

#### Merging vs rebasing
These two strategies have the same aim: To add a set of changes from one branch to another branch. The main thing to note here is that you should never use rebasing on a public branch, only on your local branches! Then rebasing can bring your branches up to date with other people's work on the master branch or other long-term branches. You can achieve a linear history for your branch, rather than one with a lot of forks. Here you can find a good explanation of the differences between merging and rebasing:
https://www.atlassian.com/git/tutorials/merging-vs-rebasing

#### Tip when updating from a remote
If you have done some work, but somebody else has worked on the same branch, it can happen that you cannot automatically pull it (pull = fetch + merge) because the branches have diverged. You get an error message. In that case you can use *pull* with the *--rebase*, flag. This will rollback your changes, merge the changes from the remote, and then reapply your changes again:
git pull --rebase*

#### Fetching branches from a remote
If somebody added a branch to a remote after you initially cloned it, you will explicitly need to fetch this branch. It will not automatically be fetched when you do a *git pull*. After fetching the branch, you can check out a local copy.

#### Pull requests
Pull requests are often used in Open Source projects, where most contributers don't have write access to the repo. To make a pull request, you need to fork the project to your own repo (we are using GitHub as an example). You clone from your copy, but then add the original repo as a second remote: 
*git remote add upstream \<project url\>*
You can then keep your repo sync'd with the project repo by pulling changes from there. When you want to contribute, you push to your clone, then you can make a pull request on the original branch through the GitHub interface. 
A good explanation on how to track the original project repo is here: https://github.com/CodeHubOrg/discussions/issues/9


### About this repo

This repository was set up for a Git workshop for CodeHub Bristol in October 2016 and then modified for another workshop in February 2017. In November 2017 I added some new exercises. It is based on the idea from the [OpenTechSchool Git workshop](http://opentechschool.github.io/social-coding/) to add Cafes and Pubs to a directory. You can see the resulting website here: https://codehuborg.github.io/gitworkshop/

And these are some slides illustrating some of the concepts: https://slides.com/katjadurrani/git-2017/live#/
