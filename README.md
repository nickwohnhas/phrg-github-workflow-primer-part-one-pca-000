# Pairing Project No. 1

## What is a Pairing Project?

[Pair programming](http://wiki.c2.com/?PairProgramming) is an [Extreme Programming Practice](http://wiki.c2.com/?ExtremeProgrammingPractice). Two developers actively collaborate on the same development effort. Traditionally pairing takes place at the same workstation with the pair sitting together. Developers can pair on individual computers when screen sharing used. Pairing can even be remote. What matters is the pair is seeing the same screen and communicating as they work.

In a pairing session the pairing team contribute complimentary efforts while collaborating. The members of the pair will have separate roles, and will likely switch roles over the course of the pairing session. Each member performs the action the other is not currently doing.

For example:
The developer currently driving will write code. The other will read code; looking for errors, consider the solution, and offer suggestions.

In the above example the developer is refered to as the "driver" and the second is the "navigator".

## The Pairing Plan

In the middle of this lesson's tasks, your responsibilities will pivot. Whomever starts as the driver will switch and become the navigator where the lesson specifies. And vice versa.

Let's begin!

# Getting used to Git and Github

## Objectives

1. Reinforce basic bash commands like `cd`, `mkdir` and `touch`
1. Reinforce basic git commands like `init`, `add`, `commit`, and `push`
1. Learn how to create and merge Pull Requests on Github
1. Introduce markup language called `Markdown`

## Introduction to Markdown

*Markup* is another name for HTML elements which style text. It has *Markup* right in its name. `Markdown` is a plain text specification for writing text using special formatting which can be read easily on its own, or converted to *Markup* to be displayed as a normal HTML web page.

So what does `Markdown` look like? Well, you are actually reading some stylized Markdown right now. Let's take a look under the hood. Open a new browser tab and open up this page once again. Now click on the github link for this lesson. Displayed below the file system in this Github view you will see this exact `README.md`. CAN YOU FIND THIS QUESTION IN THE FILE?

You'll notice that this text looks different on Github than it does on Learn. That is because on Learn, this file has had a lot more styling applied to it. That style comes directly from css files attached to the Learn project. On Github, there are fewer styles applied to this text.

So why is this text classified as a markup language? Let's pull back the final layer to find out. Click on the README.md file itself, listed in the file system towards this top of the page.

![Readme Link](img/readme-link.png?raw=true "Readme Link")

And now click on the "Raw" button, in the top right corner of the document.

![Raw Button](img/raw-button.png?raw=true "Raw Button")

What you see now is Markdown code. No where near as fancy as what you see on Learn, but really its just some text with special characters.

We won't be exploring Markdown in great detail. But it is important to know about its existance and that it is a handy tool developers use for to quickly create stylized documentation for the web. To investigate more, [check out this Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) or peruse the [Markdown doc pages themselves](https://www.markdownguide.org/basic-syntax).

## Instructions

* `cd` to a directory of your choice that will be a great place to keep your pairing projects
* Verify the location on your laptop's file system with `pwd`, which stands for "print working directory"
* Create a new directory called "pairing-projects" with the `mkdir` command
* `cd` into `pairing-projects`
* Create another new directory that will match the name of this project. Let's name it "<your_first_name>_and_<your_pair's_first_name>_first_git_project". For example, if Garett Arrowood and Bryan Reed were creating this project together, and Garett was driving, he would run this command: `mkdir garett_and_bryan_first_git_project`
* `cd` into the new directory
* In a browser, navigate to your github profile page
* In the top right corner, click on the "+" icon and select "New repository"

![Create New Repository](img/create-new-repo.png?raw=true "Create New Repository")

* In the next screen, enter the name of your new project under "Repository Name"

![Name New Project](img/name-new-repo.png?raw=true "Name New Project")

* Click the green "Create Repository" button at the bottom of the form
* Now take a long look at the next screen Github has presented to you. We are going to create a new repository on the command line
* Shift back to your shell session. You should still be in your new directory. Verify it with `pwd`
* Create a `README.md` file using the `touch` command

### Time to send this up to Github!

* Instantialize the new repository with `git init`
* Add your blank `README.md` file with `git add README.md`
* Commit your work with `git commit -m "First commit"`
* Go back to your browser and use the clipboard icon to copy your SSH remote URL. Make sure that SSH is selected. This is where the clipboard icon is:

![Copy Remote Url](img/copy-remote.png?raw=true "Copy Remote Url")

* In your shell session, add the remote with `git remote add origin <paste-remote-url-here>`. The remote URL will look something like "git@github.com:<your-github-handle>/<name-of-project>.git"
* Finally push up the files with `git push -u origin master`

### Switch drivers

Complete the next set of instructions on the other pair member's laptop.

* `cd` to a directory of your choice that will be a great place to keep your pairing projects
* Verify the location on your laptop's file system with `pwd`
* Create a "pairing-projects" directory with the `mkdir` command
* `cd` into `pairing-projects`
* In a browser, navigate to your partner's profile page and locate the new repository you just created
* When on the repo page, locate and click the "Fork" button in the top right corner:

![Fork Button](img/fork-button.png?raw=true "Fork Button")

This will redirect you to a copy of the codebase in your github account.

* Next, locate the green "clone or download" button towards the top right corner. Click on this button and verify that it says "Clone with SSH". If not, switch it to ssh. Then click on the clipboard icon to copy the remote url:

![Copy Clone Url](img/clone-project.png?raw=true "Copy Clone Url")

* Return to your shell session and clone down the project with `git clone <paste-remote-url-here>`
* `cd` into the new project folder
* Open up the codebase in your text editor
* Verify you can view the blank `README.md` files from your text editor

Now you will create a branch using `git`. Once you have completed your set of code changes, you will add and commit the work, then create a Pull Request (PR) for your partner to merge.

* Create a git branch off the main `master` branch. Lets name the branch "add-developer-names". Notice that the branch name contains no whitespace. Our command line can not process a name with whitespace because it will think you are passing it a new argument. To create our new branch, run `git checkout -b add-developer-names`
* Navigate to the `README.md` and add an h1 markdown element with the title "Nitro Developer Bootcamp Students" (check out the Markdown links above to see what this looks like)
* Next, add h2 markdown elements for each of the class participants. Each element should be titled with the first and last name of a Student Developer
* Stage your changes to the `README.md` with `git add README.md`
* Commit your changes with `git commit -m "Add developer names to README file"`
* Push your commit to your branch with `git push origin add-developer-names`

Back to the browser! If all went well, the project page should now be displaying a yellow-tinted prompt with a green button that says "Compare & pull request". Press that green button.

![Pull Request Prompt](img/yellow-tinted-pr-prompt.png?raw=true "Pull Request Prompt")

This will open up a screen that allows you to give your Pull Request (PR) a title and description. Also, you can scroll down to the bottom and see the code additions you have made. Make the PR title "Add Developer Names" if it is not already and give it a description of "My first PR description.". Find the green "Create pull request" button and click it.

![Compare Changes View](img/compare-changes.png?raw=true "Compare Changes View")

Congrats! You both have not only created your first github repo, you have also created your first PR on that repo. There is only one last step. The original driver can merge the Pull Request into their master branch with one more green button click.

![Pull Request View](img/pull-request.png?raw=true "Pull Request View")
