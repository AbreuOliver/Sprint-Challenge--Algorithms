#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) Runtime Analysis: Linear: O(n)

b) Runtime Analysis: Quadratic/Polynomial: O(n^2)

c) Runtime Analysis: Linear: O(n)

## Exercise II

n = total stories of building (ex: 25 stories)
f = highest floor from which eggs are not broken when dropped

Goal: Determine the value of f in a way that breaks the least number of eggs (in least amount of attempts)

Psuedocode:

1. declare highest floor of building ( n )
2. go to highest floor of building, so that current floor equals highest floor ( c = n )
3. from current floor, determine middle floor ( m = c/2 )
    4. from new current floor, drop 1 egg ( new_c = m )
        5. if egg breaks, go back to step 3
        6. if egg does not break, add 1 to new current floor ( new_c + 1 )
            7. if egg does not break, go back to step 6
            8. if egg breaks, then the highest floor from which eggs are not broken when dropped is the new current floor ( return f = new_c ) END

> Runtime Analysis: Logarithmic O(log n) - This seems like a variation of the 'guessing game', which assumes a sorted array of floors, as well as one correct answer (the highest floor from which eggs are not broken when dropped). By performing a slightly modified binary search, one can arrive at the correct answer
