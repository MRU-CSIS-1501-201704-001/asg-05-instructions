# Assignment 05: Getting Loopy

## GPA Chart Challenge

_It's full of stars._

---

_A small college wants to be able to quickly see how well their students are doing. You have been contracted to design, then implement a program to create a program that prints out a simple graphical representation of the GPA distribution of students._

_At this college, a student earns Honours status if the GPA is 3.6 or above. They fail if it is under 2.0._

_Your boss likes asterisks. A lot. So you decide to use asterisks to do the graphical representation, ‘cause sucking up and all._

---

**MAKE THIS HAPPEN:**

1. Prompt for and read in the number of students.
    1. You can assume that the user enters in an integer – but you can’t assume that it will be a valid one!
    1. If the user enters in a number <= 0, give a descriptive error message and terminate the program.
1.	Read in the GPA for each student. Don’t prompt for these numbers.
    1. You can assume all GPAs entered are legal, that is, values >= 0.0 and <= 4.0.
    1. Each GPA is separated from the next by white space (spaces, tabs, newlines).
1. Print out a graph that shows the distribution of GPA categories for those students. (see the example below)


**Example 1**  

    Assume that there were 10 students: 3 with Honours, 5 who passed, and 2 who failed. 
    Then we would output the following:

    GPA Distribution

    Honours   :***
    Pass      :*****
    Fail      :**

**Example 2**  

    Assume that there were 10 students: 1 with Honours, 4 who passed, and 0 who failed. 
    Then we would output the following:

    GPA Distribution

    Honours   :*
    Pass      :****
    Fail      :

**NOTES:**

* Your graph should have the title GPA Distribution.
* The label field (with ‘Honours’, ‘Pass’, ‘Fail’) should have a width of 10.
* If a GPA category has 0 students in it (nobody failed, for example), you still need to print the label and colon – you just won’t print any stars.
* You will only be given one automated test for this challenge - you are expected to come up with more on your own. You are strongly encouraged to test your code manually. Look carefully at the output produced - you must match it exactly for your code to pass our automated tests!
