# GIT

## Basics

#### Setup
* See where Git is located: `which git`
* Get the version of Git: `git --version`
* Create an alias (shortcut) for `git status`: `git config --global alias.st status`
* Help: `git help`

#### General
* Initialize Git: `git init`
* Get everything ready to commit: `git add .`
* Get custom file ready to commit: `git add index.html`
* Commit changes: `git commit -m "Message"`
* Add and commit in one step: `git commit -am "Message"`
* Remove files from Git: `git rm index.html`
* Update all changes: `git add -u`
* Remove file but do not track anymore: `git rm --cached index.html`
* Move or rename files: `git mv index.html dir/index_new.html`
* Undo modifications (restore files from latest commited version): `git checkout -- index.html`
* Restore file from a custom commit (in current branch): `git checkout 6eb715d -- index.html`

#### Reset
* Go back to commit: `git revert 073791e7dd71b90daa853b2c5acc2c925f02dbc6`
* Soft reset (move HEAD only; neither staging nor working dir is changed): `git reset --soft 073791e7dd71b90daa853b2c5acc2c925f02dbc6`
* Mixed reset (move HEAD and change staging to match repo; does not affect working dir): `git reset --mixed 073791e7dd71b90daa853b2c5acc2c925f02dbc6`
* Hard reset (move HEAD and change staging dir and working dir to match repo): `git reset --hard 073791e7dd71b90daa853b2c5acc2c925f02dbc6`

#### Update & Delete
* Test-Delete untracked files: `git clean -n`
* Delete untracked files (not staging): `git clean -f`
* Unstage (undo adds): `git reset HEAD index.html`
* Commit to most recent commit: `git commit --amend -m "Message"`
* Update most recent commit message: `git commit --amend -m "New Message"`

#### Branch
* Show branches: `git branch`
* Create branch: `git branch branchname`
* Change to branch: `git checkout branchname`
* Create and change to new branch: `git checkout -b branchname`
* Rename branch:
  * `git branch -m branchname new_branchname` or:
  * `git branch --move branchname new_branchname`
* Show all completely merged branches with current branch: `git branch --merged`
* Delete merged branch (only possible if not HEAD):
  * `git branch -d branchname` or:
  * `git branch --delete branchname`
* Delete not merged branch: `git branch -D branch_to_delete`

#### Merge
* True merge (fast forward): `git merge branchname`
* Merge to master (only if fast forward): `git merge --ff-only branchname`
* Merge to master (forc a new commit): `git merge --no-ff branchname`
* Stop merge (in case of conflicts): `git merge --abort`
* Stop merge (in case of conflicts): `git reset --merge` // prior to v1.7.4

#### Stash
* Put in stash: `git stash save "Message"`
* Show stash: `git stash list`
* Show stash stats: `git stash show stash@{0}`
* Show stash changes: `git stash show -p stash@{0}`
* Use custom stash item and drop it: `git stash pop stash@{0}`
* Use custom stash item and do not drop it: `git stash apply stash@{0}`
* Delete custom stash item: `git stash drop stash@{0}`
* Delete complete stash: `git stash clear`

#### Gitignore & Gitkeep
* About: https://help.github.com/articles/ignoring-files
* Useful templates: https://github.com/github/gitignore
* Add or edit gitignore: `nano .gitignore`
* Track empty dir: `touch dir/.gitkeep`

#### Log
* Show commits: `git log`
* Show oneline-summary of commits: `git log --oneline`
* Show oneline-summary of commits with full SHA-1: `git log --format=oneline`
* Show oneline-summary of the last three commits: `git log --oneline -3`

* Show only custom commits:
  * `git log --author="Sven"`
  * `git log --grep="Message"`
  * `git log --until=2013-01-01`
  * `git log --since=2013-01-01`
* Show only custom data of commit:
  * `git log --format=short`
  * `git log --format=full`
  * `git log --format=fuller`
  * `git log --format=email`
  * `git log --format=raw`
