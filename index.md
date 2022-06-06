# Lab Report 5

## Part 1: How you found the tests with different results?

I used vimdiff on the results of running a bash for loop.


## Part 2: Link to two of the test-files with different-results
1. [File 194](https://github.com/nidhidhamnani/markdown-parser/edit/main/test-files/194.md)
2. [File 201](https://github.com/nidhidhamnani/markdown-parser/edit/main/test-files/201.md)


## Part 3: For Each Test

### a. Describe which implementation is correct, or neither if both give the wrong output
1. For file 194, the provided output is correct;
2. For file 201, our implementation is correct.

### b. Indicate both actual outputs (provide screenshots) and also what the expected output is (list the links that are expected in the output).

- Actual output for our implementation (File 194)

![alt text](194wrongus.png)

- Actual output for the provided implementation (File 194)

![alt text](194wrongpr.png)

- Expected output for file 194 should be `url`
- Actual output for our implementation (File 201)

![alt text](201correctus.png)

- Actual output for the provided implementation (File 201)

![alt text](201wrongpr.png)

- Expected output for file 201 should be empty.

### c. For the implementation that’s not correct, describe the bug (the problem in the code) in about 2-3 sentences. 

- (File 194) When there are some extra text between the brackets and parenthesis, the program should automatically ignore those text and instead treat it as an actual link. This means we can not simply assume that one index after `[` would guarantee the start of a link content at line 29 (See Screenshot Below). 
- (File 201) If there are `<` in between the text mentioned above, then the entire line should not be considered a link anymore. This means that at line 64-45 when a `<` or `>`is encountered there should be an if statement to reconsider the next possible sequence of link. (See Screenshot Below). 


### d. Provide a screenshot of code and highlight where the change needs to be made.
- For File 194
![alt text](problem1.png)

- For File 201
![alt text](problem2.png)

