## Part 1 

Here is the implementation/code for the webserver that keeps track of a single string that gets added to by incoming requests:

<img src="URL Code.png" width="600" height="500">

**Screenshot #1:**

<img src="Hello.png" width="500" height="300">

* Above the HandleRequest method is called, using the url parameter. 
* The request matches the condition of the method in which the url contains the string "/add-message". 
* To read the string content of the request, I used the getQuery method and take the string reqeusted by creating a String array. To get the actual String requested I also split it by the "=" so that only the String would be read and stored in the array. 
* After satisfying the conditions that the String requested is followed by "s" and split by "=", the String is then updated to the "runningString" String field. This is a field of an empty String that I declared outside the method as a placeholder for the String requests. The update also concatenates to the next line for the next String to be listed. 


**Screenshot #2**

<img src="HowAreYou.png" width="500" height="300">

* In this 2nd screenshot, the same method is called, using the same url parameter 
* Here we see the previous String listed on the page because we have saved the first request in the runningString that concatenates to the next line. 
* So when the second request is called, instead overriding/replacing the first String, the method updates the page with a list of the previous String and the current running String. 

**The values of the requests will only be read as String values and will be listed as is in the web page becuase the return type of the method is a String. If we want the return values to be another primitive return type, we would probably need to cast it to the desired return type (i.e. (Integer))**



## Part 2
For this part, I chose the reversed method as the method that contains a bug in the code. 

**A failure-inducing input for the buggy program as a JUnit test:**

```
public void testReversed() {
    int[] input2 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input2));
  } 
```

The JUnit test input above induces a failed output that indicates that there is a bug within the progarm such as wrong implementation of the method. This test has the appropriate expected value, which is a new array containing the reverse elements of the original array. The actual value also calls the method appropriately. Therefore this test input should run the code correctly and in this case will induce a failed/incorrect output. 

**An input that doesn’t induce a failure as a JUnit test:**

```
public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

The JUnit test input above doesn't induce a failure because does not call the method appropriately, or does not represent what the method should implement. This input calls an empty array, which will of course produce an empty array. This will consequently pass the JUnit test as the expected value and the actual value will match, making the program think that the method is implemented correctly. However, the method is supposed to take an array that contains elements and produe a new array in which the elements are placed in the reversed order, which in this case the input does not call such array with elements. Therefore this input is an input that doesn't induce a failure. 

**The Symptom:**

<img src="Symptom.png" width="500" height="300">

When we run the apprpiate JUnit test, the test does not pass because the expected value does not match the value that was called from the method. The above screenshot shows that the first test method passes but the second one does not because the expected value of the first element should be 3, but the actual value that we get is 0. This is an example of a symtom, showing the wrong behavior or error that we see when running the test. 

**Code before it is fixed (buggy code):**

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

**Revised code that fixes the wrong implementation:** 

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      newArray[arr.length - 1 - i] = arr[i];
    }
    return newArray;
  }
```

This fix addresses the wrong implementation in the for loop and return value after the iteration from the for loop. The for loop iterates through the original array correctly, but the body still updates the original array, instead of the new array. To fix this, I just switched the newArray and the originial array from one side to the other. Secondly, since the method should return a new array with the elements in reveresed order than the original array, the original method does not return the new updated array, but instead return the original array. When I changed the return value to the new array, the test passes with the correct values.


## Part 3

**Some things I learned from Lab 2/3:**

From Week 2 Lab I learned that you can host your own web server from VS Code with certain built in functions in the Java progam. I was not aware of this before and I think it's fun that you can build/implement your own server and even share it with other folks. I also learned a lot more about GitHub functions such as forking and cloning, which I was also not aware of before lab. 
