# Lab Report 2

## Part 1

Code for StringServer:


<img width="1512" alt="Screen Shot 2023-04-24 at 2 20 52 PM" src="https://user-images.githubusercontent.com/130090548/234119913-6c018fd0-9a14-42fc-96ad-570ccc9fa910.png">

Screenshot of using /add-message?s=Hello:

<img width="615" alt="Screen Shot 2023-04-24 at 2 19 47 PM" src="https://user-images.githubusercontent.com/130090548/234120301-fca2a1e2-42c0-44e3-9060-80a6ac3205b3.png">


<img width="611" alt="Screen Shot 2023-04-24 at 2 20 01 PM" src="https://user-images.githubusercontent.com/130090548/234120290-30cb3728-8065-430e-86e4-79d07da6fdc5.png">







Screenshot of using /add-message?s=How are you:

<img width="608" alt="Screen Shot 2023-04-24 at 2 20 20 PM" src="https://user-images.githubusercontent.com/130090548/234120238-2112497d-135f-4e08-846f-93aac516fed9.png">



<img width="608" alt="Screen Shot 2023-04-24 at 2 20 33 PM" src="https://user-images.githubusercontent.com/130090548/234120225-28153043-6f74-4f6b-9bc5-ae588b1f5188.png">



For each of the two screenshots, describe:

Which methods in your code are called?


Screenshot using hello:
It calls the method handleRequest()

Screenshot using How are you:

It calles the mthod handleRequest()

What are the relevant arguments to those methods, and the values of any relevant fields of the class?


Screenshot using hello:
URI object representing the incoming request. In this case, the URI path is /add-message and the query string is s=Hello

Screenshot using How are you:
UrI object reperesenting the incoming request. In this case, the URI path is /add-message and the query string is s= How are you.

How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
By values, we mean specific Strings, ints, URIs, and so on. "abc" is a value, 456 is a value, new URI("http://...") is a value, and so on.)


Screenshot using hello:
Message is an emptry string before the request and its value changes to hello after the request

Screenshot using How are you:
message is hello before the request and its value changes to How are you after the request.


# Part 2

## ArrayTests

This is a JUnit test class for the `ArrayExamples` class, which contains a method called `reverseInPlace` that attempts to reverse the order of elements in an integer array in place.

### testReverseInPlace

The first test method test the `reverseInPlace` method with failure-inducing input for the buggy program

The second test method test the `reveseInPlace` method that doesn't induce a failure.

####

```java
int[] arr = {1, 2, 3, 4, 5};
ArrayExamples.reverseInPlace(arr);
assertArrayEquals(new int[]{5, 4, 3, 2, 1}, arr);

int[] input1 = { 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input1);

```

## Sympton as the output of running the test(screenshot)
<img width="1512" alt="Screen Shot 2023-04-24 at 4 42 08 PM" src="https://user-images.githubusercontent.com/130090548/234138584-4937557b-602d-4fc0-b2b4-9eadf99ae154.png">

<img width="1512" alt="Screen Shot 2023-04-24 at 4 42 13 PM" src="https://user-images.githubusercontent.com/130090548/234138588-20b24f20-43d5-4d03-8167-2a931075ccce.png">


As you can see with the screenshot the it doesnt reverse the array the input is 1,2,3,4,5 and the correct output should be 5, 4,3, 2,1 , but the original code returns 2 not 4.
Bug is that it doesn't actually reverse the array, but replaces each of the elements. To fix it you can use a two pointer to place the two points the start and end and swap the start and end while incrementing both the start and end with 1.

### The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
#### Before:

```java

 static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }

```

#### After:

```java
static void reverseInPlace(int[] arr) {
  int left = 0;
  int right = arr.length - 1;
  while (left &lt; right) {
    int temp = arr[left];
    arr[left] = arr[right];
    arr[right] = temp;
    left += 1;
    right -= 1;
  }
}
```
Fixed code uses two indices left and right to initialize the first and last element of the array. It then sawps the values of left and right while incrementing left and decrementing the right until they meet at the middle.

# Part 3

Things that I learned in week2 for lab was creating a webserver and how to create supports for the path and behavior. Another thing that I learned in week3 was how to look for bugs and create test cases to find the bugs and check the behavior of it.
