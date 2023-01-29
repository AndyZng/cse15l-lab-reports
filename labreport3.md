# Lab Report #2
---

## Part 1: String Server
>Code for the string server

<img width="960" alt="image" src="https://user-images.githubusercontent.com/115373033/215318073-6f7e5071-2c83-4e61-8e42-dae46d0ff340.png">

This code uses the method `handleRequest`, which takes in a url and splits its path and adds the string in the path into the list of words to be displayed on the page.
The URL should have a `add-message?s=` before the desired string to be added in order for the method to split the url correctly. 

>Screenshots of the site

<img width="457" alt="image" src="https://user-images.githubusercontent.com/115373033/215318732-6338f483-4e0d-473f-be56-8f2576286a0b.png">
<img width="415" alt="image" src="https://user-images.githubusercontent.com/115373033/215318769-d825d63f-14d9-4aab-a250-93c6bbd8ba86.png">

The values that are processed by the method are "hello", and "goodbye", and they are concatenated to `string a` which is then displayed on the site. 

## Part 2: A bug from Lab 3
>Snippet of buggy code

<img width="320" alt="image" src="https://user-images.githubusercontent.com/115373033/215319111-9559f726-9623-41a7-bff6-51df22c180ed.png">

This method intends to reverse the contents within an array, however it does not work as intended all the time. 

>Junit testing of method

<img width="960" alt="image" src="https://user-images.githubusercontent.com/115373033/215319725-61f54fee-a340-4bcd-bb39-a6c6f0d4a179.png">

Here, we see that inputs with lengths less than 2 like { } and {1} had corrected outputs. However, when the length was increased in an input like {1, 2, 3}, the output
differed from the expected. 

<img width="401" alt="image" src="https://user-images.githubusercontent.com/115373033/215319945-a7edd251-4942-4f0e-9686-02fb0bf38d7b.png">

From the error message, we can see the symptom of the bug, which is that the method wrongly reverses the array. Instead of {3, 2 ,1}, it outputs {3, 2, 3}

>Fixed code

<img width="333" alt="image" src="https://user-images.githubusercontent.com/115373033/215320105-cf43ce97-0dea-49ce-8f11-3207a3a2fc13.png">
The problem with the original code was that the method was changing the values within the array as it was reversing it. The solution to this was to make a hard copy of the array being passed in and iterating through it backwards to assign it into the original array. This fixed the issue of wrongly replacing items in the original array. 

## Part 3: What I learned

One of the main things I learned in labs 2 and 3 was how to create a site on a local host and passing in arguments through the search bar to make the site display certain things. The creation of the server involved using java.URI and a URL Handler, and the path of the URL could be split to pass in a certain desired part of the URL into the back end code of the site and perform functions that are coded by the creator.  





