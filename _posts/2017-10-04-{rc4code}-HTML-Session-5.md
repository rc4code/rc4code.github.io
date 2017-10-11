---
layout: post
title:  "HTML/CSS Course: Session 5"
authors: ["Kat Li Yang"]
date:   2017-10-04 17:10:00 +0800
categories: HTML/CSS courses
---

From this session onwards, we will be starting to put what we have done in the past weeks online. We will be working with the popular platform Github with Github Pages. Github Pages enables Github users to host static sites on their servers.

First and foremost, we need to set up a Github account. For those who have yet to create a Github account, please follow this link and sign up for an account: [https://github.com/](https://github.com/)

Once you have signed up for an account, please download and install Github Desktop from here: [https://desktop.github.com/](https://desktop.github.com/)

While it is possible to use Git without a Graphical User Interface, it is much easier for new users to work with the GUI first. If you are interested in learning more about Git and the Git workflow, please feel free to read up from the git manual here: [https://git-scm.com/docs/gittutorial](https://git-scm.com/docs/gittutorial)

Once you have signed up for a Github account and installed Github Desktop, we will now create out first repository. A repository is like a folder where we store our code. After logging in to Github, click on the '+' sign on the top right. as shown.

![New repository]({{ site.url }}/assets/new-repo.png)

You should see the page below:

![New repository]({{ site.url }}/assets/github-pages.png)

For the name of the repository, please use [username].github.io. Only when your repository is named as such can it be set up as a Github Pages repository.

Once you have successfully set up your repository, here's what you should see:

![Open in desktop]({{ site.url }}/assets/github-pages.png)

Click on "Set up in Desktop" and allow Github Desktop to open.

Github Desktop should now prompt you about the location to set up the local repository. Choose a convenient location, such as your Desktop for now. What Github Desktop will do now is to clone the repository from the remote server onto your Desktop. You can make changes in the local folder. Let's try adding a simple page.

Move the simple page into the local repository.

![Local repository]({{ site.url }}/assets/git-repo.png)

Now, go into Github Desktop and you should see that there are some new changes made to your local repository.

![Local repository]({{ site.url }}/assets/github-changes.png)

In summary, add a description for your new commit. You may also add some message that would describe what you have changed. For instance, "Add page index.html" for the description summary.

![Local repository]({{ site.url }}/assets/commit-msg.png)

Click on "Commit to master". Then, click on "Publish" in the top right corner. Now, the changes you have made to your local repository will be sync-ed with the remote repository on Github's servers.

![Remote repository]({{ site.url }}/assets/remote-repo.png)

Go to settings on Github.

![Github settings]({{ site.url }}/assets/settings.png)

Select "master branch" under "Github Pages".

![Github settings]({{ site.url }}/assets/select-master.png)

Congratulations! Your site is now accessible.

For now, work on the site on your local repository, and sync it to Github when you want to see it online.
