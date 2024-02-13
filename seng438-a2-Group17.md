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

### 1.Boundaries Directly: 
This partition focuses on whether the lower and upper bounds are correct and the range class sets the boundaries accurately according to user inputs.

### 2.Zero Length Range: 
This partition examines the case where the range has zero length. By testing this condition, it verifies that the length calculation is appropriately done when the lower and upper bound values are the same. 

### 3.Contains at Boundaries: 
This partition focuses on testing the  contains method, specifically testing its behavior with boundary values. It verifies whether a range contains or not contains a specific number.

### 4.Shift With Zero Crossing:
This partition does the testing of the shift method, which focuses on cases where the range crosses zero as a result of the shift operation. By testing this condition, it ensures that the class handles range shifting accurately, adjusting boundaries correctly without any outliers when crossing zero.

### 5.Shift Without Zero Crossing:
This partition is the opposite of the  previous partition, this partition examines the shift method's behavior when the range is shifted without crossing zero. It verifies that the range boundaries are appropriately adjusted without crossing the zero boundary, maintaining the correctness of the range.

### 6.Get Length for Different Ranges:
This partition aims to verify that even if its a positive, negative value the get length method calculates the correct range.

### 7: Nullshift exception: 
When testing the Shift method we put one of the parameters as null to check if it throws an exception and gives an error.

By considering these input partitions, the unit test strategy ensures a good  coverage of the Range class working. Each test case is designed to target specific aspects of the class's behavior, promoting effective verification and debugging.


## Detailed Description of Unit Test Strategy for DataUtilites.java:

### 1. Direct Row Access: 
  This partition verifies the method's ability to accurately calculate the total of all values in a specified row of a `Values2D` dataset. It ensures that the method correctly sums the elements of the row, taking into account the correctness of indexing and summing functionalities.
  
### 2. Primitive to Object Conversion:
  This partition focuses on the method's capability to convert an array of double primitives to an array of `Number` objects. By testing this functionality, it verifies the method handles the conversion correctly, ensuring each primitive value is encapsulated into a corresponding `Number` object, preserving the value accurately.

### 3. Cumulative Calculation Accuracy: 
  This partition aims to validate the correctness of cumulative percentage calculations within a `KeyedValues` dataset. It examines whether the method computes cumulative percentages correctly, ensuring the calculations are accurate and the results maintain the integrity of the original data, reflecting proper cumulative logic.

### 4. 2D Array Conversion Integrity:
  This section tests the method's ability to convert a 2D array of double primitives to a 2D array of `Number` objects without losing data integrity. It ensures the method accurately handles the conversion of each element, maintaining the original values and structure of the 2D array.

By adopting this structured approach to testing, similar to the one used for `Range.java`, we ensure comprehensive coverage and reliability of the methods within the DataUtilities class or similar utility classes. Each test case is meticulously designed to target specific functionalities, enabling effective validation and ensuring the methods perform as expected under various scenarios.




# 3 Test cases developed:


## Test Cases Developed for Range.java:
### Test Boundaries Directly                                                                                          
 Methods: getUpperBound() and getLowerBound()                                                                                    
 Description: Verifies if the lower and upper boundaries are set correctly when directly provided during initialization.

### Test Zero Length Range:                                                                                                                       
 Method: getLength()                                                                                                   Description: Ensures that the length of the range is correctly computed when the range has zero length.

### Test Contains at Boundaries:                                                                                                                     
 Method: Contains()                                                                                                                                      
 Description: Tests the contains method to verify if it correctly identifies whether the range contains boundary values.


### Test Shift With Zero Crossing:                                                                                                              
 Method: Shift()                                                                                                                                              
 Description: Validates the shift method's behavior when the range crosses zero.

### Test Shift Without Zero Crossing:   
 Method:Shift()                                                                                                                                                             
 Description: Checks if the shift method maintains the range boundaries without crossing zero.

### Test Get Length for Different Ranges:                                                                                                     
 Method: getLength()                                                                                                                                                  
 Description: Ensures that the getLength method calculates the correct length for negative, zero, and positive ranges.


 These test cases cover the input partitions identified in the test strategy, ensuring thorough testing of the Range class functionalities.



## Test Cases Developed for DataUtilities.java:

### Test Calculate Row Total:
 Methods: calculateRowTotal()
 Description: Verifies that the calculateRowTotal method accurately computes the sum of values within a specified row using a mocked Values2D object.

### Test Create Number Array:
 Methods: createNumberArray()
 Description: Ensures that the createNumberArray method correctly transforms an array of double primitives into an array of Number objects.

### Test Get Cumulative Percentages:
 Methods: getCumulativePercentages()
 Description: Tests the getCumulativePercentages method to confirm it accurately calculates the cumulative percentages of values in a KeyedValues dataset.

### Test Create Number Array2D with Valid Input:
 Methods: createNumberArray2D()
 Description: Assesses if the createNumberArray2D method can accurately convert a 2D array of double primitives into a 2D array of Number objects.


These test cases are designed to cover key functionalities within the DataUtilities class, ensuring comprehensive testing across a variety of input conditions. Through meticulous validation of method outputs and behaviors, these tests aim to identify potential issues or regressions within the DataUtilities implementations used in the JFreeChart library.




# 4 How the team work/effort was divided and managed:

Team Work was divided into two Groups. And we adopted the pair programming approach where within each group one was writing code and the other was the observer but we switched roles and cross checked each other's work. Rohan Kapila and Shayyan Asim tested the Range.java class whereas Qazi Ali and Fayzan Toor tested the DataUtilities.java class but both groups then tested each other’s assigned class and cross checked.


# 5 Difficulties encountered, challenges overcome, and lessons learned:

During our test making process for the DataUtilities class, we encountered some difficulty when implementing methods that needed Mocking to replicate their dependent classes. This was encountered when we specifically went to test the CumulativePercentages method that required KeyedValues as input to function. We tried to use the example Mock given in the github repo, but our test would not even run. By using the JUnit logs, we discovered the issue was based on the methods we were mocking being called once, when they were expected to be used multiple times. We had to use online resources and ChatGPT to figure out the implementation of calling methods multiple times. From this experience, we learned how to call on methods repeatedly while mocking.

# 6 Comments/feedback on the lab itself:

This assignment was a fun way to get hands-on experience with Junit testing and understanding the importance of testing in software engineering. It taught us how we should design test cases by coding and then running them. The lab was designed nicely and it was easy to run through every step however for windows user in our group we were not able to render the index.html file, in future we hope that all files given to us by lab instructions are capable on running on any type of OS.



