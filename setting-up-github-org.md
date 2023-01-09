# Setting up Your Github Org

Please follow these instructions to set-up your Github organization and repo 
**Note:** only one person per team needs to do this

## Creating a Github Organization

1. Go to [github](https://github.com) and click the "+" button in the upper righthand corner
2. Select "New organization" from the dropdown
3. Select the free tier, then input a unique name for your organization (e.g. mikes-org)
4. Input your personal email, select "My personal account", and click "Next"
5. Add all your teammates to this organization by searching for their Github usernames
 - Please also add your mentor and your instructor. Once your org is set up, all team members should be made owners 
 - **Note:** you can add people after this step, so feel free to continue on if you're missing some usernames
6. Click "Complete set-up"

There's no need to fill out this next page ("Welcome to Github"). You can scroll to the bottom and click "Submit".

## Making a Member an Owner
1. On the main org page, click "People" at the top
 - In order to change a user's role, they need to first accept the invitation to the org
2. Once they accept, a settings icon will appear next to their name. Click on that.
3. Click "change role", and then select "owner"

## Creating and Initializing your repo

1. Go to your organizations homepage (e.g. https://github.com/mikes-org)
2. Select the green button "Create a new repository"
3. Enter the name of your repository (e.g. graceshopper-project)
4. Select "Public" for the visibility
5. Select "Create Repository" (create a blank repo, do not check any boxes that add default files).
6. Copy the URL of your repo and clone it to your local machine: `git clone https://github.com/YOUR-PROJECT-URL.git`
7. `cd` into your new repo's folder
8. Follow the instructions from the [Boilerplate repo](https://github.com/FullstackAcademy/fs-app-template-v2) where you will be instructed to run these commands:
  ```
  git remote add boilermaker git@github.com:FullstackAcademy/fs-app-template-v2.git
  git fetch boilermaker
  git merge boilermaker/main
  git branch -m master main
  ```
9. Run one more command: `git push origin main`
10. Refresh your Github page and you should see your repo initialized with the boilerplate code.

## Protect your Main Branch

1. From your repo's github page, select "Settings" (rightmost option under the repo name)
2. On the sidebar, select "Branches"
3. Click "Add rule"
4. Put `main` in the text field for "Branch name pattern"
5. Select two checkboxes: "Require pull request reviews before merging" and "Include administrators".
6. Finish by selecting "Create"
