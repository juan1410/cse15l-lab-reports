# Lab Report 2

## Part 1
Code for web server, StringServer:
![Image](StringServer.png)


Using /add-message:

![Image](add-message1.png)
- In my code for String Server, as I added the first message in the web server, the url.getPath() method and url.getQuery() method were called.
- The url.getPath() method was first called in order to check the "/add-message" request. After it did, it called the url.getQuery() method with the argument "s=Good Morning" in order to split at "=". The split was necessary in order to check the message after the "=" in order to respond with that string given.
- The first value of "str" was an empty string at first since we have not yet added anything. After the first "/add-message" was called, "str" now concataned with the message given after the "=". A new line message, "\n", was also given at the end therefore creating a new line after the given string was concataned with the other. Therefore the new "str" value was "Good Morning" with a new line after it.


![Image](add-message2.png)
- In the code, the url.getPath() and url.getQuery() methods were both called.
- The url.getPath() method first checked "/add-message" request. After it contained this request, it called the url.getQuery() method with the argument "s=Hello" in order to split at "=". After spliting, it checked the message after the "=" in order to respond with that string given and any other string that was already requested before this one. 
- The value of "str" before this method was called was "Good Morning" with a new line after it. However, after calling this method, "Hello" was concated with str but since there was a new line created with the previous request, "Hello" was given to a new line under "Good Morning". However, "Hello" was also concated with a "\n" at the end, therefore creating a new line after it. Therefore, the new "str" value was "Good Morning" and then "Hello" in a new line and a new line after "Hello".




## Part 2
Failure-Inducing input:
```
public void testReverseInPlace2(){
  int[] input = {10, 15, 20};
  ArrayExamples.reverseInPlace(input);
  assertArrayEquals(new int[] {20, 15, 10}, input);
}
```

Input without a failure:
```
public void testReverseInPlace(){
  int[] input1 = {5};
  ArrayExamples.reverseInPlace(input1);
  int[] input2 = {5};
  assertArrayEquals(input2, input);
}
```

Symptom:
![Image](symptom.png)


Before code change:
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```
After code change:
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length/2; i += 1) {
    int num = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = num;
  }
}
```
- The fix being presented in the after code change helps fix the issue. First we changed the loop for it to only run half of the array's length. Then we assigned 'num' to contain the reference of the element at index 'i'. After we assign the element at index 'i' to be the element at index[arr.length - 'i' - 1], which is what was done in the before code as well. However, this time we assign the element at index[arr.length - 'i' - 1] to be the element that was stored at num, which was the reference, to the element at index 'i'. Therefore, the elements at index 'i' and index[arr.length - 'i' - 1] are being switched. And since we assign the second half and first half of the array in one loop, we do not need to loop through the full length of the array but instead just half, which is why we changed the loop to run arr.length/2 times.




## Part 3

