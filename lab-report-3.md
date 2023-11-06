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
      static void reverseInplace(int[] arr) {
        for(int i = 0; i < arr.length / 2; i+=1) {
          int temp = arr[i];
          arr[i] = arr[arr.length - i - 1];
          arr[arr.length - i - 1] = temp;
        }
      }```
      
The bug is: The previous one didn't create a new variable to store the new elements. It grab and store elements in the same input variable, which makes it grab the already replaced element in the variable. 

  - Briefly describe why the fix addresses the issue.
    - 
