---
title: 'Intro to bash computing'
disqus: hackmd
---


# Intro to bash computing

###### tags: `bash`, `unix`, `command line`

> This tutorial will get us started with basic bash tools that will help us process and analyze genomic data. 



- Auto-generated Table of Contents
[ToC]

## A Note on Computing
Increasingly, biological research requires competent computing skills including the ability to install and use command-line programs. The only way to learn computing skills is to practice them! However, computing is collaborative: When you run into a problem, talk about your code with your classmates, read about similar problems on StackOverflow, and spend time on Google learning about how other people have solved the problems. Consider these challenges to be learning opportunities.  :female-student: :memo:

## Computing tips before starting
If you are new to Unix, please watch the "Introduction to Linux" video here http://www.hpc.lsu.edu/training/archive/tutorials.php. 

You can also find tips and tricks in the [GitHub repository](https://github.com/CassinSackett/BioinformaticsWorkshops).

***My biggest tips***:
-==Never use spaces in file names== - only dashes- and underscores_
-Short but informative names are best
-Use tab complete to avoid typos: start typing a file or directory name, and hit the tab key to auto-complete


## Getting set up on the supercomputer 

If you do not yet have an account on LONI (our HPC - Louisiana Optical Network Infrastructure), start here!

1. Visit https://allocations.loni.org/ to sign up for an account. I am your account sponsor (my user name is sackettl).
2. Learn about our computing resources here http://www.hpc.lsu.edu/index.php
3. If you are new to remote computing environments, please watch the two "HPC User Environment" recordings here http://www.hpc.lsu.edu/training/archive/tutorials.php

Once you have a LONI account and have familiarized yourself with its directory structure and how to appropriately use shared files and directories, please tell me your username so that I can add you to our class's project directory and give you access to our computing resources.

---

## Required Software

Windows:
-[Git for Windows](https://gitforwindows.org/) (a Unix emulator for running command-line programs)    
-[Notepad](https://notepad-plus-plus.org/downloads/v8.4.7/) (Important - After you have installed it, open and go to Settings, Preferences, New Document, and set the line endings to Unix)    

MacOS:
-[BBEdit](https://www.barebones.com/products/bbedit/) (for fast text manipulation)    

## SSH for newbies (via Woods Hole course)
SSH stands for Secure SHell. Shells are computer programs that represent the outermost layer of the operating system, allowing you to interact with the OS via commands. Another name for a shell is command interpreter. SSH is secure because every bit of text that moves between your keyboard and the operating system is encrypted.

**SSH on Mac OS**

* Open a Terminal window (in /Applications/Utilities)
* Log in to LONI using your username: ssh -X username@qbc.loni.org and supply your password when prompted
 
**SSH on Windows**

* Use Git for Windows to access LONI (Start menu - All Programs - Git BASH)
* Log in to LONI using your username: ssh -X username@qbc.loni.org and supply your password when prompted

## Basic Unix Syntax
Unix commands follow the general format of
```
command -options target
```
although not all commands need options or targets.

:drum_with_drumsticks: 
## Let's get started!
### Step 1: Organize some files

- [x] Open a terminal window
- [ ] Create a directory for today's files
- [ ] Add some files

When you open a new Terminal window, you will automatically be in your "home" directory. On a Mac, this means you are in /Users/yourname. You can always navigate back here by simply typing ``` cd ```.

#### 1a. Make a new folder (directory) and name it
```
mkdir pdog_snps
```

#### 1b. Make a README file and write a short description about what the directory will contain
```
vi README.txt
```

```vi``` will open a text editor called vim. Once here, you can edit the file. To type something, first you need to tell vim you want to **insert** text, so type the letter i. Now, you can insert either by typing manually or pasting text that you wrote in a text editor.

After writing something in the file, hit the escape key to exit editing/insert mode. To save and exit back to where you were working in Terminal, type ```:wq``` for write & quit.  If you screwed up and want to quit without saving (writing) the file, you can type ```:q!```

##### vim shortcuts
D    deletes the rest of the line after where the cursor is placed
$    moves the cursor to the end of the line
0    moves the cursor to the beginning of the line
ctrl-arrow    moves the cursor one word at a time


#### 1c. Copy an existing file to your directory
It will be easiest if we all have a copy of the major files to work on, so you'll copy them from my directory into the directory you just created.
```
cp /project/sackettl/workshop/BTPD.vcf.gz /Users/yourname/pdog_snps
```
or, if you are already in the directory where you want the files:
```
cp /project/sackettl/workshop/BTPD.vcf.gz ./
```

(the ./ means the current directory you are in)

:stars: Great; now we have some files to work with! :stars:


 

### Step 2: Write something in Markdown


:::info
:bulb: **Hint:** You can also apply styling from the toolbar at the top :arrow_upper_left: of the editing area.

![](https://i.imgur.com/Cnle9f9.png)
:::

> Drag-n-drop image from your file system to the editor to paste it!

### Step 3: Invite your team to collaborate!



:::info
:pushpin: Want to learn more? ➜ [HackMD Tutorials](https://hackmd.io/c/tutorials) 
:::

---


