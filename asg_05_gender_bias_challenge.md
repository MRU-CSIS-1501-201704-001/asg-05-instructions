# Assignment 05: Getting Loopy

## Gender Bias Challenge

_Good luck with that playing God thing._

---

_Adapted this from a Martin Gardner book - Entertaining Mathematical Puzzles - where he explains he himself got it from a book by George Gamow and Marvin Stern._

_Image there's some jerkwad misogynistic military leader of some kingdom that rules his people with an iron fist. He decrees that in order to increase the size of his (males-only) army, that from this point forward, a woman can only have multiple children if she gives birth to a boy - if she gives birth to a girl, she can no longer have any children._

_Assuming that the people follow this rule without question, what effect do you think this policy will have on the male:female ratio over time? Let's build a simulation to find out!_

---

**MAKE THIS HAPPEN:**

1. Create a table showing the results of running 10 simulations, each consisting of the ratio of boys to girls born to 10,000 mothers under this policy.
    * Your results should have the following format:  
        1. The first row is this header row: `Run#[2 spaces]M[1 space]:[1 space]F[newline]`
        1. The next 10 rows have this format:   
            `<run#>[2 spaces]1[1 space]:[1 space]<# females to 1 male>[newline]`
            1. The `<run#>` part is in a field of width 4.
            1. The `<# females to 1 male>` part must be rounded to 5 decimal places. (Ex. 2.13001)
        1. If you deviate from this format, the automated tests will fail.

Example (doesn't show correct numbers, though!):  

    Run# M : F  
       1 1 : 2.00132  
       2 1 : 1.99312
       ... etc

**NOTES:**

* We'll assume that every birth results in a single child (no twins, triplets, etc.), that every child lives, and that the odds of having a boy is 50%.
* You'll likely find it useful to look through section 4.10 (_Application: Random Numbers and Simulations_) in the text.
* Taking a skim through the Random class in the Java 8 API would be useful. Some methods you'll find there are more readable than others, especially for this challenge.
* You **must** use `Random randomGenerator = new Random(1);` when you are ready to test your code with Cucumber. This way, your results (if you've coded things correctly) will match what the tests are looking for. (Do you understand why?) Before this point, you **don't** need to use `Random(1)` - you should use `Random()`.
