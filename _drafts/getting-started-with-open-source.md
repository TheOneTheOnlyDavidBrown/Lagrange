---
layout: post
title: "Getting started with open source"
date: 2017-04-29
categories: musings
tags: [open-source]
comments: true
image:
  feature: hacker.jpg
  teaser: hacker-teaser.jpg
  credit:
  creditlink:
---

Purpose of article:
+ encourage open source involement
+ explain how to contribute


It took me over two years into my career to start contributing to open source. I, and if you're reading this you probably feel the same, felt intimidated by proposing changes to a project that someone else with (presumably) many more years of experience created and will critique. But It's also the best way to hone your skillset because if they critique your code, you will learn and fine tune your craft. And the more code you expose yourself to, the better your code will be. If you ascribe to Malcolm Gladwell's 10,000 hour rule you will know that exposure and practice play a huge part in developing skillsets.

Much like Pascal's Wager, the worst case for contributing (the maintainer rejecting your change) is the same (from a project perspective) as doing nothing. My only regret for waiting so long to contribute was not doing it sooner.

I consider open source contributions a big plus on a a developer's resume. It shows enthusiasm and excitment for their field and their craft of building great software. With so many open source libraries available, if they haven't contributed to something, I'd be concerned.

If you are an employer/mananger (or will one day be one), let your employees contribute to open source libraries. Their contributions expose them to more code styles, patterns, and tools which in turn will help them write better code faster for YOUR company. You as an employer benefits from the increased skillset of your employee.

Now if you are content with not challenging your employees and letting their skills go stagnant until they decide to leave for a company they feel they will grow in, then go for it. The cost of replacing your team is much more than the small time investment of allowing your team to learn and give back to the community. The same community that releases all the open source tools and libraries you use on a daily basis.

Successful open source projects are very maintainable and usually are written with good patterns and tools. These patterns and tools are good to follow on your projects.

Keep in mind that one of the biggest drawbacks in open source software is the (lack of) documentation. And that is the easiest thing for you to fix. For this tutorial we will be fixing what amounts to a documentation fix.

### How to contribute

Here is the step by step process to contribute to an open source project. This is an expansion of [my contribution guidelines](https://github.com/TheOneTheOnlyDavidBrown/contributing_guidelines/blob/master/CONTRIBUTING.md)

- First things first, create a [**GitHub**](http://github.com) account.

- **Then learn some basic Git.** [This tutorial](https://try.github.io/levels/1/challenges/1) will teach you enough of the basics to get started.

- Now that you've created your Github account, head over to [**my repository**]() and click on the **'fork'** button. This creates a copy of the codebase under your name so you can edit and add code as needed. For this tutorial, I'll have you add your name/social media handle (how else am I supposed to follow you?) to the README.md file.

- Now that you have the code in a repository that you own, it's time to clone it to your machine. **Click the 'clone' button** and copy the url to your clip board.

- Open up a terminal and **navigate to the directory that houses your projects**. So if your `projects` directory is in your home directory, you'd enter `cd ~/projects` then `git clone <paste your url here>` (no <>s) the run `cd ` to enter the projects directory.

- You now have your project on your machine and ready to edit! Woohoo!

- Typically you'd **create a branch** at this point but I'm omitting that for simplicity

- Now open the directory in your editor of choice. **Open to the REAME.md file and add your name/handle** and save it.

- If this were a code based change, **this is where you would write/run the tests to make sure you didn't break anything.**

- Go back to the terminal and type **`git add README.md`**. This stages your files so you can clump changes together for simplicity.

- Then **`git commit -m 'adding a name to README.md'`**. Or you could put something more clever to make me laugh. This says that all the files that you staged are one cohesive change and the message is what will go in the log.

- Now run **`git push origin master`**. This sends your code to your repository on GitHub. Just one more step before it's up to me to merge in your changes.

- **Navigate to my repository on GitHub** (the one you created your fork from).

- Click **New pull request**.

- **Compare the changes** to make sure you are trying to merge the right code in.

- Click **Create pull request**.

- From there, **I can merge your changes in!**

Hooray! **You made your first open source contribution!** This process is the same (sans any project specific requirements like running tests) for any project on GitHub so go out and contribute!

