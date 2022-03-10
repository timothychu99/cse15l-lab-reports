## How I Found Tests with Diff Results
- I used the command ``diff <test_file1> <test_file2> ``.
- when running it, it will show in terminal an output like:

![terminal_diff_output](https://user-images.githubusercontent.com/60487968/157586101-341b6e39-8e91-47ee-bd71-8747520d50f6.png)
  - ``<line_num1>c<line_num2>`` represents line_num1 of test_file1 is compared to line_num2 of test_file2.
  - the ``< [<link>]`` means that that is what the test_file1's getLink resulted to.
  - the ``> [<link>]`` means that that is what the test_file2's getLink resulted to.
## Test1 for line 212 of both results.txt and another_result.txt
- line 211 and 212 of results.txt

![line 212 of results.txt](https://user-images.githubusercontent.com/60487968/157586771-ec0de238-ea1d-453e-842f-9c5128636436.png)

- line 211 and 212 of another-result.txt

![line 212 of another-result.txt](https://user-images.githubusercontent.com/60487968/157587283-0060beb4-d097-4ca0-a7c8-68bf27e4d0ec.png)

- test-files/194.md

![image](https://user-images.githubusercontent.com/60487968/157586968-b4629285-6fa5-417e-9d18-cf95476974b4.png)
  - There should be no link in this markdown file, because there is no paranthesis right after the brackets in the text file.
  - As a result, the another-result.txt, which was created from my own implementation of MarkdownParse.java and getLinks method is right in displating no links. The results.txt, which was the instructor's implementation of MarkdownParse.java and getLinks method is incorrect, because it displays ``url`` as a link.

  - The problem with the instructor's getLinks result is that it located a link wrong. The link should be in parenthesis that is directly following a ``]`` bracket. In this case, the parenthesis that the 'link' was in did not follow the property of following a ``]`` bracket.
   
 ##Test2 for line 906 of both results.txt and another_result.txt
- line 905 and 906 of results.txt
- ![line 906 of results.txt](https://user-images.githubusercontent.com/60487968/157589850-9e587b8b-6b90-4c7e-ad68-ec545f640c16.png)

![line 906 of results.txt](https://user-images.githubusercontent.com/60487968/157589580-f73cfb80-a665-4125-8fd3-017aa0231ba6.png)

- line 906 and 907 of another-result.txt
- ![line 906 of another-result.txt](https://user-images.githubusercontent.com/60487968/157589794-2ae009f8-1fea-426a-830b-aa6d4fe0bb58.png)

![line 906 of another-result.txt](https://user-images.githubusercontent.com/60487968/157589650-a153b767-06ac-4e62-b4bb-bd98529da732.png)

- test-files/506.md

![image](https://user-images.githubusercontent.com/60487968/157589974-5d5bd14d-bce8-4bbe-bded-9b30fe0cb01e.png)
 - There should be one link ``/url "title"`` in this markdown file, because there is the .
  - As a result, the another-result.txt, which was created from my own implementation of MarkdownParse.java and getLinks method is right in displating no links. The results.txt, which was the instructor's implementation of MarkdownParse.java and getLinks method is incorrect, because it displays ``url`` as a link.
[link](/url "title")
  - The problem with the instructor's getLinks result is that it located a link wrong. The link should be in parenthesis that is directly following a ``]`` bracket. In this case, the parenthesis that the 'link' was in did not follow the property of following a ``]`` bracket.

Explain:

How you found the tests with different results (Did you use diff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)
For each test:
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.
For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.
