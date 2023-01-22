# Internship Guide

*This is a personal and opinionated guide of the lessons I've learned over the course of 7 software engineering internships at companies like Google, Two Sigma, and Semiotic Labs. Feel free to use this guide if it is helpful to you.*

## 1. Before the internship

**Ask your team / intern manager what you can learn or prepare ahead of time.**

* What tech stack does the team use? What programming languages?
* This is how you can really get an edge and focus on the important stuff once you start.

**Outline what you want to learn during your internship. These are learning goals that you should keep in your mind throughout the internship.**

* New to software engineering? Aim to learn the fundamentals of writing clean, readable, and maintainable code.
* New to working within a team?
* New to working within a large, existing codebase?
* New to this particular domain / tech stack?

Take some time to get comfortable with Git (assuming that's the version control your company is using).

* Learning Git upfront will save you a lot of headaches and lost work. I have (multiple times) lost work or otherwise wasted time from having an incomplete understanding of Git.
* Learn the [Git feature branch workflow](https://docs.github.com/en/get-started/quickstart/github-flow#following-github-flow): create a branch, make some commits, and put out a PR.
* Use `git log` to visualize your branches as you work.
* This [git visualization & sandbox](https://learngitbranching.js.org/?NODEMO) is an easy way to gain an intuition for what different commands do in git.

## 2. During the internship

### Soft-skills

**There is a balance to be made between trying to figure something out on your own and getting help from your team.**

* Regardless of what you're getting help on, you should make sure to demonstrate that you've put in an effort to try to figure it out yourself before going to anyone for help. You can say something like: "Hey, I'm having problem X and have tried Y and Z but I'm still stuck. Do you know how I might be able to fix this?".
* Remember that everyone asks for help, all the time. Part of being an engineer is working on systems so complicated that no one single person understands the whole thing. That's what teammates are for.
* If you know that something will take you a day to figure out on your own but 20 minutes if you ask a teammate, ask the teammate.

**Talk to people outside of your team**. Set up informal meetings with people working on things that interest you. It is easy to get too comfortable within your own team and forget to talk to people from across the company (including non-engineers!). As an intern, you're in a privileged position to evaluate the company and all of its various teams before having to commit to anything.

* This is uncomfortable, but really important.

At your first opportunity, tell your manager about your learning goals for the internship. This will help them to give you specific feedback throughout the internship.

Make it explicitly clear to your manager that you want any and all feedback, and that they should not hold back at all. This is a great way to break the ice on receiving feedback, and to demonstrate to your manager that you're here to learn.

When having meetings with your manager, prepare ahead of time with *specific* questions to get feedback. It's hard to give feedback, so make it easier for your manager by prompting them with specific areas of concern.

* These questions should often relate back to your learning goals. For example: "How is my code quality? How could things be more readable?" or "How is my use / understanding of technology X?" or "What would you have designed differently in this PR?"

Prepare for every meeting beforehand. It is often way easier to have a structured, informed conversation when you've prepared.

* Any relevant information, maybe an outline of the points you want to bring up
* Any questions you have for the others in the meeting

Don't get too obsessed with your project. Leave time for other things like meeting people, going to intern events, or learning things outside of your project.

* Your intern project is designed to leave some room for other activities. As long as you put good work in on most days, you should have no trouble meeting expectations.

### Engineering

**Make an effort to put out small, self-contained PRs.**

* In my experience, reviewers put in the same amount of effort to review a PR regardless of its size. So by putting out large PRs, you're getting less scrutiny and useful feedback on your changes. Additionally, it's generally seen as "not nice" to put a huge scrawling PR on someone's plate.
* Making small, self-contained PRs requires planning before you start coding: think about the major changes you need to make, which of these changes are somewhat self-contained, and in what order the changes must appear.
* If things don't go as planned, you can always go back and split things up into separate branches after-the-fact.

**Write detailed PR descriptions.**

* Create a bulleted list highlighting the major changes you've made in your PR.
* If relevant, include a section titled `Testing` that explains how you've tested your changes. Do the existing automated tests pass? Did you perform some manual tests? This gives your reviewer more confidence that your changes don't break things.
* You should expect that any question you had during development a reviewer will also have. So in the PR description, preemptively provide the answers to your questions.

**Design should be a deliberate step in your development process.**

* Maintain a document (design doc) where you answer questions like:
  * What is the problem I'm trying to solve? What do my customers (users, other developers) want?
  * What is *not* the problem I'm trying to solve? This is to avoid ["scope-creep"](https://en.wikipedia.org/wiki/Scope_creep).
  * What are the different approaches to this problem? What are the trade-offs to each approach? Why am I choosing my particular approach?
  * What does a minimum-viable-product look like? What are extra features that can be added on later?
  * What does the timeline for this project look like? During each week, what will I work on and how long do I expect it to take?
  * What are the maintenance requirements for my project? What does my team need to know to maintain my project once I'm gone?
* You should only start real implementation once you've ironed-out your design. Implementation is its own beast. You don't want to have to think about both at the same time, and you don't want to have to backtrack after spending time writing and getting code reviewed.

"Premature optimization is the root of all evil"

* Constantly ask yourself "could this be simpler?" "how am I over-complicating things?"
* In my first real software internship, I felt like I needed to impress my managers by writing complex and performant code. However the opposite was more true. Engineers tend to prioritize simplicity over all else because: it makes things easier to read and maintain, it requires the least engineering effort.
* One surprising fact I learned about real-world engineering is that "software engineering hours" have a real (often very high) cost, and if that cost is more than the extra CPU cycles you're burning from inefficient code, then the priority will be placed on simplicity.