* Show changes: `git log -p`
* Show every commit since special commit for custom file only: `git log 6eb715d.. index.html`
* Show changes of every commit since special commit for custom file only: `git log -p 6eb715d.. index.html`
* Show stats and summary of commits: `git log --stat --summary`
* Show history of commits as graph: `git log --graph`
* Show history of commits as graph-summary: `git log --oneline --graph --all --decorate`

#### Compare
* Compare modified files: `git diff`
* Compare modified files and highlight changes only: `git diff --color-words index.html`
* Compare modified files within the staging area: `git diff --staged`
* Compare branches: `git diff master..branchname`
* Compare branches like above: `git diff --color-words master..branchname^`
* Compare commits:
  * `git diff 6eb715d`
  * `git diff 6eb715d..HEAD`
  * `git diff 6eb715d..537a09f`
* Compare commits of file:
  * `git diff 6eb715d index.html`
  * `git diff 6eb715d..537a09f index.html`
* Compare without caring about spaces:
  * `git diff -b 6eb715d..HEAD` or:
  * `git diff --ignore-space-change 6eb715d..HEAD`
* Compare without caring about all spaces:
  * `git diff -w 6eb715d..HEAD` or:
  * `git diff --ignore-all-space 6eb715d..HEAD`
* Useful comparings: `git diff --stat --summary 6eb715d..HEAD`
* Blame: `git blame -L10,+1 index.html`

#### Releases & Version Tags
* Show all released versions: `git tag`
* Show all released versions with comments: `git tag -l -n1`
* Create release version: `git tag v1.0.0`
* Create release version with comment: `git tag -a v1.0.0 -m 'Message'`
* Checkout a specific release version: `git checkout v1.0.0`

#### Collaborate
* Show remote: `git remote`
* Show remote details: `git remote -v`
* Add remote origin from GitHub project: `git remote add origin https://github.com/user/project.git`
* Add remote origin from existing empty project on server: `git remote add origin ssh://root@123.123.123.123/path/to/repository/.git`
* Remove origin: `git remote rm origin`
* Show remote branches: `git branch -r`
* Show all branches: `git branch -a`
* Compare: `git diff origin/master..master`
* Push (set default with `-u`): `git push -u origin master`
* Push to default: `git push origin master`
* Fetch: `git fetch origin`
* Pull: `git pull`
* Pull specific branch: `git pull origin branchname`
* Merge fetched commits: `git merge origin/master`
* Clone to localhost:
  * `git clone https://github.com/user/project.git` or:
  * `git clone ssh://user@domain.com/~/dir/.git`
* Clone to localhost folder: `git clone https://github.com/user/project.git ~/dir/folder`
* Clone specific branch to localhost: `git clone -b branchname https://github.com/user/project.git`
* Delete remote branch (push nothing):
  * `git push origin :branchname` or:
  * `git push origin --delete branchname`

#### Misc
* Create a zip-archive: `git archive --format zip --output filename.zip master`

--------

