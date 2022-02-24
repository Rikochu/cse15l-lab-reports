# **CSE 15L Lab Report 4**

## Rishi Munagala

## Week 8:

Used CommonMark demo site to see what should be produced: 
  
  **Snippet 1)**
  ![Image](snip1.JPG)
  
  **Snippet 2)**
  ![Image](snip2.JPG)
  
  **Snippet 3)**
  ![Image](snip3.JPG)
 
***

**[My MarkdownParse](https://github.com/Rikochu/markdown-parse)**
   
  Output of my MarkdownParse:
  ![Image](mine.JPG)
   
  **Snippet 1)**
  
  I think it would need to be a small change fix. Checking if the character at the index before the open bracket is a backtick can avoid including the false links. Also to fix the issue where the bracket inside the bracket causes the link not to be included can be fixed by checking if the next closed bracket is before the next open bracket or if there is no next open bracket. This would then allow the code to use the second open bracket rather than the one that should be considered part of the text. 
  
  **Snippet 2)**
  
  
  **Snippet 3)**
  

 ***

 **[Reviewed MarkdownParse](https://github.com/kathyychenn/markdown-parse)**
   
  Output of Reviewed MarkdownParse:
  ![Image](katy.JPG))

