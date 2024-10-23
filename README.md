# Recruitment Test - Web Dev / DevOps

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=whitewhite)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-330F63?style=for-the-badge&logo=gitlab&logoColor=white)

## Subject

The goal of this test is to evaluate your skills on creating an Angular / Node.js web app and setting up a deployment with Docker and GiLab. You'll be judged on your code, your logic of implementation and how you structure the project.

Once finished, send us the URL of the git repository or optionally as an archive.
If you choose to send an archive, remember to delete the `node_modules` before compressing.
Finally, set the times it takes you to finish this test below &#8595;.

Estimated time: ~1h30min\
Time to complete:

> A minimum of UI/UX design effort will be appreciated, but don't spend too much time on it.
> You're allowed to use external libraries like [Angular Material](https://v16.material.angular.io/) if you're familiar with them.

## Prerequisites

Here's the list of framework and packages required before to start the test:

| App                               | Version |
|-----------------------------------|---------|
| [Git](https://git-scm.com/)       |         |
| [Node.js](https://nodejs.org/fr)  | ≥ 18.13 |
| [Docker](https://www.docker.com/) | ≥ 20    |

## Installation

Install dependencies of each project with the following command:

```bash
npm i
```

If the project isn't already in a git repository, you must init one from GitLab, GitHub or using:

```bash
git init
```

## Description

The test is composed in three main parts:

1. Create a simple web app.
2. Create docker images and containers.
3. Create a GitLab pipeline.

### Web App

You're going to create a server and a client app to retrieve and display fake users.

At your disposal, you have :

- A template of an Angular project: `client/`
- A template of a Node.js / Express project: `server/`
- A faked database (see `server/database.js`) already containing data.

You'll improve each of these projects according to the requirements listed below &#8595;.

#### Requirements

**Server**

- [ ] Implement a route to retrieve a list of users.

**Client**

- [ ] Create a top-navbar allowing to navigate between two pages: home and user.
- [ ] The home page should be displayed by default.
- [ ] The home page should display a welcome message.
- [ ] The user page should display a list of users retrieved by calling the server.
  When a row is clicked, all the user information must be displayed below the list.
- [ ] The user list and the user information must be in separate components.

### Docker

Once your app is ready, create a `docker-compose.yml` to build and run the project (client/server).
Please add the execution commands below.

### GitLab CI

Finally, create a `.gitlab-ci.yml` to configure a gitlab pipeline.
The pipeline should at least contain the following jobs :

- lint: a job that executes eslint on the whole project.
- prettier: a job that executes prettier on the whole project.

To run and test the pipeline locally, use the following command:

```bash
npm run ci
```

> Be aware, untracked and ignored files will not be synced inside isolated jobs, only tracked files are synced.
> In other words, remember to `git add` or `git push` untracked files before running the pipeline.

## Report an issue?

Please feel free to contact us if you encounter any configuration issue during your test.
