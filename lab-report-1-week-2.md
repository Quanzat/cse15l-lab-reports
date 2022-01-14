<p align="center">
    <img width="200" src= https://images1.content-hci.com/commimg/myhotcourses/blog/post/myhc_89683.jpg
</p>

<p align="center">
    <h1 align="center">CSE 15L: Course-specific Account and Ieng6 Computer</h1>
    </p>
</p>

---

## What is a course-specific account?

* A course-specific account is an account created for students in specific courses (i.e., CSE 12, CSE 15L, etc...).
* An example of a course-specific account look like this: cse15lwi22zz@ieng6.ucsd.edu
* The "zz" is replaced by specific assigned letters to each student.

## How to gain access to a course-specific account?
* First, in order to gain access to a course-specific account, you must go to https://sdacs.ucsd.edu/~icc/index.php and look up your assigned account address. 

<p align="center">
    <img width="1000" src= accountlookup.png
</p>

* Second, you will then need to enter your UCSD username and Student ID, which will prompt information about what course-specific account belongs to your student ID.

<p align="center">
    <img width="1000" src= 2.png
</p>

* You will be asked to change your password in order to activate your course-specific account. This process will take up to severals minutes for the changes to take effects. (Note: You can your current PID password if it met all the requirements.)

<p align="center">
    <img width="1000" src= passwordchange.png
</p>

## How to access Ieng6 Computer?
* There are two ways to access the Ieng6 computers. The first is to access them on campus in the CSE building. The second way is to access them remotely. For this course specifically, you will be using <strong> Visual Studio Code </strong> to remotely access to these computer and do work on them. 
* To connect remotely, you will need your course-specific account and password that you have set in order to activate that account to log into the computer. 

## What is Visual Studio Code and how to get it?
* This is an IDE which is also known as a code editor. It work like any other code editors out there. 
* You can obtain it by either search it up or go to this link here: https://code.visualstudio.com/
* There is a version for every platform out there so no need to worries about device compatibilities.

<p align="center">
    <img width="1000" src= vscodedownload.png
</p>

## What to do with Visual Studio Code?
* Once you have obtain Visual Studio Code, you should see this screen. (Note: It might look different depend on the operating system you are on.)

<p align="center">
    <img width="1000" src= https://ucsd-cse15l-w22.github.io/images/vscode.png
</p>

* From here you will then open terminal. To achieve this, you either use keyboard short cut (Ctrl or Command + `) or navigating to Terminal --> New Terminal. 

<p align="center">
    <img width="1000" src= terminal.png
</p>

## Accessing Ieng6 Computer Remotely

* In terminal, you will run a secure shell to the ieng6 computer with your course-specific address. Use the following command to begin (Note: The "zz" is replaced with your specific assigned letters): 
    
    `ssh cs15lwi22zz@ieng6.ucsd.edu`

* For the first time connecting, you will get this message similar to the image below. All you need to do is type "yes". 

    ```
    The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
    RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
    Are you sure you want to continue connecting (yes/no/[fingerprint])? 

    ```

*You will then be prompt to enter your password (Note: While typing your password, nothing will appear on the screen and that is to be expected. Just continute and press enter once you done typing it).

<p align="center">
    <img width="1000" src= 
</p>

