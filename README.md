# Yearly Technical Interview Prep Guide
*This is a personal and opinionated guide, but feel free to use it if it's helpful to you.*

Damn, is it already that time of year again? It felt like just yesterday that you had secured your career plans and were smooth sailing. This guide serves as a reminder for how you've prepared for technical interviews in the past in order to hopefully save you time in the future.

## Quick links

* Open source, comprehensive guide for technical interviews: https://techinterviewhandbook.org/

## 1. Recall the structure of a technical interview (~hours)

Technical interviews often follow a set structure that you can gamify:

1. **Listen to the problem**
   * Your interviewer will ask you a technical question, or will write one down for you to read
   * *Avoid jumping into the problem too fast* -- you want a breadth-first search of the solution space, not a depth-first search
   * *Clarify the specifics, and ask about corner cases* -- this is your time to show the interviewer that you can quickly identify and resolve corner cases
2. **Create a few examples / test cases**
   * *These examples should be as simple as possible*, as they will be used to step through a solution once completed
   * *Create a test case for each noted corner case* -- this is the time to identify corner cases
3. **Start thinking about solutions**
   * Have a direction? Write out pseudocode for your solution
     * *Think about specific implementation details here (control structures, data structures, variables, etc.)* -- we want to frontload as much of the thinking here as possible, as it's much messier to backtrack in the implementation stage
     * *Want to map out all information needed for implementation*
   * Stuck?
     1. Think about how certain key data structures could be used to solve this problem
     2. Start with the brute-force solution, and look for optimizations -- bottlenecks, unused information, unnecessary work, duplicated work
     3. Think about how you would solve it and translate that intuition into an algorithm
     4. Solve a simpler version of the problem and then expand the solution
4. **Do a pass over the algorithm before implementation**
   * *Identify the time and space complexity*
   * *Run through an example manually*
5. **Implement the solution**
6. **Manually run through the solution using an example**
7. **Write formal tests for the solution**

## 2. Review key data structures and algorithms (~weeks)

Below is a table containing the key data structures, algorithms, and concepts that should be reviewed in preparation for technical interviews. They are loosely ordered by importance.

|    Data Structures     |      Algorithms      |        Concepts         |
| :--------------------: | :------------------: | :---------------------: |
|     Arrays / lists     |    Binary search     |  Big O time and space   |
|   Hash tables / sets   |  Depth-first search  |        Recursion        |
|        Strings         | Breadth-first search |   Dynamic programming   |
|      Linked lists      |      Quick sort      | Memory (stack vs. heap) |
|    Stacks & Queues     |      Merge sort      |    Bit manipulation     |
| Trees, Tries, & Graphs |                      |                         |
|         Heaps          |                      |                         |

Review each data structure with these steps:

1. Review the common use-cases and benefits
2. Review the time and space complexity for key operations + understand why that is the case
3. Review the syntax in your langauge of choice

Review each algorithm with these steps:

1. Review the common use-cases and benefits
2. Review the time and space complexity
3. Review the syntax or implementation patterns in your language of choice

Review each concept with these steps:

1. Write out a general overview of the concept
2. Review the common use-cases and benefits
3. Review the implementation patterns in your language of choice

## 3. Practice LeetCode problems (~months)

LeetCode problems should be used to practice key concepts and the use of key data structures and algorithms. Problems should be picked intentionally with this in mind.

Aim to do 5-7 problems a week. When solving a problem, set a timer for 30 minutes wherein you attempt to solve the problem with no assistance. If you reach the end of the 30 minutes and you have made no considerable progress towards a solution, look at the LeetCode solutions and explanations and **ensure that you completely understand the solution** by explaining it to yourself via comments, and then coding out the solution yourself.

Below is a list of some good collections of practice questions that you've used in the past:

* https://techinterviewhandbook.org/best-practice-questions

## 4. Do some mock interviews (~hours)

Find some friends to do mock interviews with. Aim to do at least one, but ideally 3+. Offer to do a mutual interview-for-interview.

If you can't find any friends to do mock interviews with, consider using [Pramp](https://www.pramp.com/), a free mock interviewing platform (I've never used it, but I remember looking into it once).

## 5. Practice the soft stuff (~hours)

A technical interview is still an interview. Being personable and prepared to talk about yourself is important for leaving a good impression.

Review the points on your resume and be prepared to talk about each. 

Prepare stories for the bigger items by outlining the main points you'd like to get across and practicing cohesively covering them all.

Practice everything out-loud.