## In Detail
* Remove a current tracking relationship: `git branch --unset-upstream`
* Cryptographically sign all commits: `commit.gpgsign`
* Revert a single file with uncommitted changes to HEAD: `git checkout <filename>`
* Unstage a file: `git reset HEAD <file>`
* Print changed files in last commit: `git show --name-only [commit]`
* Undo commit, keeping changes: `git reset --soft @~1`
* Go one step back in history: `git checkout @~1`
* Show commit changes: `git show <commit-sha>`
* Push master branch to origin: `git push origin master`
* List all branches: `git branch -a`
* List remote branches: `git branch -r`
* Sync list of remote branches: `git remote update`
* Checkout remote branch into local repository: `git checkout -t -b <local-name> <remote-name>`
* Create a branch: `git checkout -b <name>`
* Push local branch to remote: `git push origin <remote-name>`
* Merge two branches: `git checkout <target>` & `git merge <source>`
* Merge two branches with squash: `git checkout <target>` & `git merge --squash <source>`
* See what branches are merged into master: `git branch -r --merged master`
* pull changes from the server + rebase (equivalent of git stash save && git pull && git stash pop && git push) + push: `git pull --rebase && git push`
* Set up git inet server: `git daemon --base-path /home/git --verbose`
* Add remote origin: `git remote add origin <url>`
* Fix 'branch not tracking anything': `git config --add branch.master.remote origin` & `git config --add branch.master.merge refs/heads/master`
* Extract patch from a given file: `git diff --patch-with-raw rev1 rev2 patched_file > diff_file`
* Diff with paging: `GIT_PAGER='less -r' git dc`
* Apply a patch: `git apply diff_file`
* Publish branch: `git push origin <name>`
* Delete remote branch: `git push origin :<name>`
* Cherry-pick a commit: `git cherry-pick -n <sha>`
* Revert commit: `git revert -n <sha>`
* Reset HEAD to n commits back: `git reset --hard HEAD~<n>`
* Squash N last commits: `git rebase --interactive --autosquash HEAD~N`
* search git log commits: `git log -S "free text"`
* Prune history: `git gc`, `git gc --aggressive`, `git prune`
* Checkout GitHub PR: `git fetch origin pull/1234/head:local-branch-name`
* Global gitignore: `git config --global core.excludesfile ~/.gitignore`
* Global username & email: `git config --global user.name "Jakub Pawlowicz"` & `git config --global user.email '<email>'`
* Local username & email: `git config user.name "Jakub Pawlowicz" & git config user.email '<email>'`
* Convert long sha to short one: `git rev-parse --short <sha>`
* remove file from history (can use 'git rm -rf...' to remove files recursively):

```
git filter-branch --index-filter 'git rm --cached --ignore-unmatch <path to file>' --prune-empty --tag-name-filter cat -- --all
git push origin master --force
rm -rf .git/refs/original/
git reflog expire --expire=now --all
git gc --prune=now
git gc --aggressive --prune=now
```

* Some useful aliases:

```
git config --global alias.aa "add --all"
git config --global alias.ai "add --interactive"
git config --global alias.b "branch"
git config --global alias.ba "branch -a"
git config --global alias.c "commit"
git config --global alias.ca "commit --amend"
git config --global alias.cf '!sh -c "git commit --fixup $@"'
git config --global alias.co "checkout"
git config --global alias.col '!sh -c "git checkout -b $@"'
git config --global alias.cor '!sh -c "git checkout --track -b $@ origin/$@"'
git config --global alias.cp "cherry-pick"
git config --global alias.cpa "cherry-pick --abort"
git config --global alias.cpc "cherry-pick --continue"
git config --global alias.cs '!sh -c "git commit --squash $@"'
git config --global alias.d "diff"
git config --global alias.dc "diff --cached"
git config --global alias.ds "diff --stat"
git config --global alias.dsc "diff --stat --cached"
git config --global alias.fpr '!sh -c "git fetch origin pull/$@/head:$@-pr"'
git config --global alias.l "log"
git config --global alias.lf "log --follow"
git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative --all"
git config --global alias.m "merge"
git config --global alias.mb "merge-base master HEAD"
git config --global alias.ms "merge --squash"
git config --global alias.pl "pull"
git config --global alias.ps "push"
git config --global alias.psc '!sh -c "git push --set-upstream origin \$(git rev-parse --abbrev-ref HEAD)"'
git config --global alias.psd '!sh -c "git push origin :\$(git rev-parse --abbrev-ref HEAD)"'
git config --global alias.r "reset HEAD"
git config --global alias.rb "rebase"
git config --global alias.rba "rebase --abort"
git config --global alias.rbc "rebase --continue"
git config --global alias.rbi "rebase --interactive --autosquash"
git config --global alias.rbm "rebase --interactive --autosquash origin/master"
git config --global alias.rh "reset --hard"
git config --global alias.rs "reset --soft"
git config --global alias.s "status"
git config --global alias.sh "show"
git config --global alias.shs "show --stat"
git config --global alias.st "stash"
```

