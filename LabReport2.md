## Part 2
For this part, I chose the reversed method as the method that contains a bug in the code. 

A failure-inducing input for the buggy program as a JUnit test:

```
public void testReversed() {
    int[] input2 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input2));
  }
 
```

An input that doesn’t induce a failure, as a JUnit test:

```
public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
  
```
