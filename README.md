# CareerPath

## TABLE OF CONTENTS 
1. [Overview](##Overview) 
2. [Product Spec](##ProductSpec)
3. [Wireframes](##Wireframes)
4. [Schema](##Schema)
5. [Networking](##Networking)
6. [Milestone1](##Milestone 3)

## Overview

**Description**

A website for anyone and everyone to figure out what they would like to do for the rest of their lives. CareerPath will give detailed steps and recommendations for what kind of job, school, or plan you can have to get where you need to be. 


**App Evaluation**
- **Category:** Educational
- **Story:** Gives a person career path(schools, jobs, certificate programs, etc.) based on their interes.
- **Market:** Men and Women ages 16 - 35
- **Habit:** This website should be used whenever someone feels unsure about their future or needs guidance going into the next stages of their life.
- **Scope:** First we would like to start by asking the user a series of questions. Based on their answers, the system will output a list of jobs based on their interest and personality. The user will then choose which job sounds the most interesting to them. Finally, a list of universities will be displayed, certification programs, and more ways to allow them to get to the career desired.

## Product Spec

1. **User Stories (Required and Optional)**
**Required Must-have Stories**
- User logs in to have the ability to be able to keep track of jobs that were listed to them so they can change what they would like to go into
- users will answer a series of questions (Survey/Questionaire)
- Job Information (description, salary, etc.)
- Settings (accessibility, notifcations, General, etc.)
**Optional Nice-to-have Stories**
- Choose whether they want to look at high learnings or actual careers
- University information (other programs, college history, etc.)
- Connect and talk to certain professionals in the field 

2. **Screens**
- Login
- Register
- Survey/Questionaire
- Job Information
- List of jobs
- List of Universities, certification processes, etc.
- Settings Screen

3. **Navigation**

**Tab Navigation** (Tab to Screen)
- Home
- settings 

Optional:
- Top choices
- Connects/messaging

**Flow Navigation** (Screen to screen)
- Forced Log-in -> account creation if no login is available
- Home Page -> shows job interested, retake the questionaire/survey, connects, etc. 
- Profile page -> Settings page 

## Wireframes

![photos](https://user-images.githubusercontent.com/89495809/155232557-07575334-2ee0-4bb4-a35f-183ff0b6eea2.jpg)

## Digital Wireframes and Mockup

<img width="281" alt="Screen Shot 2022-02-22 at 7 44 08 PM" src="https://user-images.githubusercontent.com/89495809/155244185-fe99dbcb-2912-488c-86f8-996e898c1dbe.png">

## [Bonus] Interactive Prototype

https://user-images.githubusercontent.com/89495809/155262107-c8666fb4-3baf-466b-9973-e432288c82c1.mov

## Schema
**Models**

User
| Property | Type | Description |
| ----------- | ----------- | ----------- |
| username | String | unique id for the user and a way to login |
| firstName | String | user first name |
| lastName | String | user last name |
| email | String | a way for user to get notifications |
| password | String | A way for user to login |

Chats
| Property | Type | Description |
| ----------- | ----------- | ----------- |
| objectId | String | unique id for the user and a way to login |
| author | Pointer to user | user image and username |
| title | String | title of the chat|
| content | String | what the users post |
| createdAt | DateTime | when the chat started |


## Networking

**List Of Network Requests by Screen**

* Survey Screen
   * (Read/GET) - Retrieve all questions needed to be answered
   * (Send/POST) - Send information by answering the questions
   * (update/PUT) - update user answers to survey
* Chats screen
   * (Read/GET) - Existing Chat
   * (Create/POST) - Create a new chat comment
   * (Delete) - Delete existing chat comment
* Feed/Home Screen
   * (Read/GET) - Career Path matching user interest
   * (Read/GET) - Chart of interest
   *  (Read/GET) - Retake survey
* Career Path Screen
   * (Read/GET) - Article post
   * (Read/GET) - Comments for on articles
   * (Read/GET) - chats created by user to talk to advisors
* Settings Screen
   * (Read/GET) Query logged in user object
   * (Update/PUT) Update user profile image

An Api for College information:

* Base Url - http://api.data.gov/ed/collegescorecard/

| HTTP Verb | Endpoint | Description |
| -------------- | --------- | ---- |
| GET  | /v1/schools | returns breaking news headlines for countries, categories, and singular publishers.|
| GET | /v2/top-headlines/sources | returns information (including name, description, and category) about the most notable sources available for obtaining top headlines from.|
| GET | /v2/top-headlines?country=us&category=business | top business headlines |
| GET | /v2/top-headlines?country=us&category=entertainment | top entertainment headlines |
| GET | /v2/top-headlines?country=us&category=business | top business headlines |
| GET | /v2/top-headlines?country=us&category=sports | top sports headlines |
| GET | /v2/top-headlines?country=us&category=science | top science headlines |
| GET | /v2/top-headlines?country=us&category=technology | top technology headlines |

## Milestone 3

https://user-images.githubusercontent.com/89495809/157316828-45befee5-5e03-4e48-b841-640b9db4804e.mov
