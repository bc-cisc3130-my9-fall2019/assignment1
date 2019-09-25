# Testing Procedures (Grading rubric)

The assignment objective was to create an output that matches the following rules:

- 2 columns of information for each word in an input file
- The first column produces either `true` or `false` value
- The second column produces a sorted order of the characters in lowercase

Note: An implied rule that wasn't explicitly stated as a bullet point in the assignment description but could be inferred from the output example, is for the boolean value in the first column to be true for the second column. 

---

## Test cases

The examples given were a very small sample, not at all a good representation of comprensive use cases - for example, all the repeated letters were right next to each other, and all the upper case letters appear earlier in the alphabet.

```
hello 
world
Brooklyn
College
```

When testing your code, I came up with other test cases to handle edge conditions such as: 

```
Testing    # an upper case letter that isn't the _smallest_ value, and a repeated letter that is not adjacent and not the same case

XYZabc     # upper case letters come before lowercase by most operating systems, this test whether you've lowercased before sorting in your logic

a1B2C3     # after sorting, 123 should come before abc
```

## Running test on CLI

I run the code, passing in the `[test.txt](test.txt)` input file with the linux `<` command and then output the entire result using the `>` command into `key.txt`

```
⋊> ~/a1 on master ⨯ javac Answer.java
⋊> ~/a1 on master ⨯ java Answer < test.txt > key.txt
⋊> ~/a1 on master ⨯ cat key.txt
false	ehllo
true	dlorw
false	bklnoory
false	ceegllo
true	1cemoprtu
false	13ccens
false	aelpp
true	ilnux
false	011dnosww
true	abcxyz
true	123abc
false	3ilmsss
true	eijmos
false	aaccerr
false	eginstt
```

I compile and run your code to see how it compares with the expected output. 

```
⋊> ~/a1 on master ⨯ javac SortInput.java
⋊> ~/a1 on master ⨯ java SortInput < test.txt > test_output.txt
```

now that I have the two versions, I can compare the outputs using the command line [diff](https://linux.die.net/man/1/diff) tool. You can check the local manual from your command line using the `man` command for manual, like `man diff`. Here I've used the `-w` flag to ignore whitespace because not everyone properly formatted with a tab space in between the columns.

```
⋊> ~/a1 on master ⨯ diff -w key.txt test_output.txt
```

This would show me which lines have errors, to which I can then deduce where your code may not have had the right logic.

___

# Example of output

```diff
4c6,4c6
< false    bklnoory
< false    ceegllo
< false    aelpp
---
> false	Bklnoory
> false	Ceegllo
> false	PPael
8,9c8,9
< true    abcxyz
< true    123abc
---
> true	XYZabc
> true	123BCa
```

---

Grading scale

```
5 - Meets all the criteria
4 - Meets most of the criteria
3 - Meets some of the criteria
2 - Meets few of the criteria
1 - Submitted but for some reason couldn't run the code
0 - Not submitted.
```
