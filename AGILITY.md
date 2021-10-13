# Agility

The word agile has become synonymous with process, as in, "We're an agile shop. We do Scrum." Scrum, Kanban, and others put structure around our work in order to simplify and standardize project management. They're great. They can work really well. But, process is only one part of agility.

The true core of agility is reliably and quickly delivering value to customers. This requires more than process.

- You need the ability to move nimbly through a codebase, writing well factored, structurally simple code and building a foundation of fast, reliable tests.

- You need dependable, performant tooling, including builds that run in under 10 minutes, and a deploy process that rarely fails and allows for easy rollbacks when necessary.

- And, you need a culture that encourages shared ownership, iteration, and a sense that we are all in it together.

Of course, every team is unique. And as such, every team needs to discover together the practices that work best for them. But, there are industry-wide best practices which the vast majority of teams should be using. And, there are others practices that have proved quite useful to me during my career.

This document describes the collection of practices that have worked best for me over the years. These are heavily influenced by Kent Beck's Extreme Programming Explained.

## Practices to Improve Code Agility

- **Coding Standards** &mdash; The team should use well-established, industry-backed coding standards to avoid trivial disagreements, and to make the code easier for everyone to understand, including new team members.

- **Code Reviews** &mdash; In order to facilitate quality, improve security, and foster knowledge and skills transfer, all code must be peer reviewed prior to merging it into the main branch.

- **100% Code Coverage** &mdash; Under normal circumstances, all production code should be tested. Prototypes and spikes do not require tests. But, before that code is shipped to production, it must be covered with tests. And, contrary to common wisdom, I have found great value in 100% test coverage. It is not a panacea. Even code with 100% test coverage will contain bugs. But, the freedom to refactor at will without fear is worth it.

- **Testing in Layers** &mdash; Tests should be written at multiple levels of abstraction. Unit tests should describe individual classes and methods. Integration tests should prove that systems interact correctly at their boundaries. And, functional tests should illuminate whether or not the software fulfills it's requirements.

- **Test-First Programming** &mdash; When fixing a bug, engineers should first write a test that reproduces the bug, then fix the test. When adding a feature, engineers should first write a test that documents the missing feature, then write the code that makes the test pass.

- **Incremental Design** &mdash; The software design should be simple and flexible enough so that it can grow with the software, through the practice of refactoring. Metaphors, when used correctly, are a powerful assistant in helping people understand the design.

## Practices to Improve Tooling Agility

- **Feature Branches** &mdash; There should be only one main branch per repository. Development should happen on short-lived feature branches. The shorter the life of a feature branch, the better. Feature branches should not span more than one week.

- **Continuous Integration** &mdash; The code should be built and the tests should be run continuously. The build and tests must both succeed prior to merging code into the main branch.

- **Ten-Minute Build** &mdash; The build (and tests) should run in as little time as possible in order to minimize context switching. At ten minutes, the build is long enough for a coffee break. Any longer than that, and the engineer is likely to move on to another task.

- **Continuous Deployment** &mdash; As software is merged into the main branch, it should be tested one last time, and upon success, deployed to production automatically. More conservative approaches may deploy to staging environments first for another round of testing. But, ultimately, the process should be automatic.

## Practices to Improve Cultural Agility

- **Shared Code Ownership** &mdash; Anyone on the team should be able to improve any part of the code at any time. Knowledge silos are terrible for the team, given that departures are a fact of life.

- **Pair Programming** &mdash; The most effective way to accomplish the goals of shared code ownership is to write code in pairs. Everyone should be so lucky as to find people they pair with effectively.

- **Small Releases** &mdash; Software should be delivered in small increments. The smaller the increment, the lower the risk, the less time it should take, and the faster customers can begin deriving value from the new code, which is the whole point.

- **Whole Team** &mdash; The team is comprised of everyone necessary to the development of the software. At a minimum, this should include a product manager and engineers. Depending on the project, the team may also include designers and/or technical specialists (like a DBA). Bonus points for including an actual customer on the team.

- **Informative Workspace** &mdash; The team's workspace (virtual or IRL) should reflect the work that happens there. For example, monitoring dashboards should be prominently displayed; stories can be tracked via 3x5 cards hung from the wall, or in a shared work item tracking system.

- **Energized Work** &mdash; Work should proceed at a sustainable pace. Team members are encouraged to take enough time away from work so that energized work is possible.

- **Team Continuity** &mdash; The team should be dedicated to a shared purpose. Team members should not have other work commitments beyond the team. And, management should strive to keep the team together, even as the team's purpose changes over time. Camaraderie and trust go a long way toward collaboration and productivity.

- **(Virtually) Sit Together** &mdash; Before COVID-19, I believed that teams functioned better when sitting together in a shared space to better facilitate communication. What I've learned from working remotely for many months is that the team is thriving. But, to keep that up, the team needs to interact as a whole at least daily.

- **Slack** &mdash; There should be slack in the schedule. This allows for team members to sharpen their skills, explore side projects, or even just take time off without worrying that they are putting the project in jeopardy.

## Practices to Improve Procedural Agility

- **Prioritized Backlog** &mdash; The team should maintain a prioritized backlog of work. Items near the top of the backlog are generally more well defined than items further down the list. Items are executed in order from top to bottom.

- **Quarterly Cycle** &mdash; The team should take time once a quarter to map out their product priorities for the next three to six months. These product priorities should include KPIs for each new feature.

- **Weekly Cycle** &mdash; Work should be broken into weekly cycles in a planning meeting at the beginning of the week. This allows the team to determine the amount of work they can complete in a fixed period of time (otherwise known as their velocity), which can be used to predict when they will complete specific elements of their roadmap.

- **Daily Cycle** &mdash; Near the beginning of the team's workday, members of the team should share their status with each other and with stakeholders. Impediments can be raised in this context, but team members should not wait to seek help when stuck.

- **Stories and Epics** &mdash; Product requirements should be expressed in the form of short stories told from the perspective of an end-user or collaborating system. These stories should include the actor, the action, and the motivation for the actor to take the action. Most importantly, each story should specify the criteria under which it will be accepted as complete. Collections of related stories are called epics.

- **Retrospection** &mdash; The team should regularly reflect on what's going well, what isn't, and how to improve. The team should also meet after completing larger projects to reflect on the lessons learned while working on the project.

- **Root Cause Analysis** &mdash; When things go wrong, fix them first, then reflect on what happened. Use the Five Why's technique to dig into the heart of the problem.

## Conclusion

I'm not saying that every team needs to do all of these practices, or even that this is an exhaustive list of best practices. I'm just saying that I've had positive experiences with each of these practices and would argue for their use on my teams. YMMV.