* Get some nice colours:

```
git config --global color.diff auto
git config --global color.status auto
git config --global color.branch auto
```

* Branch name and merge status in bash prompt (should go to local or global bash profile):

```
function parse_git_dirty {
  [[ $(git status 2> /dev/null | tail -n1) != "nothing to commit, working directory clean" ]] && echo "*"
}

function parse_git_branch {
  git branch --no-color 2> /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/[\1$(parse_git_dirty)]/"
}

export PS1='\u@\h [\033[0;36m]\w [\033[0;32m]$(parse_git_branch)[\033[0m]$ '
```

* Git log (Pretty graph view): `git log --graph`
* By making the following alias you get:
  * colors
  * graph of commits
  * one commit per line
  * abbreviated commit IDs
  * dates relative to now
  * commit references
  * author of the commit
  * And the alias is:
  * `git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"`
* And every time you need to see your log, just type in: `git lg`
* or, if you want to see the lines that changed: `git lg -p`
* Stash
  * `git stash`                                 : Stash current changes
  * `git stash save "appropriate caption here"` : Name stashed changes
  * `git stash apply`                           : Apply the last stashed item
  * `git stash pop`                             : Apply and drop most recent stash
  * `git stash list`                            : List all stashes
  * `git stash clear`                           : Clear all entries in stash
* Cherry pick and apply to current branch: `git cherry-pick ###SHA-1##`
  * In cases picking one single commit is not enough and you need, let's say three consecutive commits - rebase is the right tool, not cherry-pick.
* Forget added files in git: `git rm -r --cached .` & `git add .`
* Git Aliases: `git config --global alias.<handle> <command>`
* Deleting a branch both locally and remotely:
  * Locally: `git branch -D local_branch_name`
    * `-D` force deletes, `-d` will give you a warning if it's not already merged in.
  * Remotely: add the `-r` flag:
    * `git branch -dr origin/remote_branch_name` or,
    * `git push origin --delete remote_branch_name` or,
    * `git push origin :remote_branch_name`
* Different branch name for local and remote
  * Branch out locally:
    * `git checkout -b local_branch_name`
    * Checkout branch with an easy to remember local_branch_name
  * Push to remote & set upstream:
    * `git push -u origin local_branch_name:remote_branch_name`
  * Push the local branch to remote repo with a different descriptive name remote_branch_name
    * `git branch --set-upstream-to=origin/remote_branch_name`
  * Set your push.default to upstream to push branches to their upstreams (which is the same that pull will pull from), rather than pushing branches to ones matching in name (which is the default setting for push.default, matching).
    * `git config push.default upstream`
* Squash PR commits into one
  * Fetch from upstream (when merging clone to main upstream branch) or origin (when merging branch to master)
    * `git fetch upstream`
    * `git checkout mybranch`
    * `git merge upstream/master`
    * If necessary, resolve conflicts and git commit...
    * `git reset --soft upstream/master`
    * `git commit -am 'Some cool description for a single commit'`
    * `git push -f`
    * Note that it's super important that you merge before resetting, and that the argument is the same master branch. Otherwise you risk messing up your local history.
    * The --soft parameter tells Git to reset HEAD to another commit, but that's it. If you specify --soft Git will stop there and nothing else will change. What this means is that the index and working copy don't get touched, so all of the files that changed between the original HEAD and the commit you reset to appear to be staged.
* Keeping a forked repo in sync with the main repo:
  * `git remote add upstream <path-to-the-main-repo>`
  * `git fetch upstream`
  * `git rebase upstream/master`
* Deleting last commit from git:
  * If you already pushed, use `git revert`
  * If no one else is using your branch: `git reset --hard HEAD~1 (or) git reset --hard <sha1-commit-id>` & `git push origin HEAD --force`


