---
layout: post
title: Adding a Local Project to Github
---

There are a lot of things that I do on the web just infrequently enough to not be able to commit to memory. One of those things happens to be adding a brand new local project to GitHub. The process is the same every time. I try to remember, I head to Google, I land on [this handy page](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/) that outlines all of the steps and I type them in one by one.

Obviously, looking this up every time is a waste of time, but committing it to memory is difficult if you aren't doing it all the time. I decided to create a quick little function to include in my `.bash_profile` that automates the process. The only requirement is to pass in the address for the new repo on GitHub.

Here's the snippet:

{% highlight bash %}
function git-new() {
  git init;
  git add .;
  git commit -m "Initial commit";
  git remote add origin "$@";
  git remote -v;
  git push origin master;
}
{% endhighlight %}

Once this has been added to your `.bash_profile`, you just need to run `source ~/.bash_profile`. Now, you can navigate to the folder containing the new project you want to add to GitHub and type the following:<br>
`git-new git@github.com:YOUR-USERNAME/YOUR-PROJECT.git`
