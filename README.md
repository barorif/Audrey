# Introduction to the awk Language

awk is a general-purpose pattern scanning language available with the Coherent operating system. awk performs pattern matching, string manipulation, record processing, and report generation. 

The syntax for awk is simple. It uses only one kind of statement, consisting of one or  both of two elements: a *pattern* and an *action*. Patterns select the data to be processed, and actions specify the function to be performed on the selected data.

This tutorial explains how to write awk programs to process input. It will teach you how to use the awk interpreter and how to create an awk program. It describes the basic function of printing and the specification of input and output field and record separators. It explains the pattern scanning capabilities of awk Finally, it describes the actions awk performs in addition to printing, such as assigning variables, defining arrays, and controlling the flow of data.

## Using awk

awk reads input from the standard input (entered from your terminal or from a file you specify), processes each input line according to a specified awk program, and writes output to the standard output. This section explains the structure of an awk program and the syntax of awk command lines. 

### Program Structure

The basic element of an awk program is a statement in the form: 

    pattern {action}

awk checks each line of input with the *patterns* specified for a match, one pattern at a time. Each time the line matches a pattern, awk performs the corresponding action. After awk has compared the line with each pattern in the program, awk tests the next input line against the patterns.

An awk program may specify an action without a pattern. When awk processes an action which has no pattern, each input line matches. Therefore, awk performs the action on every line of input.

An awk program may also specify a pattern without an action. In this case, when an input line matches the pattern, awk prints the line to the standard output.

One of the special patterns that awk recognizes is the word FILENAME. This pattern causes awk to print the name of the file that it is reading. Other special patterns are discussed below.
