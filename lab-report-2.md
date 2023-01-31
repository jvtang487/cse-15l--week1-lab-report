# Lab Report 2

# Part 1:
## String Server Code: 
![Image](https://github.com/jvtang487/cse-15l-lab-reports/blob/main/lab%20report%202/StringServerCode.png)

## Use of /add-message:
![Image](https://github.com/jvtang487/cse-15l-lab-reports/blob/main/lab%20report%202/addmessage1.png)

The method that is called the handleRequest method.
The arguments that are relevant are the if statements as they check the path and query to check if they need to add certain message or just display a message.
The values that are relevant is the string `servString` as this holds the value of the single string. The url is also relevant as this is what is read by the code to detemerine what gets added to the string. The parameter of "=" and "s" is also relevant as this splits the query from the path making it easier to read the String needed to be added.

The query is changed in the url value from blank to the message "hello" this in return changes the value of the single string to also "hello". 

![Image](https://github.com/jvtang487/cse-15l-lab-reports/blob/main/lab%20report%202/addmessage2.png)

For this usage the same method, arguments, and values are called and are relevant. The only change is that query is changed with a new message. The `servString` holds both this new string and the old string. But they are seperated by lines because of the `\n` that is added to string in the previous call.

# Part 2:
## Failure Inducing Code:
`   @Test
  public void testReversed2(){
    int[] input1 = {3, 4, 5, 6 };
    assertArrayEquals(new int[]{6, 5, 4, 3}, ArrayExamples.reversed(input1));
  }
  `
## Input No Failure:
 ` @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
  `
 ## The Symmptom:
 
