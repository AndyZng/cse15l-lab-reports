# Lab Report 3
---

## Other Grep Commands

1. `grep -i "pattern" <file>` searches through the desired files for the pattern without any case sensitivity and returns the lines where the pattern appears. This is useful if we want to find all instances of a pattern regardless of its casing.

> For example, when I search for "american revolution", the file is still returned despite the actual text being capitalized 
<img width="654" alt="image" src="https://user-images.githubusercontent.com/115373033/218630476-ac2b87ad-62a3-4569-8d73-31d2d88e48ea.png">

 > Whereas searching for the same thing using the regular grep command yields no result
<img width="641" alt="image" src="https://user-images.githubusercontent.com/115373033/218630913-3322a584-2f21-4c2b-b62e-2d3e893be34d.png">

> Here is another instance of grep -i searching for "ANCIENT ROME". We can see that it returns all of the lines that contain "Ancient Rome" without regard to
 capitalization. It is also important to note that the search is being done within all of the text files and not on the names of the text files. 
 
<img width="747" alt="image" src="https://user-images.githubusercontent.com/115373033/218632029-d8fe167d-5ca5-469e-8744-491debdaa06a.png">

2. `grep -r "pattern" <directory>` searches recursively throughout the entire directory and all of its subdirectories to find lines that match the pattern. This can be useful as it lets us search for a pattern in a whole directory without knowing where it actually is.

 > In this example, grep -r searches for the patter "computer science" throughout every file within the written_2 directory. This means that it searches through the
 non-fiction and travel guide directories and all of their subdirectories. Here, grep found one file containing "computer science" in the non-fiction directory.
 
 <img width="825" alt="image" src="https://user-images.githubusercontent.com/115373033/218634317-ea70d364-925b-4cf1-958e-426230a279dc.png">
 
 > Searching for "industrial revolution", grep returns files from the travel guides directory, showing that grep -r traverses through each subdirectory.

<img width="827" alt="image" src="https://user-images.githubusercontent.com/115373033/218634599-b6e35657-b0cc-44ed-9800-6ad4572a5f41.png">

3. `grep -v "pattern" <file>` searches through the desired files for lines that *do not* contain the pattern. This could be useful for filtering out certain files or words. 

> For example, if I wanted to find all the files within written_2 that are not from a non fiction directory, I could do `find written_2 >` a text file and then use grep -v
to find all of the files which don't contain "non-fiction" 

<img width="310" alt="image" src="https://user-images.githubusercontent.com/115373033/218636005-6c410283-38dc-4a0e-a67a-61e8f08cad32.png">

Original text:

<img width="320" alt="image" src="https://user-images.githubusercontent.com/115373033/218637364-071dc68b-8ca0-4259-a230-3d2bc4bc414a.png">

Using grep -v:

<img width="339" alt="image" src="https://user-images.githubusercontent.com/115373033/218636169-882a2a93-aaa6-41b5-a085-4efb0cbeb184.png">

> This can also be used in text files to find all of the lines which do not contain a certain pattern. For example, grep -v "The" would return all of the lines which
 do not contain file in this text. Note: words containing "The", such as "There" are also ommitted. 
 
 Original text:
 
 <img width="827" alt="image" src="https://user-images.githubusercontent.com/115373033/218638338-2f47f2c3-00be-44bf-abbf-16fc089c9577.png">
 
 Using grep -v:
 
<img width="819" alt="image" src="https://user-images.githubusercontent.com/115373033/218638364-12f2e6f3-89a3-47f4-8029-a3cd0cd3770f.png">

4. `grep -C [num] "pattern" <file>` searches for the number of desired contextual lines surrounding the input pattern. In num, we put the number of lines we want to
see before and after the pattern we are searching for. Note: the line containing the pattern itself is also returned. This is useful if we want to find the context around a certain pattern. 

> For example, if I search for 1 line surrounding the pattern "Paris", the command returns the lines before and after (only after in this case since Paris is in the 
 first line of the text).
 <img width="815" alt="image" src="https://user-images.githubusercontent.com/115373033/218641066-560adc70-433e-4cc5-b73f-29e6f9bf8b55.png">
 
> Here is another example where I search for the contexual lines of "Amphrite" in WhereToItaly.txt, where grep returns a line before and after the instance of 
"Amphrite" in the text.

Original text:

<img width="425" alt="image" src="https://user-images.githubusercontent.com/115373033/218641700-fc87f7c6-30aa-44a7-ab23-b2f0d69f1e8a.png">

After using grep -C:

<img width="442" alt="image" src="https://user-images.githubusercontent.com/115373033/218641739-dc48d3cc-a940-4f33-bbac-2e95c96151b8.png">




