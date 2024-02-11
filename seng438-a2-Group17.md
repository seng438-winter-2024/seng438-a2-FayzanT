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

Range.java:
Boundaries Directly: Tests the accuracy of lower and upper boundaries set during initialization.
Zero Length Range: Examines cases where the range has zero length to ensure correct length calculation.
Contains at Boundaries: Checks the contains method for correct identification of boundary values.
Shift With Zero Crossing: Tests the shift method for scenarios where shifting results in crossing zero.
Shift Without Zero Crossing: Focuses on the shift method when shifting does not result in crossing zero.
Get Length for Different Ranges: Validates the getLength method across ranges of negative, zero, and positive lengths.

DataUtilities.java:
Testing calculateRowTotal Method: Aims to verify accurate calculation of total values in a row of a Values2D dataset.
Testing createNumberArray Method: Ensures correct conversion of a double array to a Number[].
Testing getCumulativePercentages Method: Verifies accurate computation of cumulative percentages for a KeyedValues dataset.
Testing createNumberArray2D Method: Confirms correct conversion of a 2D double array to a 2D Number[].
Overall Strategy:
Mocking Dependencies: Uses mocking to isolate methods under test, allowing for controlled inputs and outcomes.
Assertion Precision: Utilizes assertions to check for equality, type correctness, and non-null results.
Incremental Testing: Focuses each test on a specific method to clarify functionality testing.
Coverage: Aims to cover a broad range of functionalities within the DataUtilities class.


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









# 4 How the team work/effort was divided and managed

Team Work was divided into 2 Groups. And we adopted the pair programming approach where within each group one was writing code and the other was the observer but we switched roles and cross checked each other's work. Rohan Kapila and Shayyan Asim tested the Range.java class whereas Qazi Ali and Fayzan Toor tested the DataUtilities.java class but both groups then tested each other’s assigned class and cross checked.


# 5 Difficulties encountered, challenges overcome, and lessons learned

During our test making process for the DataUtilities class, we encountered some difficulty when implementing methods that needed Mocking to replicate their dependent classes. This was encountered when we specifically went to test the CumulativePercentages method that required KeyedValues as input to function. We tried to use the example Mock given in the github repo, but our test would not even run. By using the JUnit logs, we discovered the issue was based on the methods we were mocking being called once, when they were expected to be used multiple times. We had to use online resources and ChatGPT to figure out the implementation of calling methods multiple times. From this experience, we learned how to call on methods repeatedly while mocking.

# 6 Comments/feedback on the lab itself

Comments/Feedback:  This assignment was a fun way to get hands-on experience with Junit testing and understanding the importance of testing in software engineering. It taught us how we should design test cases by coding and then running them. 


