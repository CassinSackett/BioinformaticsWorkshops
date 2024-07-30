---
title: 'Intro to bash computing'
disqus: hackmd
---


# Intro to bash computing

[![hackmd-github-sync-badge](https://hackmd.io/-4j7x-bKQESS2pQcfJ-1SA/badge)](https://hackmd.io/-4j7x-bKQESS2pQcfJ-1SA)


###### tags: `bash`, `unix`, `command line`

> This tutorial will get us started with basic bash tools that will help us process and analyze genomic data. 



- Auto-generated Table of Contents
[ToC]

## A Note on Computing
Increasingly, biological research requires competent computing skills including the ability to install and use command-line programs. The only way to learn computing skills is to practice them! However, you don't need to practice by yourself, especially as you are getting started. Computing is collaborative: When you run into a problem, talk about your code with your classmates, read about similar problems on StackOverflow, and spend time on Google learning about how other people have solved the problems. Consider these challenges to be learning opportunities.  :female-student: :memo:

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
-[Notepad +](https://notepad-plus-plus.org/) (Important - After you have installed it, open and go to Settings, Preferences, New Document, and set the line endings to Unix)    

MacOS:    
-[BBEdit](https://www.barebones.com/products/bbedit/) (for fast text manipulation)    

## SSH for newbies (via Woods Hole course)
SSH stands for **S**ecure **SH**ell. Shells are computer programs that represent the outermost layer of the operating system, allowing you to interact with the OS via commands. Another name for a shell is command interpreter. SSH is secure because every bit of text that moves between your keyboard and the operating system is encrypted.

**SSH on Mac OS**

* Open a Terminal window (in /Applications/Utilities)
* Log in to LONI using your username: ssh -X username@qbc.loni.org and supply your password when prompted
 
**SSH on Windows**

* Use Git for Windows to access LONI (Start menu - All Programs - Git BASH)
* Log in to LONI using your username: ```ssh -X username@qbc.loni.org``` and supply your password when prompted

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
- [ ] Log in to the cluster
- [ ] Create a directory for today's files
- [ ] Add some files

When you open a new Terminal window, you will automatically be in your "home" directory. On a Mac, this means you are in /Users/yourname. You can always navigate back here by simply typing ``` cd ```.

#### 1a. Make a new folder (directory) and name it something informative
```
mkdir pdog_snps
```

#### 1b. Make a README file and write a short description about what the directory will contain
```
vi README.txt
```

```vi``` will open a text editor called vim. Once here, you can edit the file. To type something, first you need to tell vim you want to **insert** text, so type the letter ```i```. Now, you can insert either by typing manually or pasting text that you wrote in a text editor.

A good README file describes what the folder contains, where the information comes from, and what the aim of the project is. You can always go back and edit this to add more information as you go.

After writing something in the file, hit the **escape** key to exit editing/insert mode. To save and exit back to where you were working in Terminal, type ```:wq``` for **w**rite & **q**uit.  If you screwed up and want to quit without saving (writing) the file, you can type ```:q!``` (the ! means 'not', so you are saying quit-not-save)

##### vim shortcuts
**D**    deletes the rest of the line after where the cursor is placed
**$**    moves the cursor to the end of the line    
**0**    (the number) moves the cursor to the beginning of the line    
ctrl-arrow    or option-arrow moves the cursor one word at a time


#### 1c. Upload this file to the cluster and then log in
Most genomics work requires working on a cluster or on the cloud, especially for the first stages of sequence processing. This is especially true for collaborative projects.

Let's change locations into our home directory:
```
cd ~
```

Now, upload the file to your home directory on LONI using **S**ecure **C**o**P**y (scp).

```
scp README.txt username@qbc.loni.org:/work/username/
```
Oops!  Why didn't that work? :confused: 

Because we changed into our home directory, we were no longer in the same directory as the file we wanted to upload. There are two solutions: either ```cd``` again into the directory containing the file, or provide the full path when we are uploading:

```
scp ~/pdog_snps/README.txt username@qbc.loni.org:/work/username/
```

This command will prompt you for your password, which you can type or paste at the prompt. (You will not see any letters or cursor movement, but if you are typing, Terminal is listening!)

Now, your file is waiting for you on the cluster, so let's log in:
```
ssh -X username@qbc.loni.org
```
and provide your password at the prompt, as before.

Verify that you are where you think you are by checking your **P**resent **W**orking **D**irectory:
```
pwd
```

We are always in our home directory when we log in. However, we want to store files (short term) and submit jobs from our work directory, so let's go there:

```
cd /work/username/
```


Now, check whether the file you just uploaded is indeed in your directory by listing all the files:
```
ls -lh
```
If you include the ```l``` flag, it will print in **l**ong format, i.e., information about each file like the time of modification, file size, and permissions. The ```h``` flag makes the numbers **h**uman-readable, which is useful when we are working with genome-scale files. I also usually use ```tr``` to print the files in **r**everse order according to the **t**ime they were last modified, with most recent files at the bottom.

Do you see your file?  Take a look at what's inside by using
``` less README.txt ``` . After you've seen it, type ```q``` to **q**uit this viewing mode. You'll notice that the file's contents, which were previously displayed on the screen, have disappeared. Sometimes there will be part of a file that you want to print in a way that it does not disappear. One way is to use ``` more README.txt ``` which will print one screen at a time. Beyond this first screen, you can hit 'enter' to print one line at a time or 'space' to print another whole page. If you don't want to print the whole document, you can use the same ```q``` to quit the ```more``` command.


#### 1d. Copy an existing file to your directory
It will be easiest if we all have a copy of the major files to work on, so you'll **c**o**p**y them from my directory into yours.  

First, make a new directory to organize all the files:
```
mkdir pdog
```

Now you can copy the files to the directory you just created.
```
cp /project/sackettl/GPD_37spatial/GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz /work/username/pdog/
```
or, if you are already in the directory where you want the files:
```
cp /project/sackettl/GPD_37spatial/GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz ./
```

(the ./ means the current directory you are in.)

:stars: Great; now we have some files to work with! :stars:


 

### Step 2: Write a job submission script
Because clusters have hundreds or thousands of users, we  need to reserve computational resources. This is an organizational system that ensures that users do not interfere with each other.

To reserve resources, we submit a request to the cluster to run our "job" for a certain amount of time and using a certain amount of memory.

LONI uses [slurm](https://slurm.schedmd.com/documentation.html) to organize its computing resources. A typical job script looks like this:

```
#Lines that tell LONI what queue you need, how much time and memory, the name of the project you are working under, etc.
#Lines that create a log file and an error file

Line(s) that load software

Lines that run the software with your specific files, producing output files
```

In slurm, that looks like this:
```
#!/bin/bash
#SBATCH -p workq
#SBATCH -N 1
#SBATCH -n 24
#SBATCH -t 8:00:00
#SBATCH -A loni_gwas_ajaz 
#SBATCH -o log-file_date.out 
#SBATCH -e error-file_031124.err

export JOBS_PER_NODE=22

module load module_name

cd /home/username/pdog/

commands

```
where    
``` -p ``` is the name of the queue    
``` -N ``` is the number of nodes    
``` -n ``` is the number of tasks/ CPU cores     
``` -t ``` is the maximum time, in hh:mm:ss format    
``` -A ``` is the Allocation/ project name,
and    
``` -o ``` and ``` -e ``` specify the log file and error files, respectively.

Every job script submitted on LONI will start with this.

#### 2a. Create a new job script
I like to use the file extension .sh because this is a bash script, but you could also use .job or something else that makes sense to you.

Create a new script with a descriptive name. Let's practice by creating a script that will uncompress (unzip) our .gz file (even though most software will recognize compressed fastq.gz files).

``` vi gunzip.sh ```
and then add the text above, but for the single queue and with a 30 minute time limit.

Now add the major command for this script, gunzip.

``` gunzip compressed_file.gz ```

:eyes: :point_right:   Hint: the filename is not GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz; it is /work/username/GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz  :eyes: 


#### 2b. Submit your job script
After you have saved (:wq) your script, you are ready to submit it!

``` sbatch gunzip.sh ```


My preferred way to make new scripts that do different things is to copy an existing script and modify it. Go ahead and do this for the next step.

``` cp gunzip.sh vcftools.sh ```

Now, when we are ready, we'll only have to change the runtime, the amount of memory, the queue, the name of the log/error files, and the command.

### Step 3: Use [vcftools](https://vcftools.github.io/man_latest.html) to learn something fun about the data!

Peruse the documentation for [vcftools](https://vcftools.github.io/man_latest.html) to get an idea of some of the functionalities of the software. Each group will write a script for a different function in vcftools.

The vcftools format for all commands is similar:
```
vcftools --vcf GPD37_rangewide_Q20SNPsMNPsQC.vcf --options --recode --out GPD37_rangewide_Q20SNPsMNPsQC_modified
```
where the ```--out``` refers to the prefix you want to give the file, ```--recode``` means make a new vcf file with the options you provided, and the ```--options``` are various filtering steps or analyses. You can combine multiple options in one step. Let's filter by missing data for an example.

Create a file that contains only sites genotyped in at least 80% of individuals (note the ```--gzvcf``` flag for compressed files):
```
vcftools --gzvcf GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz --max-missing 0.8 --recode --out GPD37_rangewide_Q20SNPsMNPsQC_80pct
```
Note that the VCFtools syntax may seem a little backwards; ```--max-missing 0.8``` gives a dataset that is 80% complete (20% missing allowed).

Now we can do the same using ```--max-missing 1.0``` to create a dataset with no missing data.
```
vcftools --gzvcf GPD37_rangewide_Q20SNPsMNPsQC.vcf.gz --max-missing 1.0 --recode --out GPD37_rangewide_Q20SNPsMNPsQC_nomissing
```

Usually, the

#### Step 3a. Output the SNP data as a numerical matrix

To do this, we will use the --012 option to output the SNP data as a numerical matrix that we can use for a PCA, heatmap and other analyses and visualizations. 





-output a Hardy-Weinberg p-value for every site in the vcf file



:::info
:pushpin: Want to learn more? ➜ [HackMD Tutorials](https://hackmd.io/c/tutorials) 
:::

---


