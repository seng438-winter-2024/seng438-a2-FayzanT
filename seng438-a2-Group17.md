**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#2 – Requirements-Based Test Generation**

| Group \#:      |   17  |
| -------------- | --- |
| Rohan Kapila | 30145862 |
| Fayzan Toor               | 30141139    |
| Shayyan Asim               |  30149567   |
| Qazi Ali              | 30142452    |

# 1 Introduction:
In this assignment we are tasked to test 2 different classes. DataUtilities.java and Range.java using Junit. The objective of this assignment is to educate us on the fundamentals of automated unit testing, emphasizing testing procedures aligned with the specific requirements of each unit. By creating tests and mocking behaviors of dependent classes, we get to fully explore the intricacies of black box testing.

# 2 Detailed description of unit test strategy:

## Detailed Description of Unit Test Strategy for Range.java:

### 1. Boundaries Directly: 
This partition focuses on whether the lower and upper bounds are correct and the range class sets the boundaries accurately according to user inputs.

### 2. Zero Length Range: 
This partition examines the case where the range has zero length. By testing this condition, it verifies that the length calculation is appropriately done when the lower and upper bound values are the same. 

### 3. Contains at Boundaries: 
This partition focuses on testing the  contains method, specifically testing its behavior with boundary values. It verifies whether a range contains or not contains a specific number.

### 4. Shift With Zero Crossing:
This partition does the testing of the shift method, which focuses on cases where the range crosses zero as a result of the shift operation. By testing this condition, it ensures that the class handles range shifting accurately, adjusting boundaries correctly without any outliers when crossing zero.

### 5. Shift Without Zero Crossing:
This partition is the opposite of the  previous partition, this partition examines the shift method's behavior when the range is shifted without crossing zero. It verifies that the range boundaries are appropriately adjusted without crossing the zero boundary, maintaining the correctness of the range.

### 6. Get Length for Different Ranges:
This partition aims to verify that even if its a positive, negative value the get length method calculates the correct range.

### 7: Nullshift exception: 
When testing the Shift method we put one of the parameters as null to check if it throws an exception and gives an error.

By considering these input partitions, the unit test strategy ensures a good  coverage of the Range class working. Each test case is designed to target specific aspects of the class's behavior, promoting effective verification and debugging.


## Detailed Description of Unit Test Strategy for DataUtilites.java:


### 1. Direct Row Access:
This partition confirms the method’s functionality to calculate the values in a specified row using the Values2D dataset. It checks the accuracy of the results by taking into account the indexing and summing functions of Values2D.


### 2. Primitive to Object Conversion:
This partition uses the method’s ability to convert an array of double values into an array of Number objects. Through the test of this method, the functionality is verified when handling the conversion of primitive values into Objects.


### 3. Cumulative Calculation Accuracy:
This partition validates the cumulative percentage calculations within the KeyedValues dataset. It authenticates the values calculated through the method against what is expected to return from the method description.


### 4. 2D Array Conversion Integrity: 
This section verifies the method’s functionality in converting a 2D array of doubles into a 2D array of Number objects. It ensures the conversion carries over properly with data integrity.

### 5. Invalid Parameter Exception:
This partition ensures an InvalidParameterException is thrown when the incorrect parameters are input into the method. The method’s specify they are able to throw this exception, so null values are used to test it.

By adopting this structured approach to testing, similar to the one used for `Range.java`, we ensure in-depth coverage and reliability of the methods within the DataUtilities class. Each test case is designed to target specific functionalities, allowing for effective validation and ensuring method integrity across multiple inputs.



# 3 Test cases developed:


## Test Cases Developed for Range.java:
### Test Boundaries Directly                                                                                          
 Methods: getUpperBound() and getLowerBound()                                                                                    
 Description: Verifies and authenticates then the upper and lower bound are correct.

### Test Zero Length Range:                                                                                                                       
 Method: getLength()                                                                                                   
 Description: Ensures that the length of the range is correctly computed when the range has zero length.

### Test Contains at Boundaries:                                                                                                                     
 Method: Contains()                                                                                                                                      
 Description: Tests the contains method to check whether the input is in the range or not.


