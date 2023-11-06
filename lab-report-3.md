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
  - The bug, as the before-and-after code change requried to fix it (as two code blocks in Markdown)
  - Briefly describe why the fix addresses the issue.
    - 
