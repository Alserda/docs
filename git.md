#Git


***


##Fork


### Creating a fork

1. Create a fork on Github / GitLab
2. <code>git clone git@gitlab.peperzaken.nl:peter/ios.git</code>
3. <code>cd ios</code>
4. <code>git remote add upstream git@gitlab.peperzaken.nl:orapp/ios.git</code>

The purpose of adding <code>upstream</code> is to update the fork whenever the main repo gets changed.

#### Updating a fork

It'll happen that your fork is outdated, and you want to update it.

1. <code>git stash</code>
2. <code>git pull upstream (branch)</code>
3. <code>git stash apply</code>


#### Excluding files with merge conflicts

1. <code>git reset HARD (file)</code>
2. <code>git checkout -- (file)</code>

