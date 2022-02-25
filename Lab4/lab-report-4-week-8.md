<p align="center">
    <h1 align="center">CSE 15L: Lab Report 4</h1>
</p>

<p align="center">
  <img width="200" height="200" src= "lol.JPG">
</p>

# Introduction

* This lab report will be discussing errors and fixes with provided code snippets to test the implementations of MarkdownParse. 

---

# Code Repositories

* Below is two code implementation that we will be reviewing for this lab report. 

## My Implementation

* [MarkdownParse](https://github.com/Quanzat/markdown-parse)

## Reviewed Implementation

* [Reviewed MarkdownParse](https://github.com/Darrengn/markdown-parse)

---

# Snippet 1

## Snippet Output

![image](s1.png)

## Expected Output

```[`google.com, google.com, ucsd.edu]```

## My Implementation

### Test code

![image](mytest1.png)

### Test Output

![image](myso1.png)

### Discussion

* For this bug, it is doable to fix this code with changes that is less than 10 lines of code. We achieve this by adding in a couple lines that would check the indexes of backticks, brackets and parenthesis. The logic for this code would be something along the line of checking for the indexes of backsticks and comparing it with parenthesis. Then it would return the link if no link is within the indexes of open and close backsticks. This code logic would also ignore backsticks if and only when both open and close backsticks are in front or when a close backstick is behind a close parenthesis. With this condition, no link is within backsticks and so it should return normally. 

## Reviewed Implementation

### Test code

![image](retest1.png)

### Test Output

![image](reso1.png)

---

# Snippet 2

## Snippet Output
![image](s2.png)

## Expected Output

```[a.com, a.com(()), example.com]```

## My Implementation

### Test code

![image](mytest2.png)

### Test Output

![image](myso2.png)

### Discussion

* This code is not fixable with any code that is less than 10 lines. Firstly, we need to consider that some code within this snippet work while others do not. Moreover, the third code did not even produce an output at all. To fix this we would need to add in some lines that would check for each specific condition. Therefore, these errors and its complexity would require more than 10 lines to fix as each case would need to be considered. 

## Reviewed Implementation

### Test code

![image](retest2.png)

### Test Output

![image](myso2.png)

---

# Snippet 3

## Snippet Output
![image](s3.png)

## Expected Output

```[https://ucsd-cse15l-w22.github.io/]```

## My Implementation

### Test code

![image](mytest3.png)

### Test Output

![image](myso3.png)

### Discussion

* Considering this bug, it is possible to fix the code within 10 lines as we would need to add in some code with the logic that it continue checking for next indexes until it reaches a close bracket or close parenthesis. Moreover, if there is empty lines in between, then the code should move on to the next index. With this logic, the code should keep checking until it completely go through the entire snippet and treat it as there were no empty indexes in between. 

## Reviewed Implementation

### Test code

![image](retest3.png)

### Test Output

![image](reso3.png)

---
<p align="center">
    <h1 align="center">The End</h1>
</p>
<p align="center">
    <h1 align="center">Thank you for reading.</h1>
</p>

---