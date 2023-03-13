# Lab Report 4
---

## Step 1: Logging onto ieng6. 
Using an ssh key, I was able to log onto ieng6 simply by typing and entering `ssh cs15lwi23aux@ieng.ucsd.edu` without using my password.

<img width="552" alt="image" src="https://user-images.githubusercontent.com/115373033/221456268-271a7c08-461c-46cd-930e-13518174876b.png">

The ssh key was made by following these steps:

<img width="403" alt="image" src="https://user-images.githubusercontent.com/115373033/221457155-79cb1b6b-3c07-42ab-b47b-72dc65d504c0.png">


## Step 2: Cloning the fork of the repository from my Github account

I first forked the lab7 repository by clicking the fork button.

<img width="241" alt="image" src="https://user-images.githubusercontent.com/115373033/221459074-94490b2a-ea3d-45b4-b607-42b6ae839558.png">

Then I typed and entered `git clone <link of repo>` into the terminal to clone the repository to ieng6.

<img width="481" alt="image" src="https://user-images.githubusercontent.com/115373033/224581372-53b9c9be-8423-4a04-82f7-40cee783905e.png">

## Step 3: Checking that the JUNIT tests fail

In order to run the JUNIT tests, I had to first change directories to lab77 by entering `cd l` and then pressing `<tab>` to auto complete to the lab7 directory.

<img width="233" alt="image" src="https://user-images.githubusercontent.com/115373033/221460726-0001a38d-3849-46e4-894d-ea863c75437a.png">

To find the file to be tested, I used `ls`, which listed all of the files in the lab7 directory. 

<img width="625" alt="image" src="https://user-images.githubusercontent.com/115373033/221462055-bf6ebfe2-08a3-42c5-8040-b488321bec21.png">

Next, I copied `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore <Test file>` from the week 3 lab manual and ran them in the terminal sequentially. For the second command I typed `L` then pressed `<tab>`, then typed `T`, then pressed `<tab>` again in order to auto complete to ListExamples.Test. Then I hit `<enter>` in order to run the tests.

<img width="712" alt="image" src="https://user-images.githubusercontent.com/115373033/221462436-e2369e8f-d6d9-4877-8180-aa2d2f40b8a1.png">

## Step 4: Editing the code 

To edit `ListExamples.java` and fix its code, I typed `nano L` then `<tab>` then `.j` then `<tab>` to auto complete to ListExamples.java. I entered this to edit the file.
This was the UI that came up.

<img width="690" alt="image" src="https://user-images.githubusercontent.com/115373033/221462919-cb26f09d-860d-4dc3-92bc-ed19bdc9e5a0.png">

The problem with the file was that the code was iterating the index of the first list when it should have been iterating the index of the second one. In order to edit the error, I pressed the `down` key 43 times until I reached the line which had `index1 +=1` (The second occurrence of that line) Then I pressed the `right` key 12 times until my cursor was right after the `1`. I then deleted the 1 and replaced it with a `2`. 
> Before

<img width="379" alt="image" src="https://user-images.githubusercontent.com/115373033/221463412-fd3eb842-9203-4bf6-be6c-208140f9c866.png">
> After

<img width="387" alt="image" src="https://user-images.githubusercontent.com/115373033/221463469-414fa6a9-4d43-4bfe-b8d0-c105aea6d164.png">

To save the changes, I used `ctrl + O` and then `<enter>`, and I exited nano by using `ctrl + X`.

<img width="424" alt="image" src="https://user-images.githubusercontent.com/115373033/221463693-71f9d8f1-c818-43b1-8fe2-ae6be5776407.png">

Now I am back in the terminal

<img width="327" alt="image" src="https://user-images.githubusercontent.com/115373033/221463806-428ad15b-6222-4d1e-9a40-cd9db1f08ebb.png">

## Step 5 Running the new code

To run the new code against the JUNIT tests, I simply pressed the the `up` key 3 times to find my previous compile command. I then hit `<enter>` to recompile the files.

<img width="563" alt="image" src="https://user-images.githubusercontent.com/115373033/221464000-39eea76f-a1fe-42d9-a3be-19489d9bdeae.png">

Then I pressed `up` 3 times again to find my previous JUNIT running command. Then I pressed `<enter>` to run the tests. We see that the tests all pass now.

<img width="707" alt="image" src="https://user-images.githubusercontent.com/115373033/221464188-118c9429-47ec-4a61-9409-99e48e6c6e1e.png">

## Step 6 Committing and Pushing the change to Github

Before starting this step, I had to first make an SSH Key for github by following these steps:

<img width="354" alt="image" src="https://user-images.githubusercontent.com/115373033/221479633-1c112b8c-faa3-4750-9b32-09cbc890a94a.png">

Then I had to change my push protocol to ssh protocol by entering `git remote set-url origin git@github.com:AndyZng/lab7.git` (which has no output)

<img width="516" alt="image" src="https://user-images.githubusercontent.com/115373033/224581190-c8646fbe-fc00-403b-8bbe-2b26156b1422.png">

Now I was ready to stage the changes by using `git add <File Name>` This was followed by using `git commit -m "<message>"` to actually commit the changes.

<img width="409" alt="image" src="https://user-images.githubusercontent.com/115373033/221479791-2d1d33a4-fb6f-4007-8cbd-9317452be116.png">

Finally, I pushed my changes to Github by using `git push`

<img width="568" alt="image" src="https://user-images.githubusercontent.com/115373033/221480183-b7e37f1c-11b8-44cd-b404-9c183b2f0655.png">

We can see that the repository has been updated on Github.

<img width="657" alt="image" src="https://user-images.githubusercontent.com/115373033/221480265-ed6b7b05-4452-4407-a80e-9de9b23f3bc1.png">



















