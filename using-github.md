# GitHub Workflow

## How to push your changes to the remote repo

*Scenario: You are on your branch named ‘my-feature-branch’ and want to push up your changes.*

Step 1: Git add and commit on my-feature-branch

Step 2: git checkout main → switches you to the main branch

Step 3: git pull → pulls from remote main branch to local main branch

Step 4: Switch to my-feature-branch and then merge main into my-feature-branch

Step 5: This is where you resolve merge conflicts between main and your feature

Step 5b: If there are changes to commit, add and commit. 

Step 6: Finally, push my-feature-branch again

**We should never be commiting on main! All we ever do on main is pull in remote changes.**

## What to do if you accidentally committed on your "main" branch

1. Create a new branch from main (to save your existing changes)
2. Delete your main branch by running “git branch --delete main”
3. Run ‘git branch -a’ to make sure main is gone
4. Run ‘git checkout origin/main’ - this pulls the latest version of the remote main repo, without any commits you made locally

You now have a clean main branch, and all your changes are safe on the new branch you created.

## Feature Branches

High level overview: pull latest main, make a branch, commit changes, push to GitHub, make a PR, get it approved, merge it to main. Rinse and repeat.

1. Make issue corresponding to feature in your project tracking system
2. Run `git checkout main`  // Makes sure you're on the "main" branch
3. `git pull`  // Gets main branch up to date
4. `git checkout -b YOUR-NEW-BRANCH-NAME`  // Creates and switches you to a new branch
5. Make commits for a given feature.
  - Use semantic commit messages: `type(scope): message` e.g. `feat(client): switch to React-Redux`
  - Keep commits related to that feature branch. If you need to make unrelated commits, **go back to main**, make a new branch, add those separate commits etc.
6. When you are done, `git push -u origin YOUR-NEW-BRANCH-NAME`
7. Navigate to GitHub and select "open pull request"
8. Refer to any issues the PR will close, e.g. `Closes #32, closes #46`. Use "closes" for each issue separately.
9. Request a review and address review comments by pushing up more commits from your local branch
10. When all checks pass, merge to `main`

Now that the remote main branch was updated with your changes, run `git checkout main`on your computer to switch to your local main branch. You can then `git pull` to bring in those changes.

## Merge Conflicts

GitHub has an online merge conflict resolution tool, but you _can_ and _should_ learn how to fix merge conflicts locally too.

1. On your local machine, `git checkout main`
2. `git pull`
3. `git checkout YOUR-FEATURE-BRANCH`
4. `git merge main`
5. `git status`
6. Find all conflicts and fix them manually. Collaborate / communicate with teammates to decide how best to do so!
7. `git add -A`
8. `git commit`
9. `git push`
10. Check that the PR now has no conflicts.
