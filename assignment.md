# Probability Distributions

## Introduction

In this assignment, we will work with some common probability distributions. Often we have to identify what distribution we should use to model a real-life
situation. This exercise well get you some practice doing so.

**Please don't follow this assignment linearly. Feel free to skip so you can attempt more questions before seeing the solution.**

## Part 1: Identifying Distributions

For each question in this module, you can use `scipy.stats` module to help you calculate the results. You can following the following steps.

- Name the most appropriate distribution and the associated parameter(s)
- Set up equation for the distribution, e.g.
- Use the distribution to calculate the result.

 For example, if using Jupyter notebook, the solution to the first question in part 1 can be written as the following.

  ```python
  from scipy import stats
  dist = stats.poisson(mu=2)
  print(f'P(X = 0) = {dist.pmf(0)}')
  ```

> You can choose to skip some so you can start working on some programming exercises in the `advanced` section.

1. A typist makes on average 2 mistakes per page.  What is the probability of a particular page having no errors on it?
    - hint: You are looking at error **rate** per page.

2. Components are packed in boxes of 20. The probability of any individual component being defective is 10%. What is the probability of a box containing exactly 2 defective components?
    - hint: 20 **independent** components with a **binary** status: normal or defective.

3. Components are packed in boxes of 20. The probability of any individual component being defective is 10%. What is the probability of a box containing `AT MOST` 2 defective components?
    - hint: Find all possibilities of `AT MOST 2` defective components.

4. Patrons arrive at a local bar at a rate of 30 per hour. What is the probability that the bouncer can take a three minute bathroom break without missing the next patron?
    - hint 1:  Reduce the rate from `person/hour` to `person/minute`
    - hint 2:  Probability of `time before event happens` follows an exponential distribution.

5. You need to find a tall person, at least 6 feet tall, to help you reach a cookie jar. 8% of the population is 6 feet or taller, and people pass by on average twice per minute.  If you wait on the sidewalk, what is the probability that you will have to wait longer than ten minutes to get some cookies?
    - hint 1: Find the rate of `number of tall person/minute`.
    - hint 2: The problem is reduced to an exponential distribution function.

6. A harried passenger will be several minutes late for a scheduled 10 A.M. flight to NYC. Nevertheless, he might still make the flight, since boarding is always allowed until 10:10 A.M., and boarding is sometimes permitted up to 10:30 AM.

Assuming the end time of the boarding interval is **uniformly distributed** over the above limits, find the probability that the passenger will make his flight, assuming he arrives at the boarding gate at 10:25.

7. Your cat starts to beg for dinner at 3:30 every day, and you suspect that it meows at a fixed rate. You've observed that about one fifth of the time your cat will not meow until 3:40, giving you 10 unexpected minutes of quiet. What is the probability your cat leaves you alone for 30 minutes?
    - hint : First find the parameter for the distribution, then use the parameter you found to calculate the unknown probability.

8. Somehow you ended up with two types of forks.  There are the good forks, which are big and fit a healthy bite, but there are also these small, thin ones that you don't really understand what they are for, you should probably just get rid of them.  You need two forks for you and your partner, and grab a fistful of 5.  If there are 14 forks in the drawer, of which half are the good kind, what is the probability you have **at least** your two required good forks?
    - hint 1: This is a hypogeometric distribution problem.
    - hint 2: Decompose all possibilities of `at least` two good forks, namely 2 good forks, 3, 4 and 5.


## Part 2: Working with Distributions

### 1

*You are given a 20-sided die.*
- P(rolling between 6 and 9 - inclusive)
- P(rolling at least 12)
- P(rolling no more than 3)
- Plot the distribution.

### 2

*A light switch works 1 out of 5 times. You attempt to turn the light on 15 times.*
- P(turning on exactly 9 times)
- P(turning on < 4 times)
- P(turning on >= 3 times)
- Plot the distribution.

### 3

*A factory worker, on accident, breaks 3 widgets per hour*
- P(1 widget will be broken per hour)
- P(between 4 and 7, inclusive, will be broken per hour)
- P(less than 6 will be broken per hour)
- Plot the distribution.

### 4

*You are given a data file, sqft.csv, that contains the area in square feet from randomly selected houses in the United States*
- P(a house will contain 830 +/- 25 sqft)
- P(a house will have more than 3000 sqft)
- P(a house will have less that 275 sqft)
- Plot the distribution.

## Part 3: Basic Concepts

#### Sets

1. Out of the students in a class, 60% are geniuses, 70% love chocolate,
   and 40% fall into both categories. Determine the probability that a
   randomly selected student is neither a genius nor a chocolate lover.

#### Combinatorics

1. A fair 6-sided die is rolled three times, independently. Which is more likely: a
   sum of 11 or a sum of 12?

2. 90 students are to be split at random into 3 classes of equal size. Joe and Jane are
   two of the students. What is the probability that they end up in the same
   class?

3. A well-shuffled 52-card deck is dealt to 4 players. Find the probability that
   each of the players gets an ace.
