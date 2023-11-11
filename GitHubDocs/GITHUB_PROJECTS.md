[*< back*](GITHUB_DOCS.md)

# 📽 Projects

An excellent way to organize a long-term code project is to use GitHub Projects. GitHub Projects allow teams to visualize due dates, see specific tasks in every category, add issues to specific GitHub repositories and add it as a task, and so much more. Projects are very powerful and easy to setup systems, that can keep small teams in check. The utility is heavily integrated with GitHub, and as such has a lot of convienence features when working with it.

This article is to walk-through a standard Projects setup.

Here is an index of this article:

- [Creating a project](GITHUB_PROJECTS.md#Creating-a-project)
- [Creating a task list](GITHUB_PROJECTS.md#Creating-a-task-list)
- [Creating a timeline](GITHUB_PROJECTS.md#Creating-a-timeline)

## Creating a project

To create a project, start by going to the organization's page and click the "Projects" tab.

![P1](/GitHubDocs/Images/P1.png)

Click the green "New Project" button.

Give the project an appropriate name and start with the `Robot Template`. This template sets up most of the options for you, however you will need to edit some values.

Click the green "Create" button.

## Creating a task list

You will see a view that looks something like this:

![P2](/GitHubDocs/Images/P2.png)

> NOTE: The input fields may be a bit larger on your screen since GitHub does not automatically scale them to fit the screen

Here is a brief description of each field:

- **Title**: A one-line description of what needs to be done

- **Repository**: The repository this task needs to be assigned to

  - If there are none, do not select a repository

- **Assignees**: Who needs to work on the project

  - This field sometimes glitches, you may need to click a person multiple times to add them

- **Status**: Update status based on where you are with a task
- **Start**: The day task is started, the task starts the minute the clock strikes 12
- **Due**: The day the task is meant to end. Note that the task should be largely completed before this day even arrives
-  **Phase**: Groups tasks into stages. Each stage needs to be completed before moving on to the next one
- **Subsystem**: Specifies the subsystem that needs to be worked on

> NOTE: If you add a repository to the task, an issue will automatically be created for the repository

When creating a task, it is important to fill out every field. Now, lets look at the other views.

## Creating a timeline

Click on the "Roadmap" tab, it should be a bit above the input field titles. 

You should see something that looks like this:

![P3](/GitHubDocs/Images/P3.png)

The Roadmap will automatically populate the tasks that are added in Task List. This is also where the **Start** and **Due** fields from the previous board come into play. The task bar in the timeline will automatically adjust based on the given **Start** and **Due** dates. This bar will also include the **Title** of the task and the **Assignnees**.

A Roadmap is a great way to view how much time certain tasks have left. It is also excellent for presenting to mentors as they can visually see what needs to be done and how long it is going to take.

The final view is "Feature Overview", so let's look at that tab; you should see something like this:

![P4](/GitHubDocs/Images/P4.png)

Here you can see what has been completed at a glance, what needs to be reviewed, what features are still being worked on, and what needs to be started. This is where the **Status** field comes into play. When you update **Status** in Task List, it will automatically move the task into the respective area.

This tab is good for project managers to see where their people and their project currently is.

# 🗃 Organization

GitHub Projects are a powerful tool, that this article just barely touches on. However, here are some more rules for organizaing a project:

- **Update** your project manager 📝
  - Despite GitHub Projects being an excellent project organization tool, the mentors still prefer to use Google Spreadsheets for a quick overview of all projects for the Robotics team. As such, please keep that spreadsheet *AND* your GitHub Project up to date
- **Talk** to your team members 🎙
  - Most new people on the team are typically shy and do not know where to begin. Just talk to people, most of the time you'll find that they really do not mind. It is imperative that discussion takes place during projects, do not withhold valuable information because you were too afraid to speak to others
- **Plan**, but not too much 🗺
  - Planning is essential to a project. It is important to consider everything in an initial discussion. Set the goals for what the project should achieve; and build a Roadmap to visualize them and confirm with everyone that this is what you want to do
  - However over planning, such as creating an entire code logic map for every single method is a bit excessive. While you should think through each stage of the code, you don't need a box and an arrow for each method. Something simple, like Armstrong's plan below should be sufficient

![P5](/GitHubDocs/Images/P5.png)
