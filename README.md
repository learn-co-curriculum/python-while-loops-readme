
# While Loops

## Introduction
After writing enough for loops to fill a novel where the next line is a an `if` statement, we must be asking ourselves if there is a better way? Or asking ourselves if there is a way to have a loop **without** a collection to iterate over? Well, this is where **while** loops come into play. We can use a while loop to perform the same action over and over until a condition is met. We don't even need an *iterable* or collection to iterate over. We can just define a condition an perform the while block until the condition is met. Pretty cool, right? 

## Objectives
* Understand how wile loops work
* See how while loops can replace simple for loops with conditional statements

## What is a `while` loop and how does it work?

A while loop is just that; a loop! Similar to a for loop, except there is no need for a collection to iterate over. Instead, a while loop uses a condition to know when to stop executing. When the condition is true, the block inside the while loop is executed. When that condition is false, we exit the while loop and move on to the next piece of our code.

Let's look at an example:


```python
stop_number = 4
while stop_number > 0:
    print(stop_number)
    stop_number -=1
print("The stop_number reached", stop_number, "so the while loop's condition became False and stopped execution")
```

Note the lack of a `list` or other collection, and that our second print statement only printed after our stop_number become 0.

Also, notice that the structure of a while loop is such that it could execute for an *unkown* amount of times. For example, if we didn't know the stop_number because it changed from time to time, our while loop could execute more 100 times or 3. 

For example, if we used a random number:


```python
import random
random_num = random.randint(1,20)
while random_num > 0:
    random_num -= 1
    print(random_num)
```

However, we know that eventually that number will be less than 0 and the loop will eventually stop. This is of critical importance. A while loop must always have a condition that will stop the loop, otherwise we will have an **infinite** loop. Infinite loops can crash your browser or program, if you don't have a way to end it, so, it is very important to make sure your loops have a fairly defined **end** case.

*If you do ever accidentally create an infinite loop, don't worry. Your current tab or browser might freeze, and then kill the page to stop the execution. You can then re-open the browser again normally.*

## When To Use While Loops

While loops are fairly straight forward. We use them in instances where we have a **condition** that serves as the point at which we want a process to stop. For example, if we think about our apetite, we should eat until we aren't hungry, right? Some days that might be two slices of pizza, some days that might be 5 slices of pizza (and that is assumes all pizza slices to be of equal size, which is a *generous* assumption).

![liz_lemon_eating_pizza](liz_lemon_eating_pizza.gif)

In keeping with our food theme, let's see how we can make sure we're drinking enough water during the day using a while loop:


```python
hydration = 0
water = 1 # in gallons
while hydration < 100 and water > 0:
    print('----[sips water]-----')
    water -= .1
    print('ah, that was refreshing')
    hydration += 10
    print("hydration is now at", hydration, "%\n")
```

## Summary

Awesome! While loops are great, right? We can use them to perform operations based on the truthiness of a condition instead of needing to iterate over the elements in a collection. They provide a more dynamic way to perform an operations, but we need to be careful when writing while loops because we need there to be a condition that ends the loop. Otherwise we will have an **infinite** loop which will give us and our computer a real headache.
