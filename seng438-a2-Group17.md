**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#2 – Requirements-Based Test Generation**

| Group \#:      |   17  |
| -------------- | --- |
| Rohan Kapila | 30145862 |
| Fayzan Toor               | 30141139    |
| Shayyan Asim               |  30149567   |
| Qazi Saboor               | 30142452    |

# 1 Introduction

In this assignment we are tasked to test 2 different classes. DataUtilities.java and Range.java using Junit. The objective of this assignment is to educate students on the fundamentals of automated unit testing, emphasizing testing procedures aligned with the specific requirements of each unit. JUnit, a prominent member of the XUnit framework family, serves as the primary unit testing framework for Java.

# 2 Detailed description of unit test strategy

# Detailed Description of Unit Test Strategy for Range.java:

1. Boundaries Directly: This partition focuses on testing the correctness of the lower and upper boundaries directly when provided during initialization. It ensures that the range object sets its boundaries accurately based on the input values.

2. Zero Length Range: This partition examines the scenario where the range has zero length. By testing this condition, it verifies whether the class handles cases where the lower and upper bounds are equal appropriately, ensuring that the length calculation is correct.

3. Contains at Boundaries: This partition targets the contains method, specifically testing its behavior with boundary values. It validates whether the method correctly identifies whether the range contains its boundary values or not, covering both inclusive and exclusive boundary scenarios.

4. Shift With Zero Crossing: This partition tests the shift method, focusing on scenarios where the range crosses zero as a result of the shift operation. By testing this condition, it ensures that the class handles range shifting accurately, adjusting boundaries accordingly without unexpected behavior when crossing zero.

5. Get Length for Different Ranges: This partition aims to validate the correctness of the getLength method across different types of ranges: negative, zero, and positive. By testing these scenarios, it ensures that the method accurately calculates the length of the range regardless of its position relative to zero.

By considering these input partitions, the unit test strategy ensures comprehensive coverage of the Range class functionality, guaranteeing its correctness and reliability under various scenarios. Each test case is designed to target specific aspects of the class's behavior, facilitating effective validation and debugging.


# Detailed Description of Unit Test Strategy for DataUtilites.java:

1. Direct Row Access: This partition verifies the method's ability to accurately calculate the total of all values in a specified row of a `Values2D` dataset. It ensures that the method correctly sums the elements of the row, taking into account the correctness of indexing and summing functionalities.
  
2. Primitive to Object Conversion: This partition focuses on the method's capability to convert an array of double primitives to an array of `Number` objects. By testing this functionality, it verifies the method handles the conversion correctly, ensuring each primitive value is encapsulated into a corresponding `Number` object, preserving the value accurately.

3. Cumulative Calculation Accuracy**: This partition aims to validate the correctness of cumulative percentage calculations within a `KeyedValues` dataset. It examines whether the method computes cumulative percentages correctly, ensuring the calculations are accurate and the results maintain the integrity of the original data, reflecting proper cumulative logic.

4. 2D Array Conversion Integrity: This section tests the method's ability to convert a 2D array of double primitives to a 2D array of `Number` objects without losing data integrity. It ensures the method accurately handles the conversion of each element, maintaining the original values and structure of the 2D array.

By adopting this structured approach to testing, similar to the one used for `Range.java`, we ensure comprehensive coverage and reliability of the methods within the DataUtilities class or similar utility classes. Each test case is meticulously designed to target specific functionalities, enabling effective validation and ensuring the methods perform as expected under various scenarios.




# 3 Test cases developed

Out of the 15 methods we tested the following 5 methods.

# Test Cases Developed for Range.java:
# Test Boundaries Directly                                                                                          
 Methods: getUpperBound() and getLowerBound()                                                                                    
 Description: Verifies if the lower and upper boundaries are set correctly when directly provided during initialization.

# Test Zero Length Range:                                                                                                                       
 Method: getLength()                                                                                                   Description: Ensures that the length of the range is correctly computed when the range has zero length.

# Test Contains at Boundaries:                                                                                                                     
 Method: Contains()                                                                                                                                      
 Description: Tests the contains method to verify if it correctly identifies whether the range contains boundary values.


# Test Shift With Zero Crossing:                                                                                                              
 Method: Shift()                                                                                                                                              
 Description: Validates the shift method's behavior when the range crosses zero.

# Test Shift Without Zero Crossing:   
 Method:Shift()                                                                                                                                                             
 Description: Checks if the shift method maintains the range boundaries without crossing zero.

# Test Get Length for Different Ranges:                                                                                                     
 Method: getLength()                                                                                                                                                  
 Description: Ensures that the getLength method calculates the correct length for negative, zero, and positive ranges.


 These test cases cover the input partitions identified in the test strategy, ensuring thorough testing of the Range class functionalities.



# Test Cases Developed for DataUtilities.java:

# Test Calculate Row Total:
 Method:calculateRowTotal()
 Description: Verifies that the calculateRowTotal method accurately computes the sum of values within a specified row using a mocked Values2D object.

# Test Create Number Array:
 Methods:createNumberArray()
 Description: Ensures that the createNumberArray method correctly transforms an array of double primitives into an array of Number objects.

# Test Get Cumulative Percentages:
 Methods:getCumulativePercentages()
 Description: Tests the getCumulativePercentages method to confirm it accurately calculates the cumulative percentages of values in a KeyedValues dataset.

# Test Create Number Array2D with Valid Input:
 Methods:createNumberArray2D()
 Description: Assesses if the createNumberArray2D method can accurately convert a 2D array of double primitives into a 2D array of Number objects.


These test cases are designed to cover key functionalities within the DataUtilities class, ensuring comprehensive testing across a variety of input conditions. Through meticulous validation of method outputs and behaviors, these tests aim to identify potential issues or regressions within the DataUtilities implementations used in the JFreeChart library.




# 4 How the team work/effort was divided and managed

Team Work was divided into 2 Groups. And we adopted the pair programming approach where within each group one was writing code and the other was the observer but we switched roles and cross checked each other's work. Rohan Kapila and Shayyan Asim tested the Range.java class whereas Qazi Ali and Fayzan Toor tested the DataUtilities.java class but both groups then tested each other’s assigned class and cross checked.


# 5 Difficulties encountered, challenges overcome, and lessons learned

During our test making process for the DataUtilities class, we encountered some difficulty when implementing methods that needed Mocking to replicate their dependent classes. This was encountered when we specifically went to test the CumulativePercentages method that required KeyedValues as input to function. We tried to use the example Mock given in the github repo, but our test would not even run. By using the JUnit logs, we discovered the issue was based on the methods we were mocking being called once, when they were expected to be used multiple times. We had to use online resources and ChatGPT to figure out the implementation of calling methods multiple times. From this experience, we learned how to call on methods repeatedly while mocking.

# 6 Comments/feedback on the lab itself

Comments/Feedback:  This assignment was a fun way to get hands-on experience with Junit testing and understanding the importance of testing in software engineering. It taught us how we should design test cases by coding and then running them. 


