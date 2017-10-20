# Assignment 05: Getting Loopy

## Go Loop Translation Challenge

_Lost in Translation._

---

_“If I had to describe Go with one word it’d be ‘sensible’.” – Christoffer Hallas_

---

**MAKE THIS HAPPEN:**

Turn this Go loop into its Java equivalent. 

You are encouraged to [play with this code](https://tio.run/##bZBfT4MwFMXf@ymuTWZA2VJi9rKJCZE5l0xj3B5NTIUWm0EhwGaM2WdnpQME9IGG3D@/c@4Jk7JMqb@jIYOYColEnCZZAZjHBUaI76Wv64YJPwjAT2RewGbrvm5Xz8v39ephAQ7YhCDVjARna8YLmDn9EdUTuRuJA6taRbZnFeqTypB5Ik8j@l3VMa4gPMm0EsCBZhp5rwdByEKXlbHJxqeSG3gUYAsuf2dMPYD028cr@uPCXWPdErzLvXWA1Ir/bHlPy/PS8Yxtb7x2OhDU5er23SCkRqAd@BuR0gAW5azH6bnrLJN5XWuCdYBTtdz1OrhzAKrLVw6M7XpLp9dk/JKpxKuQp7kxIjeBOQN9SfX/JlXwvaysDtNqjZqtkYvGZ2PhI2N0N2@FteVWNpIG9hgNQCZfE2yiIypLG9kEje2p@gg5AQ) You can type in your input in the Input section and then type Ctrl+Enter to run the code on that input. The result will appear in the Output section. If you create a situation that causes an infinite loop, you should refresh the page.


    package main
    import "fmt"

    func main() {
        const STARTING_LIFE = 100

        lifeLeft := STARTING_LIFE
        isAlive := true
        changeDisplay := ""

        for {
            var lifeChange int
            fmt.Scanf("%d", &lifeChange)
            

            changeDisplay = "HEAL"
            if lifeChange <= 0 {
                changeDisplay = "DMG"
            }

            lifeLeft += lifeChange

            if lifeLeft > STARTING_LIFE {
                lifeLeft = STARTING_LIFE
            } else if lifeLeft <= 0 {
                lifeLeft = 0;
                isAlive = false
            }

            if lifeChange < 0 {
                lifeChange *= -1
            }
            
            fmt.Printf("%5s(%03d): LIFE %03d\n", changeDisplay, lifeChange, lifeLeft)

            if !isAlive {
                break;
            }
        }

        fmt.Println("Dead now.")
    }


**NOTES:**
1. Go syntax hints:
    * Go uses `:=` instead of `=` for assignment.
    * Go uses `const` to declare constants.
    * `fmt.Scanf("%d", &var)` reads an integer from the keyboard and stores in into variable `var`.
    * Go's `Printf` works just like Java's `printf`.
    * Go doesn't have a while loop; instead a for loop is used that breaks out when a certain exit condition is true.
1. Do **not** use a break to accomplish this task.
1. Although Go does not have while loops, Java does - so do **not** use a for loop to accomplish this task.
1. You will only be given _one_ automated test for this challenge - you are expected to come up with more on your own. You are strongly encouraged to test your code manually. _Look carefully at the output produced - you must match it exactly for your code to pass **our** automated tests!_