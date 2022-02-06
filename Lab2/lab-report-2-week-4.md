<p align="center">
    <h1 align="center">CSE 15L: Lab Report 2</h1>
</p>

<p align="center">
  <img width="200" height="200" src= "lol.JPG">
</p>

# Introduction

* This lab report will be discussing the relationship between the bug, the symptom, and the failure inducing input in the codes written during lab 3 and 4.

---

# Code Change 1

![image](sc1.png)

### Failure-inducing input: [test1](https://github.com/Quanzat/markdown-parse/blob/main/test1.md)

### Run Command
```
javac MarkdownParse.java
java MarkdownParse test1.md
```

### Output

* Below is the output before the code was changed as shown above in the picture.

```
Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 19
        at java.base/java.lang.String.checkBoundsBeginEnd(String.java:3751)
        at java.base/java.lang.String.substring(String.java:1907)
        at MarkdownParse.getLinks(MarkdownParse.java:18)
        at MarkdownParse.main(MarkdownParse.java:26)
```

<p align="right">
    <h4 align="right">(Figure. 1)</h4>
</p>

### Discussion

* In this case, the bug in this failure-inducing code is that `[a link!] google.com` is in a wrong format because it doesn't have parenthesis around `google.com`. As a result the symptom of this code throw an `IndexOutOfBoundsException` (Figure. 1). This is because after the code is run, index for `closeParen` is at `-1`, which is out of bound.

### Solution

* The solution that our group came up together is to include an `if` statement (Figure. 2) to account for a bug input where no parenthesis is found.

```
if (markdown.indexOf('(') != -1)){
  ...
}
```

<p align="right">
    <h4 align="right">(Figure. 2)</h4>
</p>

---

# Code Change 2

![image](sc2.png)

### Failure-inducing input: [test2](https://github.com/Quanzat/markdown-parse/blob/main/test2.md)

### Run Command
```
javac MarkdownParse.java
java MarkdownParse test2.md
```

### Output:

* Below is the output before the code was changed as shown above in the picture.

```
[youtube.com]
```

<p align="right">
    <h4 align="right">(Figure. 3)</h4>
</p>

### Discussion

* In this case, the bug in this failure-inducing code is that `link (youtube.com)` is in a wrong format because it doesn't have bracket around `link`. As a result the symptom of this code would still return a link when it not supposed to. The correct output of this failure-inducing code should of been `[]` and not `[youtube.com]`.

### Solution

* To fix this bug, our group came up with the idea of adding in another `if` statement (Figure.4 ) to make sure that the code would not return if either bracket or parenthesis is missing. With this fix, the code would only return the link if both bracket and parenthesis is found. 

```
if (markdown.indexOf('(') != -1) && markdown.indexOf("[") != -1){
  ...
}
```

<p align="right">
    <h4 align="right">(Figure. 4)</h4>
</p>

---

# Code Change 3

![image](sc3.png)

### Failure-inducing input: [test3](https://github.com/Quanzat/markdown-parse/blob/main/test3.md)

### Run Command
```
javac MarkdownParse.java
java MarkdownParse test3.md
```

### Output:

* Below is the output before the code was changed as shown above in the picture.

```
[google.com]
```

<p align="right">
    <h4 align="right">(Figure. 5)</h4>
</p>

### Discussion

* In this case, the bug in the failure-inducing code is that there is a space between `[link]` and `(google.com)`. The symptom of the program gave us `[google.com]` (Figure. 5). This is wrong because the correct format of link should include no space in between and if there is space, it should of return `[]` instead of a link. 

### Solution

* To fix this code, our group added in one more `if` statement (Figure. 6) to ensure that the input code should have no space between `[link]` and `(google.com)`. Otherwise, if this `if` condition is not met, then it would just end the program and return `[]`.

```
if (openParen-nextCloseBracket == 1){
    toReturn.add(markdown.substring(openParen + 1, closeParen));
}
```

<p align="right">
    <h4 align="right">(Figure. 6)</h4>
</p>

---
<p align="center">
    <h1 align="center">The End</h1>
</p>
<p align="center">
    <h1 align="center">Thank you for reading.</h1>
</p>

---