## A Simple, Straightforward, Inelegant-but-Foolproof Git Workflow

This workflow may be a bit redundant for a git pro, but it's the simplest way to avoid headaches for git beginners. Basically, you only work in feature branches that never leave your machine. You only push/pull from 'mainstream' branches in which you **never edit files directly**. You link these two worlds by merging feature branches into 'mainstream' branches (which correspond to branches hosted on Github). (Assume that we are starting with a freshly cloned repository. We'll call the current branch testing1, since it doesn't need to be master).

1. **Pull the branch** (git pull testing1). (Do this if you are not starting with a freshly cloned repository. Make sure you specify the branch name, or you will pull from the wrong branch on GitHub).
1. **Make a new feature branch**. This feature branch will only exist on your machine, and you are free to delete it once it has been merged and pushed (git branch -d). Please do not clutter up the foreign repo by pushing extraneous feature branches.
1. **Switch to the feature branch** (git checkout NEWBRANCH). (You have just switched from testing1 to NEWBRANCH).
1. **Make changes, commit**. Repeat until the feature is done, and you are ready to merge back into the original branch.
1. **Switch to the original branch** (git checkout testing1).
1. **Pull the changes from the origin** (git pull origin testing2). (Make sure you use the right name for testing1, or you will pull changes from the wrong branch!). If you have been following this process properly, you cannot have merge conflicts at this stage, because you have never edited the testing1 branch on your machine since you last pulled it).
1. **Rebase the feature branch into the current branch**. (git rebase NEWBRANCH)
1. **Push the newly rebased current branch to GitHub**. (git push origin testing1). (**Make sure you include the foreign branch name, or you will end up pushing to master by default!**)
1. You're done!


## Branching Model

`git-flow` is probably the most popular branching technique out there. It's also crap. There are many caveats in it, and it doesn't use some use git primitives where it should. A succesful branching model for simple projects is:

* master is the truth of all merges
* each feature gets their own branch on the contributor's fork
* whenever a feature is done, it's pulled in
* master gets a tag

It doesn't need to be complex to be efficient. If hotfixes need to be performed, master can be rebased on top of that. If features need to be removed, just request the commit range for certain tag to roll back. Tada!

