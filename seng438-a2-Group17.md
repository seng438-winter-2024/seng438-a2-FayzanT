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

Detailed Description of Unit Test Strategy for Range.java:

## Boundaries Directly: 
This partition focuses on testing the correctness of the lower and upper boundaries directly when provided during initialization. It ensures that the range object sets its boundaries accurately based on the input values.

## Zero Length Range: 
This partition examines the scenario where the range has zero length. By testing this condition, it verifies whether the class handles cases where the lower and upper bounds are equal appropriately, ensuring that the length calculation is correct.
Contains at Boundaries: This partition targets the contains method, specifically testing its behavior with boundary values. It validates whether the method correctly identifies whether the range contains its boundary values or not, covering both inclusive and exclusive boundary scenarios.
## Shift With Zero Crossing: 
This partition tests the shift method, focusing on scenarios where the range crosses zero as a result of the shift operation. By testing this condition, it ensures that the class handles range shifting accurately, adjusting boundaries accordingly without unexpected behavior when crossing zero.
## Shift Without Zero Crossing: 
Unlike the previous partition, this section examines the shift method's behavior when the range is shifted without crossing zero. It verifies that the range boundaries are appropriately adjusted without crossing the zero boundary, maintaining the integrity of the range.
Get Length for Different Ranges: This partition aims to validate the correctness of the getLength method across different types of ranges: negative, zero, and positive. By testing these scenarios, it ensures that the method accurately calculates the length of the range regardless of its position relative to zero.

By considering these input partitions, the unit test strategy ensures comprehensive coverage of the Range class functionality, guaranteeing its correctness and reliability under various scenarios. Each test case is designed to target specific aspects of the class's behavior, facilitating effective validation and debugging.


# 3 Test cases developed

Out of the 15 methods we tested the following 5 methods.

Test Cases Developed for Range.java:
Test Boundaries Directly                                                                                                                             
Methods: getUpperBound() and getLowerBound()                                                                                    
Description: Verifies if the lower and upper boundaries are set correctly when directly provided during initialization.

Test Zero Length Range:                                                                                                                       
Method: getLength()                                                                                                                
Description: Ensures that the length of the range is correctly computed when the range has zero length.

Test Contains at Boundaries:                                                                                                                     
Method: Contains()                                                                                                                                      
Description: Tests the contains method to verify if it correctly identifies whether the range contains boundary values.


Test Shift With Zero Crossing:                                                                                                              
Method: Shift()                                                                                                                                              
Description: Validates the shift method's behavior when the range crosses zero.

Test Shift Without Zero Crossing:   
Method:Shift()                                                                                                                                                             
Description: Checks if the shift method maintains the range boundaries without crossing zero.

Test Get Length for Different Ranges:                                                                                                     
Method: getLength()                                                                                                                                                  
Description: Ensures that the getLength method calculates the correct length for negative, zero, and positive ranges.


These test cases cover the input partitions identified in the test strategy, ensuring thorough testing of the Range class functionalities.









# 4 How the team work/effort was divided and managed

Team Work was divided into 2 Groups. And we adopted the pair programming approach where within each group one was writing code and the other was the observer but we switched roles and cross checked each other's work. Rohan Kapila and Shayyan Asim tested the Range.java class whereas Qazi Ali and Fayzan Toor tested the DataUtilities.java class but both groups then tested each other’s assigned class and cross checked.


# 5 Difficulties encountered, challenges overcome, and lessons learned

Text…

# 6 Comments/feedback on the lab itself

Comments/Feedback:  This assignment was a fun way to get hands-on experience with Junit testing and understanding the importance of testing in software engineering. It taught us how we should design test cases by coding and then running them. 


