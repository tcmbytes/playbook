# Continuous Integration (CI)

**Continuous Integration** is the **team practice** where the changes are integrated and tested in short cycles. As a rule of thumb, the cycles are no longer than a couple of hours.

## Motivation

Team programming is not a divide and conquer problem. It is a **divide**, **conquer** and **integrate** problem.

The integration step of a team's work is usually unpredictable, and the longer you wait, the more it costs, and the more unpredictable the cost becomes.

## Mechanics

### Integration

Merge your changes within the whole system.

And merging isn’t a lot of fun. One benefit of integrating every couple of hours is that there aren’t many merges to do. When everyone pushes their changes in short cycles, the number, and the depth, of merges will be pretty small.

You will want to push your changes early, because the first one to push, wins! Everyone else merges.

### Building

Integrate and build a complete project. If the goal is to deploy an API, deploy the API even if it is on the test environments. 

Continuous integration should be complete enough that the eventual first deployment of the system is no big deal.

### Testing

Before you push your integrations, run all the tests locally, in your development environment:

- unit tests
- integration tests 
- functional tests

### Continuous Synchronous

Integrate your work after each pair programming session:

- write your code
- integrate that code in the whole system
- build the system
- run the entire test suit and make sure that nothing broke
- check the integrated code into the source control)

Advantages:

- **It provides a reflection time**. While you wait for the compiler and the tests to run, you have time to review what was implemented and what you might have done better.
- **It creates positive pressure for a short and clear feedback cycle**. You don't have to change context and waste time remembering what we were doing, fixing the problem, and finding back the place in the interrupted task.

### Continuous Asynchronous

Building and testing is done by a build system when it notices the change.

Continuous build systems (like Jenkins or Github Actions) monitor the git repository. Whenever someone does a push to that repository, it kicks off a build of the whole system, and runs all the unit tests and all the integration tests and all the functional tests.

Advantages:

- **It is asynchronous**. When there are problems, you are notified by email, or text message (or even better, a physical alarm).
- **It is a big improvement on daily builds**. When the build breaks, the whole team will be aware of it and must fix it.

### The build must not break

When the build breaks, it is a "Stop everything!" moment:

- the whole team should stop what they are doing and figure out what went wrong
- the build should be passing again before the team return to their work

Props ideas:

- When the build breaks, the team should receive an email with "Bob broke the build!".
- When the build breaks, there should be an alarm sounding and flashlights everywhere.
- If you break the build, you should wear the "I broke the build." t-shirt (the one that never gets washed).
- Have a calendar on the wall with all days in the year and a red dot for each day where the build broke.

## Go-to Resources

- [Extreme Programming Explained: Embrace Change](https://www.goodreads.com/book/show/67833.Extreme_Programming_Explained) by [Kent Beck](https://www.goodreads.com/author/show/25211.Kent_Beck), [Cynthia Andres](https://www.goodreads.com/author/show/38241.Cynthia_Andres)
- [Clean Code: Agile](https://cleancoders.com/series/clean-code/agile), [Episode 50: The Agile Team](https://cleancoders.com/episode/clean-code-episode-50) by [Clean Coders](https://cleancoders.com/) with [Robert "Uncle Bob" Martin](https://www.goodreads.com/author/show/45372.Robert_C_Martin)



