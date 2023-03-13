# Lab Report 5 (Lab 6)
---

## Getting Started on Making a Grading Script
During week 6, we had to create a grading script which would be run against different mock student submissions. The student submissions each contained different 
implementations of `ListExamples.java`, which was the file that the script would run Junit tests on. 

## Breakdown of the Script
1.

First, the path `CPATH` is directed to `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar` in order to reference the path in the future. I included `set +e` in order
to ensure the script didn't exit immediately after running into an error. This made it so I could see the rest scripts outputs even when there were errors. Before 
using `git clone` to clone the repository link (`$1`), I made sure to remove any contents that already existed in student-submission. I then cd'ed into 
student-submission and checked if `ListExamples.java` existed using the `-f` command. I also used `cp` to copy the Junit test file `TestListExamples` into student-submission.
Finally, I compiled` ListExamples.java` and directed the standard error output into `error1.txt`.

<img width="567" alt="image" src="https://user-images.githubusercontent.com/115373033/224608702-eae4dbed-ead2-48a9-9fe6-e1fa547381f2.png">

2.

Next, I checked to see if there were any words in `error1.txt` and used this to determine whether or not there was a compile error. If there weren't any, the script would 
continue by copying the Junit files in `lib` to student-submission and compiling and running the Junit tests in the directory. The results of the tests were directed inte 
`results.txt`, which is concatenated to show the user where their errors were. I created variables `num_tests` and `num_fails` and grepped the number of Tests ran and failures 
in them respectively.

<img width="694" alt="image" src="https://user-images.githubusercontent.com/115373033/224605974-8f906836-9d33-42dc-8818-c974cc6693be.png">

3.

Finally, I checked if there were any instances of "FAILURES" in `results.txt` and directed the lines to `failCheck.txt` I also checked the method header of the submission file
by grepping the correct method signature to see if it existed in the submission. Finally, if there were no words in `failCheck.txt`, the script would output that the submission 
passed. If there were, then it used the variables `num_tests` and `num_fails` to output the user's score.

<img width="614" alt="image" src="https://user-images.githubusercontent.com/115373033/224606112-fce44aa0-4a2f-477e-9f9b-9f1d145a7651.png">

## Running the Script

* Running against incorrect implementation:

<img width="541" alt="image" src="https://user-images.githubusercontent.com/115373033/224607815-34b0050d-c1d4-47a3-8945-e9787b582331.png">

We can see that the script produces a failure result and gives a score of 0%.

* Running against correct implementation:

<img width="424" alt="image" src="https://user-images.githubusercontent.com/115373033/224608383-b0276198-0d66-44c2-b085-3ce369991c02.png">

We can see that the script produces a passed result and gives a score of 100%.

* Running against compile error:

<img width="435" alt="image" src="https://user-images.githubusercontent.com/115373033/224608561-c9fea359-9f21-4421-9b63-d7d5fde0c701.png">

We can see that the script produces a compile error result and gives a score of 0%.

* Running against incorrect method signature:

<img width="424" alt="image" src="https://user-images.githubusercontent.com/115373033/224608868-c2ebea8f-2f56-4b9e-bebf-640bbf4629eb.png">

We can see that the script alerts the user about an incorrect method signature. However, the tests still pass, so the user receives a pass and a score of 100%.

* Running against incorrect file name and nested directory:

<img width="466" alt="image" src="https://user-images.githubusercontent.com/115373033/224609048-44886b3b-2486-42f3-b178-499c6a0e04f0.png">

Both cases produce the same output. The script tells the user to check the file name and directory.

## Reflection: Things I learned, and Things I did differently.

In making this script, I was surprised to see all the ways that a bash script can run commands. It was really interesting to see how I could cd into different
directories, use grep to check for errors, copy files to different directories, and use if statements all in one script. For my original script, I graded on a 
pass/fail basis, meaning that if I found any errors, the script would just output fail instead of outputting a score. Using Chat-GPT, I learned about the `grep -oE`
command, which allowed me to get solely the number of tests ran and failed. I also used Chat-GPT to learn how to perform arithmetic in the script. It gave me the line 
`score=$((100 * (num_tests - num_fails) / num_tests))`, which let me calculate the percentage that the user would receive no matter how many test cases there were. 












