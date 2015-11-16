
## WORKFLOW

### GETTING STARTED
  1. First things first, fork the MAIN repo (git@bitbucket.org/talentmatcher/main-repo.git) to your GitHub.
  2. `git clone <YOUR-FORKED-REPO-URL>`
      - NOTE: At this point, git should only know about your forked repo (ie, the <b>origin</b> branch), and your local machine's repo (ie, the <b>master</b> branch.
  3. `git remote add upstream https://multhazim123@bitbucket.org/talentmatcher/main-repo.git`    <<<<<<<< REPLACE THE USERNAME IN THE LINK WITH YOURS
      - Tell git about the main repository -- the one we all forked from -- (ie, the <b>upstream</b> branch):
  
  


   
### MERGING WITH THE MAIN REPO
  <b>DON'T</b> update your fork by sending a pull request from the main repo to your fork. It'll push you 1 commit ahead of the main branch (just by accepting the pull), and might cause conflicts down the line.
  A lot of the times the main repo will be changed while you're away doing other stuff. When you come back, you're going to want merge changes from the main repo into your local repo, and your forked repo. Assuming you've done the commands in #2 & #3 (under "GETTING STARTED" section), all you have to do are the 4 commands below:

1. `git checkout master`
    * Checkout (ie, look at/move the pointer to) the master branch on your local machine.
2. `git fetch upstream`
    * Fetches information (ie, commit logs) <i>about</i> the upstream (ie, MAIN repo). <b>This doesn't actually make any changes to your local repo</b>! This basically updates the information your git has <i>about</i> the upstream branch.
3. `git merge upstream/master`
    * Merges upstream's master branch
    * <b>note</b>: upstream/master doesn't mean "merge upstream with master"; it means "merge upstream's master branch with our current branch (since we haven't specified a second argument, default is target for merge is current branch).
      * <b>This is where your local repo is actually affected</b>. It uses the info it got from `git fetch upstream`. This is why you MUST `fetch` before you `merge`.
4. `git push`
    * Pushes the changes from your local repo, to your forked repo on github. (So we can keep our forked repos up to date as well)

<b>Is my repo behind the main?</b>
  Probably. Always assume your branch is behind the main so always update before starting to work (assuming no conflicts). 2 ways you can check:
  1. Make sure your fork is up to date -- Go to your fork repo on github, and it should tell you whether or not you are behind, and by how many commits.
  2. Enter these in order:
      - `git fetch upstream` 
        - Fetch upstream info
      - `git log -p origin..upstream/master` 
        - Will show the log of commits you are behind by - if output is empty, then we're good.

### WORKING ON LOCAL, PUSHING CHANGES TO MAIN

1. Work on your local repo, make changes to files, add stuff, commit, that whole process.
2. `git push`
    * Push changes to your fork
3. Go to GitHub page of your FORKED REPO, and submit a <b>pull request</b> from your fork (with its new commits) to the main repo.
4. Go to GitHub page of the MAIN REPO, and once confident of no conflicts, merge the pull.
    *<b>note:</b> We DO have priveleges to allow us to do this on the main repo.

<b>PLEASE DON'T COMMIT DIRECTLY TO THE MAIN REPO! COMMIT TO YOUR FORK, PULL REQUEST TO MAIN REPO</b>

### BRANCHES - HOW TO USE

 <b> TO DO </b>

### CONFLICTS & RESOLVING

 <b> TO DO </b>
