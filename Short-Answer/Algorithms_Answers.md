#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)  O(n) - because the number of loops we have to perform directly correlates with `n`. As `n` increases we always perform `n` number of loops until our conditional returns false and ends the loop. IE: If `n` = 4, we have to perform 4 loops. Basically, the third `n` in our while loop will determine how many loops we must perform. Since we increase `a` by (`n` * `n`) it sort of cancels out the first (`n` * `n`) in our while conditional leaving us with just `n`.


b)  O(log (n)) - because as `n` grows in size, the amount of operations we must perform does NOT increase linearly with `n`. Since we set `j` to 2 x itself each loop, we essentially cut away half of the problem each time, and this continual halfing makes me think our runtime is O(log (n)). As `n` grows larger and larger, the number of operations to perform shouldn't increase by much, over time.


c)  O(bunnies) - because the number of loops we have to perform directly correlates with `bunnies`. In this case we're basically performing a fancy loop using recursion. With each "loop" we subtract 1 from `bunnies`, bringing us a step closer to our base case where we want to break out of the loop, aka when `bunnies` == 0. Since we just decrease by one each time, we reach our base case in the same amount of steps as the number we pass in to the function.

## Exercise II

I'm not really sure what to do here... In real life, I would drop an egg from each floor, starting at the lowest. If the egg breaks, I found `f` aka the floor at which eggs will break if dropped. If not, I'll go up a floor and try again... So we will have to break at least one egg to see where that point is... I suppose my code for that might look something like this:

def egg_drop(n):
    f = 0
    broken_eggs = 0

    for i in range(n):
        < code to somehow test dropping an egg and see if it breaks >
        if broken_eggs == 1:
            f = i
        
    return f

