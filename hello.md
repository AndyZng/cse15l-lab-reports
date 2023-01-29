# CSE 15L Lab Report #1
---
## Step 1: Install VScode
* Go to [VScode download](https://code.visualstudio.com/download) and download the version of VScode that corresponds to your operating system. 
<img width="960" alt="VScode download sc" src="https://user-images.githubusercontent.com/115373033/212522753-75a5c17f-500a-4fee-ad5e-67a8b5cf9ac2.png">

* Then open a new terminal in VScode 
<img width="423" alt="image" src="https://user-images.githubusercontent.com/115373033/212522837-39890bd9-c901-4546-aa8f-c908a0cd9cdf.png">

## Step 2: Connecting to the server
* In the terminal, type ssh `cs15lwi23xxx@ieng6.ucsd.edu.` Replace xxx with your own account letters.
* The terminal will ask you to type yes or no. Type yes.
It should look something like this:
<img width="519" alt="image" src="https://user-images.githubusercontent.com/115373033/212523068-91ce405d-b222-4f64-a7b2-e77a2885f36c.png">

## Step 3: Trying out commands 
Now you can type commands into the terminal and do things like change your directory 
Try some commands such as:
* `cd ~` to change the directory to the home directory
* `cd` to change the directory 
* `ls -lat` to list the files in the current directory in long format including the time they were last modified 
* `ls -a` to list all files in the current directory
* `ls /home/linux/ieng6/cs15lwi23/cs15lwi2xxx` and replace xxx with your own id. This lists the files in the specified directory
* `pwd` to view where you currently are
* `cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/` to copy a hello.txt to the home directory
* `cat /home/linux/ieng6/cs15lwi23/public/hello.txt` to concatenate and display a file's contents

<img width="678" alt="image" src="https://user-images.githubusercontent.com/115373033/212523627-acfd36ab-5a62-4384-925f-358b71adb14c.png">
<img width="836" alt="image" src="https://user-images.githubusercontent.com/115373033/212523637-443bcb0a-b707-4775-a87d-e1a91991346d.png">

In this step, I tested out these commands and found that being on a remote server parallels being on a personal device. Using the cd command lets you change your working directory into whatever you want, and using the ls command lets you view the files which exist in that directory. The cp command lets you copy files from one directory to another, and the cat command lets you view the contents of a file. When running these tests, I saw that some of the commands did not work because the files did not exist, so make sure that the files you are trying to work with exist.




