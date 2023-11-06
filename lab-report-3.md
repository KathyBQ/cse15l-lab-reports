Part 1: choose on of the bugs from lab4
  - A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
    ```@Test
       public void testReverseInPlace3() {
          int[] input1 = { 1, 2, 3 };
          assertArrayEquals(new int []{ 3, 2, 1}, input1);
       }```
  - This is a JUnit test to test the reverseInPlace3() method, using the input1 = { 1, 2, 3}, while the expected output is {3, 2, 1}. But the shown output is {3, 2, 3}.  
  - An input that dosen't induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
  - 
