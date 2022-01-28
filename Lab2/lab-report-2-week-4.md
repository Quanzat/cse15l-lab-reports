<p align="center">
    <h1 align="center">CSE 15L: Lab Report 2</h1>
</p>

<p align="center">
     <img width="200" src= lol.JPG 
 </p>

# Introduction

* This lab report will be discussing the relationship between the bug, the symptom, and the failure inducing input in the codes written during lab 3 and 4. 

---

# Code Change 1

![image](sc1.png)

* Failure-inducing input:
    * [test1](https://github.com/Quanzat/markdown-parse/blob/main/test1.md)

* Output:

```
Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 19
        at java.base/java.lang.String.checkBoundsBeginEnd(String.java:3751)
        at java.base/java.lang.String.substring(String.java:1907)
        at MarkdownParse.getLinks(MarkdownParse.java:18)
        at MarkdownParse.main(MarkdownParse.java:26)
```

* Discussion:
    * temp




---
# Code Change 2

![image](sc2.png)

* Failure-inducing input:
    * [test2](https://github.com/Quanzat/markdown-parse/blob/main/test2.md)

* Output:

```
[(youtube.com)]
```

* Discussion:
    * temp




---
# Code Change 3

![image](sc3.png)

* Failure-inducing input:
    * [test3](https://github.com/Quanzat/markdown-parse/blob/main/test3.md)

* Output:

```
[(google.com)]
```

* Discussion:
    * temp


