# Developers Guide


## GitHub
We use GitHub for collaborating on our new.nox project. This includes sharing of our code and documentation, giving feedback to new code and organizing the whole project. 
To be able to work on this project, you have to sign up to GitHub and join the NoxAG organisation.


### What the fuck is GitHub?
For everyone that hasn't heard of GitHub or doesn't know what exactly is GitHub for, here are a view videos and websites that explain the main concept:

- Introduction Video: [Idea of GitHub](https://www.youtube.com/watch?v=w3jLJU7DT5E)
- Visual Overview Video showing the most important Git commands: [GIT Workflow - Software Development Process](https://www.youtube.com/watch?v=3a2x1iJFJWc)
- Video Playlist with videos for all the important Git commands: [Github and Git Foundations](https://www.youtube.com/playlist?list=PL0lo9MOBetEHhfG9vJzVCTiDYcbhAiEqL)
-An interactive tutorial to learn every important aspect of Git: [The Interativ Guid to GitHub](http://learngitbranching.js.org/)

*The interactive tutorial is **for everyone** and sould at least be completed partially.*

Here a short list of chapters that are essential for understanding and using git:

- Main
  - Einführung
    - Einführung in Git Commits
    - Branches in Git
    - Mergen in git
    - Einführung in Rebase
    
- Remote
  - Push & Pull -- entfernte Repositorys
    - Clone Einführung
    - Clone Einführung
    - Git Fetch
    - Git Pull
    - Teamarbeit simulieren
    - Git Push
    - Abweichende History
    
The other chapters of this tutorial are also quite good, but not necessary for the average use of Git 


### Sign up to GitHub
To sign up to GitHub just follow this [link](https://github.com/) and create an account.
If you want to get the free *Student Developer Pack* which gives acces to a number of otherwise costly developer tools just follow this [link](https://education.github.com/pack) and apply for your *GitHub Student Package*. (You'll need to add your ...@student.dhbw-mannheim.de mailing address to verify that you are actually a student)


### Join the NoxAG Organisation
Organisations in GitHub are used to manage group-owned repositorys and projects. All members of one organisation are part of the team and can be assigned different access rights. 
After you sign up to GitHub you can be invited to the NoxAG Organisation. After you have been invited you can either follow the link that should be in the invitation mail or you can just go to the [NoxAG Github Page](https://github.com/NoxAG) and accept your invite.

### Setting up the GitHub Desktop Application
GitHub provides the *GitHub Desktop* App that helps you use GitHub without the command line.
Here is the [Link](https://help.github.com/desktop/guides/getting-started/installing-github-desktop/) for the installing guide.

### How we use GitHub

#### Structure of our projects
To make sure that we can all work independently on small parts of our project without interfering in each others work, we are going to devide our project in multiple repositorys. To make this work, we will have one "NewNox-Application" repository wich is going to represent the main repository of our project. This repository depends on all the other repositors like "NewNox-Textanalyzer" or "NewNox-GUI" and all the others that we may have. Furthermore we are going to have one "NewNox-Common" repository as dependency to all other repositories that is going to contain all the classes and methods that need to be accessed by every or nearly every repository. In an optimal way this repository is going to be empty and can later be discarded.

#### The Git pull request workflow
The git pull request workflow is one way of collaborating with git.

The workflow is as follows:
1. You want to fix a bug or add a feature to an repository
2. You either already have the repository cloned on your computer or you have to clone it to your computer
3. You create a new branch with a name like "fix/<bugname>" or "feature/<featurename>" (most of the time, the parentbranch should be the master branch)
4. You checkout your new branch
5. You add your code to your branch by committing small chunks of it that each have a detailed and meandingful description of what has been changed
6. You push your commits into the remote repositoy
7. You open a pull request and ask for a code review by Person B
8. Person B reviews your code. This includes
    - requesting improvements
    - requesting clarification
    - requesting discussion (or another review by someone else)
    - and after all issues have been taken care of, the approval of your pull request
9. Merging your branch into the master (or parent) branch


## Ecplise
As IDE I would advise you to use [Eclipse Oxygen](http://www.eclipse.org/downloads/packages/eclipse-ide-java-ee-developers/oxygenr) because it already contains most of the features we need for our development (EGit, Maven, etc.).

### Code Formatting
To make sure we all follow the same code formatting conventions, you should import this [EPF-File](https://github.com/NoxAG/Developer-Guide/blob/master/eclipse-format-settings.epf) into [eclipse](https://help.eclipse.org/neon/index.jsp?topic=%2Forg.eclipse.platform.doc.user%2Ftasks%2Ftimpandexp.htm).

### Github plugin (EGit)
This plugin is already included in *Ecplipse Oxygen*. Unfortunatly importing gradle projects via the EGit plugin seems to be broken in some way. You may try, but for now I recommend you either use Git from the CommandLine or from the Git Desktop Application.

### Sonarqube Plugin
SonarQube is an open source platform for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities. It offers reports on duplicated code, coding standards, unit tests, code coverage, code complexity, comments, bugs, and security vulnerabilities.

To use this plugin, you need to install it via the Ecplise Marketplace. To do that, open Ecplise and go to *Help* -> *Eclipse Marketpalce*.
Than use the searchbar to find "*SonarLint 3.2.0*" and click *install*. As soon as the installation has finished you need to restart eclipse. After that you can use the features of sonarqube by right clicking on you project and choosing *SonarLint* -> *Analyze*

### Gradle
We use Gradle as dependency manager. But because most of the configuration has to be made upfront and only by one person, there is no need to explain the workings of gradle at this point.

## Java
You should also make sure that you have [Java SE Development Kit 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) installed.
