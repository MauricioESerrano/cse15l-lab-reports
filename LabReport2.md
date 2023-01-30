# Lab Report 2

**Part 1**
Code body
<img width="764" alt="image" src="https://user-images.githubusercontent.com/122576152/215393511-c6c89459-3726-4f05-97fc-4ebffddfb731.png">

The body checks everything after the "/". It goes through everything checking for specific instances. First it looks for add-message, then for "?"
querry, and the "s=" sign after that. After than, anything after the "=" will be considered in parameter[1]. In order for it to work, the user input 
must be a string. 

The only values that changes was parseInt and int because we no longer are dealing with count+, but rather strings. So we needed to change the code so 
that it fit that. 

Using /add-message technique
<img width="451" alt="image" src="https://user-images.githubusercontent.com/122576152/215393544-539092c3-ca93-4d11-8c9f-cfebdd58fa18.png">

**Part 2**

Code Problem 1
```
for(int i = 0; i < arr.length; i++) {

      arr[i] = arr[i]; 
    }
```
JUnit related to Code 1 that failed 
```
ArrayExamples.reverseInPlace(Input2);
assertArrayEquals(new Int[]  { 5,4,3,2,1}, input2);
```
Code fix 1
```
public void testReverseInPlace() {
    int[] input1 = { 3 };
    int[] input2 = {1,2,3,4,5};
    int[] input3 = {1,2,-1,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);

    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[] {5,4,3,2,1}, input2);

    ArrayExamples.reverseInPlace(input3);
    assertArrayEquals(new int[] {5,4,3,-1,2,1}, input3);
	}
  ```
  Code fix related Issue 1
  
  ```
  static void reverseInPlace(int[] arr) {
    int[] newOg = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {

      arr[i] = arr[i]; 
    }

    for(int i = 0; i < arr.length; i++) {

      arr[i] = newOg[arr.length - i -1]; 

    }
  } 
```
JUnit symptom screenshot

<img width="347" alt="image" src="https://user-images.githubusercontent.com/122576152/215402183-18f70834-b1e9-4c43-a919-f00523e9a524.png">

A successful JUnit

```
@Test
  public void testAverage() {

    double[] input = {0,1,2,3};

    double result = ArrayExamples.averageWithoutLowest(input);
    assertEquals(2,result,0);

  }
```

The fix was to create a new array and create a for loop assigning old "arr" to "newOg" array. This allowed for me to reverse, elements in 
"arr" into "newOg" returning the desired output. 



**Part 3**

One thing I learned in week 3 is identiying values I never knew before. For instance, when running a JUnit test, the "." refer to tests ran 
and the "E" referring to tests failed. Another thing I learned that I am actually glad that I learned involves the coding behind Part 1 of this lab report. 
Specfically referring to the query, how to HandleRequest, url.getPath and the main method referring to launching a server with ports. 
