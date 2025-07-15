# pull_request
In this repository, I make a procedure for creating a pull request.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 1. Find repository
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The first thing is to find a repository you want to contribute to. For example, if you want to make a contribution to Babak Naimi's sdm package, you can find it here https://github.com/babaknaimi/sdm

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 2. Go through README file
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Before making a contribution, ensure you go through the contents in the README document of the package/repository. It normally contains a lot of information about the repository including original author etc.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 3. Fork the repository
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Have a copy of the repository in your github account. That basically means forking the repository. This ensures that the changes you make to the repository do not affect the original immediately. You can work on this forked repository before finally requesting the original authors to pull in your changes.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 4. Pull the repository to your local machine
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

In my case, I copy the https link in the code section in the forked repository, then create a new R project as a version control project. I paste the copied link accordingly, and the repository will be created on my local machine.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 5. Create branch of the main to work in
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

It is normally highly recommended that we work on a branch, then merge later if necessary. To create a branch go to the Terminal tab in RStudio and write the following command:

<git checkout -b sdm_backgroun> # Where sdm_background is the branch name.
Now if you run git brach you should be able to see main and the sdm_background or the new branch you just created.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 6. Make your changes
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Under Files tab in the RStudio, navigate to the file you want to change, click it to open in the script window and make all the changes you want. For example in the man folder there is a file called background.Md, when I click it open, I can edit it in the script pane, then click save or Ctrl + S.
You can make as many changes as you want. However, note that the changes should be as precise as possible to give main author minimal review time.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 7. Check status
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

To ensure that the changes you made have been captured, run the following command in the Terminal:
<git status> # You should be able to see the file(s) you changed listed.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 8. Stage the changes
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The next step is to stage the changes to the file(s). I can do that using:
<git add man/background.Md>

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 9. Commit the changes
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Once staged, we commit the changes using the following code in the Terminal:

<git commit -m "Fixing typos in the background function"> # Make sure the message is super clear and precise.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 10. Push the commits to github
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

All the commits are still available locally in the machine. To ensure they go to github, you must push them from the branch as follows:

<git push --set-upstream origin sdm_background> # The normal git push won't work because this is a new branch, so we must set upstream 

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 11. Go back to your repository
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

If you navigate to your forked github repository, you will notice there is new branch recognized and asks you to Compare & pull request in green. Just go to the Pull requests tab on the top left. Then click New pull request. On the right side under compare, click the drop down to pick the new branch you created. On the right (base repository), it should be the original repository of the author (where you forked from). The click Create pull request. You can rename the pull request and leave any useful comments to the author. Then click Create pull request.

#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 12. Wait
#----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait as github checks for conflicts. If none, then your pull request will be visible to the author of the repository who will take time to review your code and hopefully merge your changes into their repository.

## THE END ##