* [git flow considered harmful](http://endoflineblog.com/gitflow-considered-harmful)
* [follow up: git flow considered harmful](http://endoflineblog.com/follow-up-to-gitflow-considered-harmful)
* [chronological git history is silly](https://news.ycombinator.com/item?id=9745966)


## Git hooks

Git hooks are a way of extending git with functionality whenever things happen. To some extent `npm` has a similar mechanism called `npm scripts`. Git hooks are just regular bash scripts that are triggerd on actions. They live in `.git/hooks`, where the filename is the name of the hook. The following hooks are available:

```
applypatch-msg
pre-applypatch
post-applypatch
pre-commit
prepare-commit-msg
commit-msg
post-commit
pre-rebase
post-checkout
post-merge
pre-receive
update
post-receive
post-update
pre-auto-gc
post-rewrite
pre-push
```

Git hook scripts cannot be checked into version control. If you want to persist scripts between multiple users you must check them into the project itself and then symlink them back in, preferably in a bootstrap script. Be careful when running hard symlinks though, as they will overwrite any local files. Instead create an aggregator script that moves the original scripts and then imports the original + repo scripts back in.

Example functionality for git hooks includes: checking code style on commit, running extended tests on rebase to master, verify that no commit is performed while rebasing, semver is updated, etc.

* [githooks](http://githooks.com/)
* [putting git hooks into repository](http://stackoverflow.com/questions/3462955/putting-git-hooks-into-repository)


### git bisect

Find by binary search the change that introduced a bug.

* [git_bisect - linus torvalds](http://yarchive.net/comp/linux/git_bisect.html)


### Manage main and fix commits

By running `--fixup` you can create fix commits for your main commit; this is a better alternative to continuously rebasing on top of your previous commit. With `--autosquash` the `--fixup` commits are automatically squashed into their relevant commit.

```
$ git commit --fixup <commit-sha>   # automatically marks your commit as a fix
                                    # of a previous commit
$ git rebase -i --autosquash        # automatically organize merging of these
                                    # fixup commits and associated normal
                                    # commits
```

* [stackoverflow/easily-fixup-past-commit](http://stackoverflow.com/questions/3103589/how-can-i-easily-fixup-a-past-commit)
* [git-fixup](https://github.com/deiwin/git-dotfiles/blob/docs/bin/git-fixup)
* [keep your branch clean with git fixup and autosquash](http://fle.github.io/git-tip-keep-your-branch-clean-with-fixup-and-autosquash.html)


#### See Also

* [how to undo almost anything with git](https://github.com/blog/2019-how-to-undo-almost-anything-with-git)
* [git koans](http://stevelosh.com/blog/2013/04/git-koans/)
* [jonathanong/git-style-guide](https://github.com/jonathanong/git-style-guide)


## Glossary

* The "blame" feature in Git describes the last modification to each line of a file, which generally displays the revision, author and time. This is helpful, for example, in tracking down when a feature was added, or which commit led to a particular bug.
* A branch is a parallel version of a repository. It is contained within the repository, but does not affect the primary or `master` branch allowing you to work freely without disrupting the "live" version. When you've made the changes you want to make, you can merge your branch back into the `master` branch to publish your changes.
* A clone is a copy of a repository that lives on your computer instead of on a website's server somewhere, or the act of making that copy. With your clone you can edit the files in your preferred editor and use Git to keep track of your changes without having to be online. It is, however, connected to the remote version so that changes can be synced between the two. You can push your local changes to the remote to keep them synced when you're online.
* A collaborator is a person with read and write access to a repository who has been invited to contribute by the repository owner.
* A commit, or "revision", is an individual change to a file (or set of files). It's like when you _save_ a file, except with Git, every time you save it creates a unique ID (a.k.a. the "SHA" or "hash") that allows you to keep record of what changes were made when and by who. Commits usually contain a commit message which is a brief description of what changes were made.
* A contributor is someone who has contributed to a project by having a pull request merged but does not have collaborator access.
* A diff is the _difference_ in changes between two commits, or saved changes. The diff will visually describe what was added or removed from a file since its last commit.
* Fetching refers to getting the latest changes from an online repository (like GitHub.com) without merging them in. Once these changes are fetched you can compare them to your local branches (the code residing on your local machine).
* A fork is a personal copy of another user's repository that lives on your account. Forks allow you to freely make changes to a project without affecting the original. Forks remain attached to the original, allowing you to submit a pull request to the original's author to update with your changes. You can also keep your fork up to date by pulling in updates from the original.
* Git is an open source program for tracking changes in text files. It was written by the author of the Linux operating system, and is the core technology that GitHub, the social and user interface, is built on top of.
* Issues are suggested improvements, tasks or questions related to the repository. Issues can be created by anyone (for public repositories), and are moderated by repository collaborators. Each issue contains its own discussion forum, can be labeled and assigned to a user.
* Markdown is an incredibly simple semantic file format, not too dissimilar from .doc, .rtf and .txt. Markdown makes it easy for even those without a web-publishing background to write prose (including with links, lists, bullets, etc.) and have it displayed like a website. GitHub supports Markdown, and you can learn about the semantics.
* Merging takes the changes from one branch (in the same repository or from a fork), and applies them into another. This often happens as a Pull Request (which can be thought of as a request to merge), or via the command line. A merge can be done automatically via a Pull Request via the GitHub.com web interface if there are no conflicting changes, or can always be done via the command line.
* Open source software is software that can be freely used, modified, and shared (in both modified and unmodified form) by anyone. Today the concept of "open source" is often extended beyond software, to represent a philosophy of collaboration in which working materials are made available online for anyone to fork, modify, discuss, and contribute to.
* Organizations are a group of two or more users that typically mirror real-world organizations. They are administered by users and can contain both repositories and teams.
* Private repositories are repositories that can only be viewed or contributed to by their creator and collaborators the creator specified.
* Pull refers to when you are fetching _in_ changes _and_ merging them. For instance, if someone has edited the remote file you're both working on, you'll want to _pull_ in those changes to your local copy so that it's up to date.
* Pull requests are proposed changes to a repository submitted by a user and accepted or rejected by a repository's collaborators. Like issues, pull requests each have their own discussion forum.
* Pushing refers to sending your committed changes to a remote repository such as GitHub.com. For instance, if you change something locally, you'd want to then _push_ those changes so that others may access them.
* A remote is the version of something that is hosted on a server, most likely GitHub.com. It can be connected to local clones so that changes can be synced.
* A repository is the most basic element of GitHub. They're easiest to imagine as a project's folder. A repository contains all of the project files (including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private.
* SSH keys are a way to identify yourself to an online server, using an encrypted message. It's as if your computer has its own unique password to another service. GitHub uses SSH keys to securely transfer information from GitHub.com to your computer.
* When talking about a branch or a fork, the primary branch on the original repository is often referred to as the "upstream", since that is the main place that other changes will come in from. The branch/fork you are working on is then called the "downstream".
* Users are personal GitHub accounts. Each user has a personal profile, and can own multiple repositories, public or private. They can create or be invited to join organizations or collaborate on another user's repository.


## Another Git Workflow

```
git init

git clone username@host:/path/to/repository

git remote add origin <server>

git add file.ext                              # add a single file to staging
git add --patch file.ext                      # add changes from file, line by line
git add .                                     # add everything

git reset file.ext                            # undo git add - unstage a file

git commit -m "Commit Message"                # commit with message
git commit -a                                 # add all, write long msg
git commit --amend                            # amend changes to previous commit

git stash                                     # saves current state for later use
git stash apply                               # restores/merges stashed state
git stash unapply                             # reverts stash apply

git rm --cached <filename>                    # stop tracking a file

git push origin master                        # upload changes
git push --set-upstream origin master         # set default upstream for push
git push                                      # once you set default

git pull                                      # default branch
git pull origin master                        # for master branch
git pull origin branchname                    # for specific branch

# If you want to be able to just do git push, git pull:
git config branch.master.remote origin
git config branch.master.merge refs/heads/master

# Drop all local commits and revert to origin:
git fetch origin
git reset --hard origin/master

# Drop all uncommited changes
git checkout -- <file>                        # drops only changes for <file>
git checkout -- .                             # drops all the changes

# Branching:
git checkout -b branchname                    # create new branch
git checkout master                           # switch back to master
git branch -d branchname                      # delete branch
git push origin branchname                    # push branch
git merge branchname                          # merge branchname into current

# Tagging:
git tag -a 1.1 -m "tag description"           # regular tag
git tag 1.1                                   # lightweight tag
git tag 1.1 9fceb02                           # tag specific commit
git push --tags                               # push tags
git tag -d 1.0                                # delete local tag
git push origin :refs/tags/1.0                # delete tag from remote

# Adding a Submodule
git submodule add usename@host:/path/to/repo foldername

# Initializing sumbodule in a cloned project
git submodule init
git submodule update

git rebase -i HEAD~3                          # rebase last 3 commits

git diff                                      # diff against working area
git diff --staged                             # dif against staged (added) files

# List files that were modified between TAG2 and TAG1
git diff --name-status TAG2 TAG1
git diff --name-status TAG2 TAG1 | wc -l      # count modified files
```

--------

## Submodule syntax (in a `.gitmodules` file):

```
[submodule "name-of-submodule"]
  path = path-of-submodule
  url = http://url.of/submodule.git
```

