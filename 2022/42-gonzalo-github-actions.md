# Gonzalo Peña-Castellanos: Automating Workflows with GitHub Actions

## Meetup
Join our Meetup group for upcoming events:
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2022/42-gonzalo-github-actions.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/282772806/
- Video: https://youtu.be/d48WGkePFq0
- GitHub repo:
- Transcriber:  ? [needs a transcriber]

## Resources
- N/A

## Event
Learn about GitHub Actions and how they can accelerate your application development workflows. A workflow is a configurable automated process made up of one or more jobs. We will learn how to configure and use workflows existing current actions and start looking at how an action can be developed from scratch.

## Speaker
I am a Colombian Civil Engineer with an MSc. in Hydroinformatics and an MSc. in Sanitary Engineering that discovered a passion for Software Development and Data Science which led me to collaborate in different open source projects and to eventually join Anaconda, Inc (formerly known as Continuum Analytics) and currently Quansight, Inc as Senior Software Engineer, and Data Scientist (in development). I am an active member of the open source community contributing to different projects and a leader in the Python Colombia Community helping shape and organize communities such as Django Girls Colombia, Python Bucaramanga, Python Colombia and the national and Latin American Python Conferences, PyCon Colombia (2018, 2019, 2020) and SciPy Latam (2019, 2021) respectively. I am currently a core developer with Project Jupyter and Project napari. I am the author of the setup-miniconda Github Action to help automate conda environment and workflows.

- LinkedIn: https://www.linkedin.com/in/goanpeca
- Twitter: https://twitter.com/goanpeca
- GitHub: https://github.com/goanpeca

## Video:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=d48WGkePFq0" target="_blank"><img src="http://img.youtube.com/vi/d48WGkePFq0/0.jpg"
alt="Automating Workflows with GitHub Actions (Gonzalo Peña-Castellanos)" width="50%" /></a>

## Transcript

## Agenda
00:00:00 Reshama introduces Data Umbrella
\
00:04:15 Gonzalo introduces self and projects
\
00:06:36 ---Outline of talk
\
00:07:55 ---PART 1: GitHub, Workflows and GitHub Actions
\
00:11:00 GitHub Development Workflow with "events"
Can trigger "events" or "actions" based on these events: issue opened, PR submitted, comment on issue or PR is merged, closed or updated
\
00:11:55 Continuous integration and continuous development (CI/CD)
\
00:12:05 ("webhook" mentioned), cross-platform testing is done by CI/CD
\
00:13:55 Microsoft and how GitHub Actions started; GH actions is a nice wrapper around Azure pipelines
\
00:15:07 What are GitHub Actions? A platform to "automate development workflows"
\
00:15:22 Mariatta's talk on CI/CD
\
00:16:00 What are developer workflows?  CI/CD does not mean GitHub actions. It is one of *many* workflows you can automate, but it is not the only one.
\
00:16:13 Types of developer workflows
\
00:19:35 ---PART 2: GitHub Action Components
\
00:19:52 Workflows (& YAML files)
\
00:20:28 Events
\
00:20:55 Jobs and Runners
\
00:21:52 Actions
\
00:22:55 ---PART 3: Workflow Syntax
\
00:23:15 Workflow yaml file
\
00:24:00 YAML = YAML Ain't Markup Language
\
00:26:21 Event types: Labels
\
00:26:44 Event types: Pushing / PRs / Branches
\
00:27:19 Event types: Manual dispatch
\
00:29:03 Dependencies between jobs
\
00:29:36 Context: expressions (run jobs conditionally)
\
00:30:53 Context: default environment variables
\
00:31:18 Strategies
\
00:32:57 User-defined environment variables: Global
\
00:33:52 Actions
\
00:35:35 Other topics
\
00:37:06 ---PART 4: GitHub Actions Marketplace
\
00:37:06 Q&A: Can we use on MacOS and Windows?
\
00:38:03 Q&A: Meaning of "17" in cron?
\
00:40:22 Cron job in GitHub actions without need for Heroku?
\
00:41:00 GitHub Workflow Rates (pricing)
\
00:42:26 Q&A: Why is MacOS more expensive than others for GitHub pricing?
\
00:43:39 Q&A: Can jobs be run in parallel?
\
00:47:40 Q&A: Where to go for support for GitHub Actions?
\
00:49:48 ---PART 4: GitHub Actions Marketplace
\
00:55:10 GH Actions: data science, conda
\
00:58:52 stale issue labeler
\
01:01:05 ---PART 5: Creating a Workflow: live examples
\
01:01:28 Migrating from other services (Azure Pipelines, CircleCI, GitLab CI/CD, Jenkins, Travis CI)
\
01:02:03 Starter Workflows!
\
01:02:20 https://github.com/actions/starter-wo...
\
01:02:35 Example: Create a new repository and start! First issue
\
01:08:00 Example: Suggested GH action for the repo: "Simple Workflow"
\
01:13:05 ---PART 6: Creating a Custom GitHub Action
\
01:13:20 Q&A: How to save (download) artifacts?
\
01:17:13 ---PART 6: Creating a Custom GitHub Action
\
01:17:20 3 ways to run GitHub Actions (Composite, JavaScript, Docker Container)
\
01:20:40 Example: Napari
\
01:21:45 napari-svg plugin
\
01:22:45 composite action
\
01:24:40 Other topics for custom actions (Docker, JavaScript / Typescript actions, Outputs on actions)
\
01:25:20 Talley Lambert with napari: https://github.com/tlambert03/napari-...
\
01:34:15 Q&A: What would an advanced GitHub Actions webinar cover?
\
01:34:35 Q&A: Resources for Learning GitHub Actions: https://docs.github.com/en/actions
\
01:36:20 Typescript example
\
01:37:35 JavaScript Action template
\
01:41:30 Closing words