### Test Shift With Zero Crossing:                                                                                                              
 Method: Shift()                                                                                                                                              
 Description: Valdates the shift method's functionality  when the range crosses zero.

### Test Shift Without Zero Crossing:   
 Method:Shift()                                                                                                                                                             
 Description: Verifies if  the shift method maintains the range boundaries without crossing zero.

### Test Get Length for Different Ranges:                                                                                                     
 Method: getLength()                                                                                                                                                  
 Description: Ensures that the getLength method calculates the  length correctly for negative, zero, and positive ranges.

 ### NULL Exception case for the shift method:
 <br> Method: Shift())
 <br> Description: Validates if the method will throw an exception if null value is given an input.


 These test cases cover the input partitions identified in the test strategy, ensuring thorough testing of the Range class functionalities.



## Test Cases Developed for DataUtilities.java:

### Test Calculate Row Total:
 Methods: calculateRowTotal()
 <br>Description: Checks that calculateRowTotal method computes the correct sum for a specified row using a mocked Values2D object. 

### Test Create Number Array:
 Methods: createNumberArray()
 <br>Description: Gurantees that the createNumberArray method transforms an array of doubles into Number objects accurately.
 
### Test Get Cumulative Percentages:
 Methods: getCumulativePercentages()
 <br>Description: Tests the getCumulativePercentages method to ensure it correctly calculates the cumulative percentages of values from a KeyedValues dataset.

### Test Create Number Array2D with Valid Input:
 Methods: createNumberArray2D()
 <br>Description: Evalutes that the createNumberArray2D method can precisely convert a 2D array of doubles into a 2D array of Number objects.

 ### Test InvalidParameterException is throwin with Invalid Input:
 Methods: createNumberArray2D(), getCumulativePercentages(), createNumberArray (), calculateRowTotal (), calculateColumnTotal ()
 <br>Description: Makes sure that these methods throw the exception within their documentation.


These test cases are designed to cover the main functionalities within the DataUtilities class, ensuring in-depth testing across a variety of input conditions.




# 4 How the team work/effort was divided and managed:

Team Work was divided into two Groups. And we adopted the pair programming approach where within each group one was writing code and the other was the observer but we switched roles and cross checked each other's work. Rohan Kapila and Shayyan Asim tested the Range.java class whereas Qazi Ali and Fayzan Toor tested the DataUtilities.java class but both groups then tested each other’s assigned class and cross checked.


# 5 Difficulties encountered, challenges overcome, and lessons learned:

During our test making process for the DataUtilities class, we encountered some difficulty when implementing methods that needed Mocking to replicate their dependent classes. This was encountered when we specifically went to test the CumulativePercentages method that required KeyedValues as input to function. We tried to use the example Mock given in the github repo, but our test would not even run. By using the JUnit logs, we discovered the issue was based on the methods we were mocking being called once, when they were expected to be used multiple times. We had to use online resources and ChatGPT to figure out the implementation of calling methods multiple times. From this experience, we learned how to call on methods repeatedly while mocking.

# 6 Comments/feedback on the lab itself:

This assignment was a fun way to get hands-on experience with Junit testing and understanding the importance of testing in software engineering. It taught us how we should design test cases by coding and then running them. The lab was designed nicely and it was easy to run through every step however for windows user in our group we were not able to render the index.html file, in future we hope that all files given to us by lab instructions are capable on running on any type of OS.

# 7 AI Usage:

We used ChatGPT for error log explanations when our tests were not passing. We gave the error message as the prompt and retrieved information that let us search up solutions to fix the error.

Prompt:
"unexpected invocation: keyedValues.getKey(<1>)
expectations:
  allowed, already invoked 4 times: keyedValues.getItemCount(); returns <2>
  allowed, already invoked 1 time: keyedValues.getValue(<0>); returns <1>
  allowed, already invoked 2 times: keyedValues.getValue(<1>); returns <2>
  allowed, already invoked 1 time: keyedValues.getKey(<0>); returns <0>
