# ProDev

------------------- Cover image to go here ----------------------------------

## Table of Contents:

[Project Overview](#Project-Overview)<br>
[Stakeholders and their business goals](#Stakeholders-and-their-business-goals)<br>
[UX Design](#UX-Design)<br>
[Component Architecture](#Component-Architecture)<br>
[Development](#Development)<br>
[Deployment](#Deployment)<br>
[Technologies](#Technologies)<br>


# Project Overview

**ProDev** is built from the ground up as an SPA with Vue 3 using Vue-router, Bootstrap 5 for responsiveness, splashes of GSAP in conjunction with Vue transitions and Firebase for the backend. 

A light weight and zippy project management hub for small teams, the main features include:

* **Team Projects view**: A zoomed out view where all members for example the front end team can collaborate on the larger project by breaking sections down for example different parts of each sprint.

* **User Projects view**: Where each team member can create, read, update and delete their own projects.

* **Bugs view**: The bug journal is a place where all team member issues and solutions are listed and shared. Sharing project bugs and solutions can reduce overall project downtime.

* **Live Chat**: Bringing it all together and focusing the conversation is the built in real-time chat feature allowing team members to quickly discuss and respond to different tasks and issues.

Overall the application is designed to be used within a developers daily operations and thus be mostly displayed for long periods of time via a laptop or desktop screen.  For this reason there is a dark mode option within the ui.  

--------------------------------------------------


# Stakeholders and their business goals

- The developer/user:

    - To easily and efficiently collaborate with the team but in an unobtrusive way that allows the developer to focus on their own tasks and get into the zone
    - To interact with a pleasant and streamlined ui that is simple and easy to use and gets out of the developers way  

- The project manager:

    - To easily track the overall project
    - To easily see how each team member is getting on and where they are in their own tasks
    - To have a single focused place to pick up and put down team discussions
    - To be able to quickly respond to issues and leverage the collective knowledge and experience of the team 
    - To create and maintain an effective remote working environment for the team

- The development firm:

    - To destruct larger jobs and delegate blocks of a project to smaller teams that each have their own remote office/environment.  This can make savings from reduced requirement for office space
    - For issues to be quickly identified, shared and solved to limit resource downtime, smooth out the project delivery and increasing the predictability of the project time horizon

- The client for the development firm:

    - Issues to be identified quickly and solutions implemented with a rapid response 
    - New requirements and changes to be acted on and implemented quickly, efficiently and smoothly 

- ProDev developer personal goals for the project:

    - To reinforce understanding and build skills in the following areas:
        - Working with Vue 3 and the composition api
        - Working with the Vue cli
        - Working with Vue router
        - Building single page applications
        - Become more consistent and patterned working with composables/modules, components, views and managing data as it is passed around
        - Get more familiar working with Vue transitions in conjunction with GSAP and JS hooks
        - Develop a better feel for how to work with box shadows to create subtle and modern looking applications
        - Reinforce understanding of js methods where possible  
        - Become more familiar with Bootstrap 5
    
    - To build knowledge and practical skills with Firebase services:
        - How to create, build, deploy and update firebase projects
        - Working with Firestore
        - Working with Storage
        - Working with Firestore Rules
        - Working with Storage Rules
        - Working with Firebase Authentication
        - become more familiar using Vue 3 with Firebase to perform crud operations


--------------------------------------------

# UX Design

**Note**: The current release would be akin to the initial alpha or beta and as such is focused on the main user, the developer and the minimum viable features for their daily workflows. Key features not incorporated in the current deployment that have been pushed back are:

* Admin authentication and UI for project manager roles
* Developer performance reporting and analysis 
* Multiple team authentication - so when a user logs in they only have access to their private team bubble
* In app notifications of unread chat messages

## User Stories

### First time visitor goals:

- To quickly and easily be able absorb content that answers the question: what does this tool do?
- To be able to easily see how to sign in or sign up in order to get access to the application
- The application to be easy and intuitive to navigate and get familiar with
- To get up and running quickly 

### Returning visitor goals

- To be able to quickly and smoothly sign in
- To clearly see when they are logged in and for any user profile settings to be loaded on login
- To easily develop workflow patterns of efficiency and fold them into their daily processes

### Frequent visitor goals

- For ProDev to become an integral cog to the users daily operations
- To at a glance get up to speed with the overall project and any changes
- To efficiently share ideas and support team members
- To quickly receive support and reduce downtime
- To manage tasks and maintain high levels of productivity through staying organised and focused
- To maintain transparency and accountability 


## Features and Functionality

- Landing page:
    
    - Simple top bar including login and signup buttons
    - Content to include images and descriptions of each section of the application
    - Login and sign up buttons also at the bottom of the content (unless fixed top bar)

- Once logged in visitors are routed to the main dashboard with the `My Projects` view active.  From here they can open and close the side chat window and access each view directly via the side panel and also switch from light to dark mode and vice versa

- The main dashboard includes top bar with user name and logout button, side nav with direct links to all views and the toggle button for the side chat and dark mode. The main `router-vew` is nested within this structure as the center piece

At the time of development component libraries that support Vue 3 are few and far between and I could not find suitable navigation options. I was not keen on Bootstraps options so decided to custom build a responsive side-nav and top-bar set-up for the project.  This was done during the early planning to identify the landscape I was working with. I used a combination of Vue tools in conjunction with native JS `window.AddEventListener('resize')` to monitor the viewport width and manage breakpoints. The internal nav-bar and top-bar are built using flexbox and the responsiveness of the whole application as managed by Bootstrap rows and columns.        

**side-note**: There is focus on creating a neutral look to the dashboard with subtle styling with an emphasis on using box shadows to create a layered multi level look and feel. Coupled with this, also a focus on using transitions and transforms to create subtle switches that provide tactile experience (if Cherry mx made application switches).  To add to the layered effect, transitions to be used to give a snappy natural feel as if scrolling through a tangible document. 

The overarching theme dark and light to be clean and subtle with an err towards a dimmed finish. 

On to the views:

- The `My Projects` and `Team Projects` views to use the same list style structure. New projects can be added from here and existing projects can be edited and deleted.  Click into a project to open a view for that specific project. Each project has a title, description, cover image and task list

- The bug journal view to have a blog structure with searchable functionality (either through tags or title keyword search). To be ordered newest at the top.  Within this view a button routing through to the `New Bug` view. Each bug ticket to have:
    
    - Title
    - Description
    - Solution
    - file upload for solution images
    - Open/closed property

- Team Live-Chat 



## Wireframes

------------------------------------------------------------

# Component Architecture


----------------------------------------------------------


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
