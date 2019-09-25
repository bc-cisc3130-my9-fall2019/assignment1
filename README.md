# cisc3130-assignment1

Instructor: Katherine Chuang \
Section: MY9 \
Brooklyn College

## Setup

If you've never used github.com before, create an account. You'll have to add the ssh keys from where your local machine to your github account [instructions](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account). You have to add the ssh keys from each machine you want to use to interact with Github.com. 

1. Go to the github classroom assignment link https://classroom.github.com/a/tBPtyLsb, it will create a repository for you. 
2. Clone the repository to your local machine [instructions](https://help.github.com/en/articles/cloning-a-repository). If you're on a linux terminal it's `git clone <repo url>`
3. This will save a directory with the repo name on your machine, go into that folder to find your files. If you're on a linux terminal: `cd <repo folder>` 
3. When you're ready to upload files, save your file(s) and then you want to commit and push. [instructions](https://help.github.com/en/articles/pushing-commits-to-a-remote-repository) If you're on a linux terminal, `git add filename` followed by `git commit -m "log message"` followed by `git push origin master`



## Objective
Read a text file (one word per line) and output information about whether the word is composed of unique characters and then output each word in its sorted order. From here on, *function* and *method* are used interchangeably to indicate a code block that has input and output.

1. `isUniqueChar()` function determines if a string has all unique characters, complete this function.
2. Edit the `sortWord()` function so that uses the InsertionSort() function to convert all letters to lowercase and print out the sorted characters for the word. 

Assume these functions will be called from the main function and return per line the output of each.  To get you started you can use these two files as a starting point. Note that there are errors in the file that you'll have to fix in order to complete the assignment, how you fix it will be up to your personal preference. 

Furthermore, the exact design of how your functions will take input parameters and the types of your inputs & outputs is up to you to decide. For example, perhaps you prefer to print from each function instead of passing values back. Perhaps you prefer working with Character inputs instead of String. These are decisions you should think about and how it can affect other parts of the code.

You may find it useful to write out pseudocode to design a strategy of how your code will work before beginning the actual coding task. You may even change the name of the functions if you like. You have the freedom to design your program. I will be checking your output format first and foremost so try to keep that consistent. Feel free to discus with classmates about strategies and design but do try to write your own code to maximize your learning opportunity. 

There is some artistic aspect to programming; this assignment is designed so that there's no one single right answer to complete the objective. Do use analytical thinking to assess whether your strategy and design are effective, if your code can be further improved. 

---

You can reference the [Java Docs](https://docs.oracle.com/javase/8/docs/api/index.html?overview-summary.html) or anything on the Internet. 

Instructions for usage by command-line can be found in the [Example.java](Example.java).

You may use [input.txt](input.txt) as a test case. The contents of the input.txt file:

```
hello
world
Brooklyn
College
```

The output for that input file should look like: 

```
false	ehllo
true	dlorw
false	bklnoory
false	ceegllo
```
#### Format

In each line you have the `true/false` value followed by a tab space, followed by the word in sorted order (lowercase).

---

## Submission
If possible, submit the completed work via the GitHub Classroom link. Use of this platform is still experimental, so it may or may not work. 

In the case that Github Classroom doesn't work - you can email me the Java source code before the deadline.   You should submit the `*.java` file, not the compiled version. Please comment with your first and last name somewhere in that file so I can identify you for grading. 

## Grading
I will be looking for the following characteristics amongst other critera:

* That it works. That the Java file submitted compiles and gives an output. Should be following the expected output format. You are welcome to attach an example of input and output for me to refer to that it works for your test case(s), however I will be using my own test case with lowercase alpha characters and numbers.
* Commenting of your code - describe the function, expected inputs, any error or exception handling. 
* Readability is important, so is the impression you want to give on your code. Try to use good principles of naming, use of comments, spacing, etc.
* I'll try to compile the source code with command-line using `javac SortInput.java` and then running with `java SortInput < input.txt`, so if there's another way to compile and run do let me know.

