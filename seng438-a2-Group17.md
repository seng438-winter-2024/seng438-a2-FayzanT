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

Text…

# 5 Difficulties encountered, challenges overcome, and lessons learned

Text…

# 6 Comments/feedback on the lab itself

Text…
