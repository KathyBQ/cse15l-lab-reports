Part 1: choose on of the bugs from lab4
  - A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
    ```
       @Test
       public void testReverseInPlace3() {
          int[] input1 = { 1, 2, 3 };
          assertArrayEquals(new int []{ 3, 2, 1}, input1);
       }```
    
This is a JUnit test to test the reverseInPlace() method, using the input1 = { 1, 2, 3}, while the expected output is {3, 2, 1}. But the shown output is {3, 2, 3}. 

  - An input that dosen't induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
    ```
      @Test
      public void testReverseInPlace2() {
        int[] input1 = {1};
        assertArrayEquals(new int[]{1}, input1);
      }```

This outputs {1}, expected and doesn't make a failure.

  - The sympton, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
    <img width="908" alt="Screen Shot 2023-11-05 at 11 40 35 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/57a22e2c-fc5f-4426-97a6-bef4fc08374e">

This is the screenshot of the above 2 tests using JUnit tests.

  - The bug, as the before-and-after code change requried to fix it (as two code blocks in Markdown)
    ```
      static void reverseInplace(int[] arr) {
        for(int i = 0; i < arr.length; i+=1) {
          arr[i] = arr[arr.length - i - 1];
        }
      }
    ```
The above is the before code with bugs.

The below is the after code without bugs.
    ```
      static void reverseInPlace(int[] arr) {
        for (int i = 0; i < arr.length / 2; i+=1) {
          int temp = arr[i];
          arr[i] = arr[arr.length - i - 1];
          arr[arr.length - i - 1] = temp;
        }
      }
    ```
      
The bug is: The previous one didn't create a new variable to store the new elements. It grab and store elements in the same input variable, which makes it grab the already replaced element in the variable. 

  - Briefly describe why the fix addresses the issue.
    The new code tracks half of the input array elements, and create a variable to store the old element, then grab the new element from the end of the input and store it at the beginning of the input, then give the new vairbale value to the end of the input.It won't make the double grab.

Part 2: researching commands
- reseaches 1 command (grep/find/less) with 4 command line options/alternate ways to use the command: (the command is in codeblocks)
  ```
  1. find <files-directory> -name "<file-name OR directory-name>"
  //see the examples below//
  ```

  example 1: ```find technical/911report -name "*.txt"```
  This example find all .txt files from technical/911report directory.
  <img width="985" alt="Screen Shot 2023-11-19 at 8 17 55 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/a8dc5890-2e79-48b5-8010-fa0c3c18b215">

  example 2: ```find technical -name "911*"```
  this example finds the directory/files starting with 911 in technical directory. In this case, only has the technical/911report satisfies. 
<img width="860" alt="Screen Shot 2023-11-19 at 8 22 57 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/45d0dc4f-66ac-4fc5-8423-86a1b5aa9387">

  ```
  2. find <directory-path> -empty
  //see the examples below//
  ```
  
  example 1: ```find ./technical -empty```
  this example finds all the empty files and directories in technical directory.
  <img width="892" alt="Screen Shot 2023-11-19 at 8 32 29 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/5cea5690-2d2b-4edd-948d-928f9a63b566">

  example 2: ```find technical/911report -empty```
  this example finds all empty files and directories in 911report directory, but these doesn't exist any empty files/direcotries. So it shows nothing.
  <img width="642" alt="Screen Shot 2023-11-19 at 8 34 51 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/8c2e6148-52d8-42d7-9963-e6a2df16402e">

  example 3: ```find technical/empty-folder -empty```
  this example finds all empty files/directories in empty-folder. the empty-folder has nothing. So it only shows itself.
  <img width="642" alt="Screen Shot 2023-11-19 at 8 37 15 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/292bd28a-8118-4e8e-a2d7-7e41d52fa69f">

  ```
  3. find <directory> -type d
  //see the examples below//
  ```

  example 1: ```find . -type d```
  this example finds all repositories and sub-repositories in the current <docsearch> repository. Here, we contain git infos and our own docsearch stuff.
  <img width="946" alt="Screen Shot 2023-11-19 at 8 38 49 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/f90402a2-5120-421c-abe0-6d57818aba40">

  example 2: ```find technical/911report -type d```
  this example finds 911report directory because there is only one repository in this and that's itself.
  <img width="671" alt="Screen Shot 2023-11-19 at 8 44 26 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/8e91a32a-d54b-44d6-a2d2-eed12882b79f">

  example 3: ```find technical/911report/chapter-1.txt -type d```
  this example finds nothing because the chapter-1.txt is not a directory, is a file.
  <img width="773" alt="Screen Shot 2023-11-19 at 8 47 00 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/bd6a7bd9-b4b6-4778-909e-b973c94b9c24">

  ```
  4. find <file-name OR directory-name> -delete
  ```

  example 1: ```find empty-file.txt -delete```
  this example finds the empty-file.txt in the current technical direcoty and then deletes it.
  <img width="847" alt="Screen Shot 2023-11-19 at 8 54 09 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/e20de81a-01f1-4225-bc7e-f7ed35164103">

  example 2: ```find empty-folder -delete```
  this example finds the empty-folder directory in the current technical directory and then deletes this empty-folder directory.
  <img width="891" alt="Screen Shot 2023-11-19 at 8 55 54 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/de96e3d6-2dd3-476b-a2e1-ba7559e7c8c1">

- provides 2 examples for each command line option/alternate usage (total of 8 examples): (each example has a corresponding output (the output of the command is a screenshot/has been formatted using codeblocks)) cites sources appropriately
  link: https://www.geeksforgeeks.org/find-command-in-linux-with-examples/
  link: https://man7.org/linux/man-pages/man1/find.1.html
