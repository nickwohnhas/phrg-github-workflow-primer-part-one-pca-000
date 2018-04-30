# Pairing Project No. 1

## What is a Pairing Project?

In software development, the word 'pair' is short for 'pair programming', and is used to generically mean working together. The technique of pairing can vary, but there are typically 2 distinct roles. The first developer is called a *driver*. They will physically write all the code for the pair. The second person is called a *navigator*, but may have the role of an observer, a navigator, or a researcher. This person's responsibility is to guide strategy, coming up with ideas for improvements and looking out for any issues that may arise in the code's design.

Traditionally, pairing is done on one computer system. However, the navigator in the following lessons will mostly function as a researcher. They will help find commands and strategies that accomplish the lesson's needs. Thus, even though only the driver will be writing code, you should utilize both members' laptops.

## The Pairing Plan

This lesson and the one's that follow will pivot team member responsibilities in the middle its tasks. So, whomever starts as the driver for this project will switch and become the navigator where the lesson specifies. And vice versa.

So let's begin!

# Getting used to Git and Github

## Objectives

1. Reinforce basic bash commands like `cd`, `mkdir` and `touch`
1. Reinforce basic git commands like `init`, `add`, `commit`, and `checkout`
1. Learn how to create and merge Pull Requests on Github
1. Introduce markup language called `Markdown`
1. Review html template elements

## Introduction to Markdown

Markup is a computer text processing, a `Markdown` is example of this. `Markdown` is a simple and widely adopted language that makes it easy for developers to apply font styling with just text. You have actually already started learning a markup language. You guessed it, `HTML` has "Markup" right in its name.

So what does `Markdown` look like? Well, you are actually reading some stylized Markdown right now. Let's take a look under the hood. Open a new browser tab and open up this page once again. Now click on the github link for this lesson. Displayed below the file system in this Github view you will see this exact `README.md`. CAN YOU FIND THIS QUESTION IN THE FILE?

You'll notice that this text looks different on Github than it does on Learn. That is because on Learn, this file has had a lot more styling applied to it. That style comes directly from css files attached to the Learn project. On Github, there are fewer styles applied to this text.

So why is this text classified as a markup language? Let's pull back the final layer to find out. Click on the README.md file itself, listed in the file system towards this top of the page.

![Readme Link](img/readme-link.png?raw=true "Readme Link")

And now click on the "Raw" button, in the top right corner of the document.

![Raw Button](img/raw-button.png?raw=true "Raw Button")

What you see now is Markdown code. No where near as fancy as what you see on Learn, but really its just some text with special characters.

We won't be exploring Markdown in great detail. But it is important to know about its existance and that it is a handy tool developers use for to quickly create stylized documentation for the web. To investigate more, [check out this Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) or peruse the [Markdown doc pages themselves](https://www.markdownguide.org/basic-syntax).

## Instructions

* `cd` to a directory of your choice that is a great place to keep your pairing projects
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
* Create an `index.html` file using the `touch` command
* Create a `README.md` file using the `touch` command
* Open your text editor with `atom .` or `subl .`
* Add an h1 markdown element titled "Nitro Developer Bootcamp Students" to the `README.md`
* Time to send this up to Github!
* Return to your shell session and instantialize the repository with `git init`
* Add your `README.md` file with `git add README.md`
* Add your blank `index.html` with `git add index.html`
* Create a commit with a message (`-m`) of "First project commit"
* Go back to your browser and use the clipboard icon to copy your SSH remote URL. Make sure that SSH is selected. This is where the clopboard icon is:

![Copy Remote Url](img/copy-remote.png?raw=true "Copy Remote Url")

* In your shell session, add the remote with `git remote add origin <paste_remote_url_here>`
* And finally push up the files, `git push -u origin master`

### Switch drivers


