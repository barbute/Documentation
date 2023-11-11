[*< back*](GITHUB_DOCS.md)

# 📛 Naming

Disappointingly, many team members struggle with naming things correctly. Whether it be a commit title, repository, or a superstructure's branch, it is simply inevitable that a team member will misname something, and cause a great deal of confusion in the near future for maintainers.

As such, all GitHub naming conventions are standards when working in the organization.

Here is an index for this article:

- [Repository](GITHUB_NAMING.md#repository)
- [Branch](GITHUB_NAMING.md#branch)
- [Commit](GITHUB_NAMING.md#commit)

## Repository

When creating a repository in the organization, it should follow the naming scheme:

**projectType**-**codeType**-**projectName**

> NOTE: The name follows [Camel Case](https://en.wikipedia.org/wiki/Camel_case).

A name will be composed of the three elements above that will describe what the code in that repository is and does. Here is what each element is:

- **projectType:** A projectType will describe the category the project falls under:

  - **robot:** This code is used for a season’s robot. It will contain all the necessary files, subsystems, commands, and libraries that are needed to make the specified robot function as intended.
  - **system:** This code is for a single concept or “structure” of the robot such as a shooter or a single-jointed arm. This code is typically developed during the off-season so it can easily be used during the build-season.
  - **program:** This code is specific for non-robot systems, such as Talon Logger (A program to log a team member’s hours worked) or the team’s scouting application.
  - **utility:** This code acts as a place for code that can be reused, it is essentially a library. Note that a system is different from a utility as a system is used to develop a structure’s code, while a utility has code that is known to work and make the production of code easier.

- **codeType:** The codeType describes what version the code is:

  - **main:** This is the main write of the code. This version is the most common and typically the only version of the code. A main codeType is the primary version of the code that the team will develop and work on until a project is complete.

  - **rewrite:** A rewrite or refactored version of the code is, as the name implies, redone. Sometimes, the main version of the code was *extremely* poorly organized to the point where it is easier for developers to create a new version rather than to stick with the main. 

  - >  NOTE: Use this sparingly though; this codeType is to be phased out soon as new repositories will require extensive planning before work is to be done.

  - **yourName:** Code with this version means that it is “your take” on the program. This code is typically forked from whatever the main version was and now you are creating your own version of the code, perhaps for testing purposes or because you are bored. However, this should not be done often and testing should be conducted on a production branch on the main code. 

    - Despite this, PLEASE do not keep code on private repositories that is being developed for the team. This makes things incredibly difficult to locate (sometimes impossible) and only adds to the chaos and clutter of managing a development team.

- **projectName**: As the name implies. 

Here is an example of a good name:

![Example](/GitHubDocs/Images/GitHubNamingRepositoryGoodExample.png)

From this we are able to tell that this repository the for a robot, it is the main iteration of the code for that robot, and it is the code for Armstrong, which is 9105's 2023 robot. While this is a basic example, and it may seem like one could simply get away with "Armstrong 2023" note that there are multiple other projects and there may be other rewrites of the code. Things could get cluttered, and this scheme makes it much easier to locate and discern repository from repository.

## Branch

This is a crucial aspect, and one that is often misdone. Naming a branch in a repository is critical to maintaining project organization. The team has often faced the momentous issue of having five separate branches with the phrase "Rewrite" in their titles.

> NOTE: While this segment does not discuss how a project will be laid out, it does intertwine with it. As such it is recommended that you read this section on organizing a programming project.

Here are the team's Git Branch conventions:

- **naming:** In a typical robot development project, there will be a branch for each **subsystem**, a **production** branch, and a **main** branch.
  - **Main:** The main branch of code is where all of the currently working code for the robot is. Changes should not be committed to main unless they have been thoroughly tested and given approval by a team-lead. Note that main may also be called master.
  - **Production:** The “prod” branch of code is where most of the code developed on different branches is merged and undergoes rigorous testing. Code features developed on separate branches should not be merged onto prod until a pull request has been submitted and approved by a team-lead.
  - **Subsystems/features:** These branches are where the bulk of the code is developed and checked extensively before anything is merged together. These branches will also usually only have one programmer developing them, which ensures there are no merge conflicts when bringing code together in prod.

When developing a single subsystem or piece of reusable code, it is still advised to follow a naming scheme similar to this.

## Commit

Naming a commit is fairly straightforward. Simply state what feature you added or what you changed all in a single line. This rule alone should be enough to tell you when you need to commit code. It is il-advised to do a multi-feature commit, but it is acceptable if you add a description to your commit message (via [GitHub Desktop](https://desktop.github.com/)).

Here is an example of a developer about to push some code to a branch:

![Example](/GitHubDocs/Images/GitHubNamingCommitGoodExample.png)

As seen here, our developer forgot to commit the `arm feedforward` and the `drive PID` features separately. To make up for it, the commit title is concise and a description has been added further explaining what was done in the commit.