what happened before this:
  keyedValues.getItemCount()
  keyedValues.getValue(<1>)
  keyedValues.getItemCount()
  keyedValues.getItemCount()
  keyedValues.getValue(<0>)
  keyedValues.getKey(<0>)
  keyedValues.getItemCount()
  keyedValues.getValue(<1>)

	at org.jmock.internal.InvocationDispatcher.dispatch(InvocationDispatcher.java:56)
	at org.jmock.Mockery.dispatch(Mockery.java:218)
	at org.jmock.Mockery.access$000(Mockery.java:43)
	at org.jmock.Mockery$MockObject.invoke(Mockery.java:258)
	at org.jmock.internal.InvocationDiverter.invoke(InvocationDiverter.java:27)
	at org.jmock.internal.FakeObjectMethods.invoke(FakeObjectMethods.java:38)
	at org.jmock.lib.JavaReflectionImposteriser$1.invoke(JavaReflectionImposteriser.java:33)
	at jdk.proxy2/jdk.proxy2.$Proxy6.getKey(Unknown Source)
	at org.jfree.data.DataUtilities.getCumulativePercentages(DataUtilities.java:185)
	at org.jfree.data.test.DataUtilitiesTest.testGetCumulativePercentages(DataUtilitiesTest.java:149)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:45)
	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:15)
	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:42)
	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:20)
	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:263)
	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:68)
	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:47)
	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:231)
	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:60)
	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:229)
	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:50)
	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:222)
	at org.junit.runners.ParentRunner.run(ParentRunner.java:300)
	at org.eclipse.jdt.internal.junit4.runner.JUnit4TestReference.run(JUnit4TestReference.java:93)
	at org.eclipse.jdt.internal.junit.runner.TestExecution.run(TestExecution.java:40)
	at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.runTests(RemoteTestRunner.java:529)
	at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.runTests(RemoteTestRunner.java:756)
	at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.run(RemoteTestRunner.java:452)
	at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.main(RemoteTestRunner.java:210)"
"
Response:
-"The error message you're encountering is related to a unit test that uses JMock for mocking dependencies. The message provides detailed information about the expectations set for mocked methods and their actual invocations, which didn't match the expectations. Let's break down the message to understand the issue and how to fix it.

Understanding the Error Message
Unexpected Invocation: The test did not expect keyedValues.getItemCount() to be called more than once, but it was.

Expectations:

keyedValues.getItemCount(); was expected to be called once and it has already been called once. This is okay, but the error message suggests there was an attempt to call it again, which was not expected.
keyedValues.getValue(<0>); was expected to be called once but never was. This indicates a missing method call that the test was expecting.
keyedValues.getValue(<1>); was expected to be called once and has been called once, which matches the expectation correctly.
What happened before this: This part of the message tells you the sequence of method calls that occurred before the error was thrown:

keyedValues.getItemCount() was called.
keyedValues.getValue(<1>) was called.
Error Trace: The stack trace provides the path through the code that led to the error, starting from the failing test method testGetCumulativePercentages in DataUtilitiesTest.

How to Fix the Issue
Given the error message, there are a few potential issues to address in your test:

Multiple Invocations of getItemCount: Your test or the code under test calls getItemCount() more than once, but your mocking setup only expected it to happen once. If the method is supposed to be called multiple times, adjust your expectation to reflect that. In JMock, you can use .times(int count) to specify the number of invocations expected.

Missing Invocation of getValue(<0>): Your test setup expected getValue(<0>) to be called, but it never was. Ensure that your test or the code under test correctly calls this method as expected. If this call is conditional or not required, you might need to adjust your expectation to match the actual logic.

Correct Expectation for getValue(<1>): Since the call to getValue(<1>) matches the expectation, no action is needed for this particular expectation.

To adjust the expectation for multiple invocations, you could modify your setup like this (assuming a hypothetical syntax based on common usage in mocking frameworks):

java
Copy code
// Expecting getItemCount to be called any number of times, returning 2 each time
expect(keyedValues.getItemCount()).andReturn(2).anyTimes();

// Expecting getValue to be called with specific arguments
expect(keyedValues.getValue(0)).andReturn(1).once(); // If it's supposed to be called
expect(keyedValues.getValue(1)).andReturn(2).once(); // Already correct
Review the logic in your test and the method under test to ensure it aligns with the expected behavior. If the method getItemCount is indeed called more than once in the flow, your expectation setup should reflect that. Similarly, ensure that getValue(<0>) is called as expected in the test scenario."




