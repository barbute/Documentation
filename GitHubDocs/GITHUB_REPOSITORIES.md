[*< back*](GITHUB_DOCS.md)

Here is an index of this article:

- 📚 [Repositories](GITHUB_REPOSITORIES.md)
  - [Organizing a repository](GITHUB_REPOSITORIES.md#Organizing-a-repository)
  - [Similar repositories](GITHUB_REPOSITORIES.md#Similar-repositories)
- 🕊 [Branches](GITHUB_REPOSITORIES.md#Branches)
  - [Project development](GITHUB_REPOSITORIES.md#Project-development)
  - [Rules](GITHUB_REPOSITORIES.md#Rules)
- 🦀 [Commits](GITHUB_REPOSITORIES.md#Commits)
  - [Naming & Desc](GITHUB_REPOSITORIES.md#Naming)

# 📚 Repositories

The team uses repositories to house the projects we develop. Every projects, whether it's a robot, superstructure, utility program, library, and more should have a repository on the organization's page. These repositories should *almost* always be public to maintain transparency. It has become increasingly appearent however, that standards are required to maintain consistency between projects and repositories.

## Organizing a repository

Organizaing a repository ties into organizing a project.

Before even creating a repository, you need to have an in-depth discussion with your team about the project's **priorities**, **goals**, and **timeframe**. Then you need to write this down and begin jotting down every single task that needs to be done for this project to meet its deliverables. This is likely going to take *at least* an hour.

Now it is time to create a repository; give it an approriate name according to the [naming rules](GITHUB_NAMING.md).

> NOTE: This is mostly just for organizing a robot project. If you're only developing a superstructure, add the appropriate subsystem and command folders following these rules

Clone the repository, and create a new robot project inside of it.

Now add the appropriate subsystem, commands, and managers folders, it should look something like this:

![P6](/GitHubDocs/Images/P6.png)

Here is a brief description of each folder:

- **subsystems**: Folder to house the **subsystem** folders, each **subsystem** will require its own folder; Each **subsystem** will have its own
  - *Subsystem* file, which is the actual **subsystem** object that other files will call from
  - *Vars* file, which holds all of the **subsystem** specific variables and constants
  - *IOs* files, which dictate all of the direct motor and sensor inputs and outputs
- **commands**: Folder to house **commands**, you may need to organize the **commands** into their own folders depending on how many **commands** there are
- **managers**: Folder to house any **managers** the robot project may require. Remember that managers are meant to manage how multiple **subsystems** interact with each other

When creating the repository, make sure you create folder and file that you need. Also add all of the necessary libraries, which you can find [here](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html).

The goal of this is to make it easier to avoid complex merge conflicts when working on seperate branches for each subsytem.

## Similar repositories

From time to time, the same superstructures and robots may require different codebases. Whether a project needs to be completely rewritten, or a new programmer is attempting to do their "own take" on a project, a new repository will need to be created.

When doing so, please follow all of the [naming conventions](GITHUB_NAMING.md) to the letter. Also inform the previous project manager that you are doing so, and specify the repository's `README.md` that this is your personnal take on the code, and that other developers should not attempt to commit to it.

# 🕊 Branches

Keeping branches clean and organized are essential to having a successful project. There have been numerous issues that have arrisen due to mismanagement of branches. Following the [naming conventions](GITHUB_NAMING.md) would eliminate many, but not all of them.

## Project development

When developing a robot project, every branch that will ever be needed should be created at the project onset (after creating every folder and file that will be needed on **main** when the repository is initially created). 

Recall from the [naming conventions](GITHUB_NAMING.md) article that **subsystems** should be created on their own branch, and then merged into a "testing" branch called **production** (prod). This is where code will still be in development, but has been approved for testing. A **subsytem** should not be merged into prod without being reviewed by the project manager. 

Once in prod, testing begins. Until this code has passed every single test and goal for this iteration, it should **not** be **merged into main**. Main is purely for working code that is "ready for competition".

## Rules

Here are some general rules for branches:

- Only **one** person should be working on a **subsystem** branch at a time
- Project Managers should create an issue for every problem found on a branch as they see it develop
- Pushing code to **prod** should only be done at the discretion of the Project Manager
  - You should only make the pull requestafter the Project Manager gives you the go-ahead
- After code has been rigorously tested, pushing code from **prod** to **main** is the duty of the Project Manager, not of any of the other developers
- Before code is to be tested, a "Code Review" should be held at home the night before by members of the team to ensure that the code is suitable for testing and that no major logical errors are present
- `README.md` files should be consistently updated with the **TO-DO**s
  - For **prod** this should also include any current issues the team is facing
  - For **main** this should include all of the resolved issues

# 🦀 Commits

Having good commit practice will aid future maintainers and debuggers in tracing code and features as they were added. Good commits will give people a solid trail of when every single feature of the code was added and what it changed.

> NOTE: Good commit conventions need to be followed even if you are doing a "personal rewrite"

## Naming

Good naming and descriptions of commits can be found [here](GITHUB_NAMING.md).
