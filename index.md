## Table of contents

* [Overview](#overview)
* [Github Organization Link](https://github.com/uh-code-submissions)
* [Deployment](#deployment)
* [User Guide](#user-guide)
* [Developer Guide](#developer-guide)
* [Continuous Integration](#continuous-integration)
* [Development History](#development-history)
* [Community Feedback](#community-feedback)
* [Team Members](#team-members)

## Overview
The Programming and Algorithms (PANDA) SIG of ACM Manoa presents algorithm mock interview problems to its members.  Currently, it does not have an effective method of collecting and storing submissions. Without a unified database of problems and solutions work is often repeated by the club officers and students will have to use difficult methods of submission such as Google Docs. Google Docs is missing key features such as consistent indentation, language-based color (for variables, etc), and the ability to compile and test submissions.  

PANDA has been interested in a program such as this for two semesters now. The requirements have been brainstormed by current and previous PANDA officers and are listed below.

The solution do this problem will be a comprehensive website that can be used to store problems and solutions submitted by students. The website should feature professional-looking themes, run at reasonable speeds, and operate without crashes or failures up to a professional standard.  

## Case Ideas
- There should also be a Problems page with a brief overview of the problem, and a tag for its difficulty.  This should list all published problems and should be sortable and searchable to some extent. For inspiration visit [here](https://leetcode.com/problemset/all/).  

- Admins of the website should be able to add new problems, they should be able to write the description, assign a difficulty tag, assign the number of points awarded for solving the problem, several test cases, and provide solutions in Java and Python. Preferably the problem description can be written in markdown, so the admins can create a detailed description of the problem using markdown features.  

- Users should be able to answer questions (requiring a sign-in). By selecting a problem from the problems page, they should be taken to a page to answer the problem where they can record a solution via a textbox. The text box should include the necessary features to submit Java or Python Code. The solution should note the language the submission was in. For inspiration see [here](https://leetcode.com/problems/symmetric-tree/). If possible, (if this is reasonable for a student to develop), code can be run in the browser and tested against the solutions submitted by the admin for the before-mentioned test cases.  

- Admins should be able to view each problem and see all submitted solutions. Admins should be able to remove any undesired solution from the database from this page.

- Everyone has access to past problems and solutions

## Beyond the Basics
- Textbox/format property (depending on programming langauge)
- Compling code in browser
- Test code against submitted code by the admin

## Deployment
Live deployment for the application can be found [here](http://uhcodesubmissions.club/).

## User Guide
Details on the user interface and screenshots of the project currently is shown in this section.

### Landing Page
The landing page will be the first part of the website that the user or admin will see in the application. On the landing page, people can view what the application is about, and be able to login or signup.

<img class="ui medium left floated image" src="../images/landing.png">

### Login Page
This page is the sign-in/login page for both the users (who solve problems) and the admins (who provide problems). The login page will be for users who already have an account for the application. The user or admin will be asked to input their email address and password.

<img class="ui medium floated image" src="../images/login.png">

### Signup Page
This page is the signup page for both the users (who solve problems) and the admins (who provide problems). The register page is for new users who will be making an account. The register page will be asking basic information such as name, class standing, email, and will be prompted to create a password.

<img class="ui medium left floated image" src="../images/register.png">

### Admin Profile Page
This is the admin profile page. The admin profile page contains a quick basic overview of the admins profile and bio. Other components that we want to implement are a questions activity feed to allow the admin to see when a student has submitted a new solution to their questions, a big green button which directs the admin to the Submit Question page, and a Meme of the Day. The page continues the light theme throughout the website.

<img class="ui medium right floated image" src="../images/admin-homepage.PNG">

### User Profile Page
This is the user profile page. The user profile page contains a quick basic overview of the admins profile and bio. Other components that we want to implement are a rating system, a list of the classes that the user has taken, a ranking system to provide an incentive to complete problems, and 'subcards' of problems that the user has recently encountered. The page continues the light theme throughout the website.

<img class="ui medium left floated image" src="../images/user-homepage.PNG">

### Add New Problem Page
This is the add new problem page. The add new problem page is only for admin to access. Through this page, the admin will be able to add new problems to the problems page. They can input the name, category, and a description of the problem. There is a submit button at the bottom left when they are ready to create it. The page continues the light theme throughout the website.

<img class="ui medium left floated image" src="../images/addnewproblem.PNG">

### Problems Page
In the problems page, there will be cards that display problems that the admin has created. The user will be able to click on one of the problems that they want to solve and be moved to the problems solutions page. In the cards, the user will be able to see the title of the problem, A short description of what the problem will be about, and what category that problem is under. The page continues the light theme throughout the website.

<img class="ui medium right floated image" src="../images/problems.png">

### Edit Problem Page
This is the edit problem page. The edit problem page is only for admin to access. Through this page, the admin will be able to edit problems that have already been created. There is a button on the card the they can click to edit. They will be able to change the title, category, and description of the problem.The page continues the light theme throughout the website.

<img class="ui medium left floated image" src="../images/edit1.PNG">
<img class="ui medium left floated image" src="../images/edit2.PNG">

### Problem Solutions Page
After selecting a problem, the user will be guided to the problem solution page. In the problem solution page, the user will be able to see the problem, type out a solution, and press the submit button. The solution submitted by the user will then go to the PANDA officers for them to review and give feedback to. The background will remain consistent with the application’s overall theme.

<img class="ui medium right floated image" src="../images/problem-solution.png">

## Developer Guide
This section provides information for a developer interested in the process of downloading, installing, running, and modifying the system/application.

### Installation

First, [install Meteor](https://www.meteor.com/install).

Second, go to [UH Code Submissions GitHub Page](https://github.com/uh-code-submissions/uh-code-submissions), and click the "Use this template" button. Complete the dialog box to create a new repository that you own that is initialized with this template's files.

Third, go to your newly created repository, and click the "Clone or download" button to download your new GitHub repo to your local file system. Using [GitHub Desktop](https://desktop.github.com/) is a great choice if you use MacOS or Windows.

Fourth, cd into the app/ directory of your local copy of the repo, and install third party libraries with:

```
$ meteor npm install
```

Lastly, run the system with:

```
$ meteor npm run start
```

If all goes well, the template application will appear at http://localhost:3000. You can login using the credentials in [settings.development.json](https://github.com/uh-code-submissions/uh-code-submissions/blob/master/config/settings.development.json), or else register a new account.

#### Application Design

This application is based upon [meteor-application-template-react](https://ics-software-engineering.github.io/meteor-application-template-react/) and [meteor-example-form-react](https://ics-software-engineering.github.io/meteor-example-form-react/). Please use the videos and documentation at those sites to better acquaint yourself with the basic application design and form processing in UH Code Submissions.

### Initialization

The config directory is intended to hold settings files. The repository contains one file: [config/settings.development.json].

This file contains default definitions for Profiles, Projects, and Interests and the relationships between them. Consult the walkthrough video for more details.

### Quality Assurance

#### ESLint

You can make sure that the application adheres to our coding standards by provoking ESLint in your app / directory:

```
meteor npm run lint
```

ESLint should show no errors. It is recommended that to do development with ESLint running in the development IDE, such as IntelliJ.

## Continuous Integration

[![ci-meteor-application-template-react](https://github.com/uh-code-submissions/uh-code-submissions/actions/workflows/ci.yml/badge.svg)](https://github.com/uh-code-submissions/uh-code-submissions/actions/workflows/ci.yml)

UH Code Submissions uses [GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions) to automatically run ESLint and TestCafe each time a commit is made to the default branch.  You can see the results of all recent "workflows" at [https://github.com/uh-code-submissions/uh-code-submissions/actions](https://github.com/uh-code-submissions/uh-code-submissions/actions).

The workflow definition file is quite simple and is located at
[.github/workflows/ci.yml](https://github.com/uh-code-submissions/uh-code-submissions/blob/master/.github/workflows/ci.yml).

## Development History
This section explores the devlopment of this application through three milestones.

### [Milestone 1](https://github.com/uh-code-submissions/uh-code-submissions/projects/1) 
- Create Mockup Pages
- Deployment
- Update Project Home Page

### [Milestone 2](https://github.com/uh-code-submissions/uh-code-submissions/projects/2) 
- Implementing Pages
- TestCafe Availability Tests
- GitHub Actions
- Update Project Home Page

### [Milestone 3](https://github.com/uh-code-submissions/uh-code-submissions/projects/3)
- Final Touches
- Update Project Home Page

## Community Feedback
We love to hear from our users, and we focus on building our app around them. One important way we listen to the community is through your submitted feedback. We really value your opinions and suggestions. Please contact one of the UH-Code-Submissions developers at the bottom of this page.

"The overall site is appeasing and straight forward. I can see how useful this sight will prove to be in aiding the PANDA club. I wish there was more incentive to answering problems. I would like to see maybe something like a personal score so I feel like I'm achieving something after spending 10 hours staring at algorithm problems in an attempt to learn something. I really like the intention of this site though!" - MR

"The website looks easy to use and clean. Signing up, I had no trouble and I enjoyed the UI of the profile page. If only I could answer those challenging algorithm problems! I guess I could get some practice in. One suggestion I have is to add more fun features. However, I believe I can really use this site to assist my learning." - JB

## Team Members
* [Chad Oshiro](https://chadoshiro.github.io/), Computer Science
* [Kanai Gooding](https://kanaigooding.github.io/), Mathematics
* [Kiran Datwani](https://kirandatwani.github.io/), Computer Science
* [Tristan DeAguiar](https://tristn.github.io/), Computer Science
