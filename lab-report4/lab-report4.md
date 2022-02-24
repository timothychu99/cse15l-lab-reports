[Return to Lab Reports Main Page](../index.md)
## Lab Report 4, Timothy Chu

# Links to the Markdown-Parse Repository and Reviewed Repository
- [My Markdown-Parse Repo](https://github.com/timothychu99/markdown-parse)
- [Reviewed Repo](https://github.com/timothychu99/markdown_parse_2)

# Running the Reviewed Repo Code
![](TestSnippetsCode.png)

![](SnippetOutpustOwnTests.png)
- It shows that it failed on all Snippet1, Snippet2 and Snippet3.
- In the code, it shows the line java.lang.assertionError with the expected and what it found.
- It shows on the at MarkdownParseTest.testSnippet line the place where the error occured in the MarkdownParseTest.java file.


![](RunReviewedSnippetTests.png)
- It shows that it failed on Snippet1 and Snippet3 but passed on Snippet2.
- In the code, it shows the line java.lang.assertionError with the expected and what it found for Snippet1 while index out of bound exceptions for 
Snipping2 and Snipping3.
- It shows on the at MarkdownParseTest.testSnippet line the place where the error occured in the MarkdownParseTest.java file.

# Question Answers
- It will take more than \>10 lines to change my program to work with backticks. To work for backticks, it must be able to track where the backtick starts 
and ends. This will involve many variables to show what is the start and end of the backtick sequence as well as if statements and for loops to iterate
through the code to find the backticks.
  - This applies for the reviewed repo because it must also include variables, if statements, and for loops to track the backticks in the markdown files.
- I think the solution would take \>10 lines to change because in my code, I have already been tracking paranthesis and have labelled if there was a 
nested parenthesis in the link. As a result, if a just make that part of my code check for nested links in addition to the nested parenthesis and 
nested parenthesis within nested paranthesis.
  - The reference passed snippet2, so this only applies only to my MarkdownParse.
- I think that this will be an easy fix because all we have to do is to make all lines in the md file to 1 line. We would take out the for loop to compare by each line and only compare the one super long line. It should take less than 10 lines to implement.
