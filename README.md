# Yearly Technical Interview Prep Guide
*This is a personal and opinionated guide, but feel free to use it if it's helpful to you.*

Other guides:

* [System Design Interview Guide](system-design.md)
* [Internship Guide](internships.md)

## Quick links

* Open source, comprehensive guide for technical interviews: https://techinterviewhandbook.org/
* LeetCode questions to practice in order of importance: https://jeremyaguilon.me/blog/ranking_interview_questions_by_cram_score
* A curated list of LeetCode questions organized by practiced skill: https://neetcode.io/

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
     2. Try visualizing the problem in multiple different ways. Sometimes a change in perspective can reveal key patterns in the problem
     3. Consider if the problem can be broken down into multiple simpler cases
     4. Think about what truths you can state about the algorithm that can help simplify to a solution
     5. Think about how you would solve it and translate that intuition into an algorithm
     6. Solve a simpler version of the problem and then expand the solution
     7. Start with the brute-force solution, and look for optimizations -- bottlenecks, unused information, unnecessary work, duplicated work
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

* Review the points on your resume and be prepared to talk about each.
* Prepare stories for the bigger items by outlining the main points you'd like to get across and practicing cohesively covering them all.
* Practice everything out-loud.

Use the table below to prepare some answers to common behavioral questions:

|            | Experience 1                                                 | Experience 2 |
| ---------- | ------------------------------------------------------------ | ------------ |
| Leadership | (Show ownership on a project, a team, etc.)                  |              |
| Teamwork   | (Provide examples of interpersonal soft-skills: getting & giving help, communication, documentation, etc.) |              |
| Success    | (What unique trait do you have that brings success?)         |              |
| Challenges | (What have you learned to handle challenging work? What steps do you take to ensure success?) |              |
| Failures   | (How do you recover from failures?)                          |              |

## Miscellaneous Tips

Talk a lot during the interviews. Avoid awkward silence where they might think you're stuck by literally saying "I'm thinking about X...".

Drink a little bit of coffee about 1 hour before the interviews for an extra boost.

Keep a log of the LeetCode problems you do, and write notes when you learn something.

In general, if something seems wildly complex with many different cases and corner-cases, you've likely missed some key realization in the problem that makes it more reasonable to solve.

Try to think about what truths you can state about the algorithm that can help simplify a solution. For example: "picking the interval that ends soonest leaves the most room for future intervals" or "this sub-problem has no dependence on what has come before, so it can be computed independently".

When determining the runtime of recursive algorithms, think about the branching factor and maximum depth of recursive calls and how those change based on input size.

Remember that dynamic programming is more than just memoization in a recursive solution. Sometimes the iterative version of the algorithm (the one that computes the solutions to sub-problems first) can reveal key information about improving space and time complexity. For example, in the iterative solution it might become clear that computing the next sub-problem only requires the solutions from the past two sub-problems, so you can use constant memoization space instead of linear.

You should aim to explain an "informal proof" for why an algorithm is correct. You should not rely on a good feeling alone. Go through the logic for why an algorithm works in each significant case.

Breadth-first search enables you to search nodes in an increasing radius around a starting node. This is useful for problems where you need to find a minimum-distance node that satisfies a condition.

For linked list problems, if it seems like there are a few special cases for the first element in the list, consider starting the operation "one reference back". Sometimes this allows you to avoid any initialization or special logic for the first element.

For 2D dynamic programming problems, it is often the case that *the path between memoization cells represents the state*. This instead of just the final memoization cell position representing the state. Oftentimes two different states can lead to the same memoization cell because they took different paths through the 2D memoization structure to get there. [This LeetCode problem](https://leetcode.com/problems/interleaving-string/) provides a concrete example. So does [this one](https://leetcode.com/problems/edit-distance/description/).
