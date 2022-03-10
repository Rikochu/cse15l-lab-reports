# **CSE 15L Lab Report 5**

## Rishi Munagala

## Week 10:

**How to find different results:** 
  
In order to find the different results between my markdownparse and the provided implementation, using the command `diff` on the `.txt` files that had the outputs of all files listed would work. To create the file with the list of outputs, creating a bash file that runs a for loop on each file and prints the output is needed. Then using the command `bash (name of script file).sh > (name of txt file).txt` allows the output of each file to be saved on each line of the file.

***

**Test 530.md:**
  
  `[![moon](moon.jpg)][ref]`
  
  **Output:**
 
  ![Image](530diff.JPG)
  
  For this case, I think that my implementation is correct. The difference here by the image above is that my implementation returns an empty list while the given implementation returns a list including `moon.jpg` which is an image link. An image link is different than a link that `MardownParse.java` should return so this input should return an empty list.
  
  To fix this, would be be have an `if` statement that checks for image links specifically. The image below shows the code from my implementation where it considers if an `!` is before the open bracket and continues without return that link. The given implementation should use a similar check.
  
  ![Image](fix2.JPG)
 
***
 
 **Test 523.md:**
  
  `[foo <bar attr="](baz)">`
  
  **Output:**
 
  ![Image](519diff.JPG)
  
  In this case, I think that my implementation shows the correct output but does not cover the issue. The correct output can be confirmed by the commonmark demo screenshot below. Common mark shows that this input should not be considered a link due to the `<` inside the brackets. Even though my implementation shows the right output, my code does not consider this case.
  
  ![Image](correctput.JPG)
  
  The given implementation does not consider if there is a less than carrot. To fix this, there needs to be a check on whether there is a less than carrot and if that index is in between the open and closed brackets. If it is, similar to with image links, it should continue without adding that link. Below is the screenshot of the code changes to consider the case on my implementation. Creating a similar check will fix the issue on the given implementation.
   
   ![Image](fix3.JPG)

***


