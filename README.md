[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8160218&assignment_repo_type=AssignmentRepo)
# React Solo Project

[Live Project](https://osrs-events.web.app/)

## Requirements

- `React.js 18`
- `Node.js ^16.10 || 18`. Need to change your version?
  - [Window](https://github.com/coreybutler/nvm-windows)
  - [Mac](https://github.com/tj/n)
- Firebase (optional, but strongly encouraged for your database, auth, hosting, and storage needs).
- Hosting: if not Firebase, it must be an pre-approved PaaS
  - Vercel
  - Heroku
  - Railway

## Getting Started

We are using "yarn" instead of "npm" in this project.

1. Install yarn. `npm install -g yarn`
2. Install all node modules. `yarn install`
3. Boot up the server. `yarn start`

### Hosting (Not necessary in sprint 1)

1. Go to the official Firebase website and set up a project.
2. Enable Firebase Hosting by going into the hosting section under Build dropdown.
3. Inside your repo run the following commands (one at a time):
4. `npm install -g firebase-tools`
5. `firebase login`
6. `firebase init`
7. `yarn build` (*remember to always build before deploying your code to production*).
8. `firebase deploy`
9. If you run into trouble take a look at: https://www.geeksforgeeks.org/how-to-deploy-react-project-on-firebase/

### Firebase (if you need authentication or a database in your project)

1. If you don't need authentication or a db, you can ignore the 'login', 'firebase' and 'authSlice' files and skip this section.
2. Go to the official Firebase website and set up a project.
3. Enable Firebase Firestore if you need a database or Firestore Authentication if you need user authentication.
4. If you need user authentication, make sure to enable google authentication in the settings.
5. If you used `yarn` to install all dependencies, you shouldn't need to install anything else.
6. Change the name of the '.env.local.example' file to '.env.local' and write your api key and other information (can be found in the settings of your project on the firebase website).
7. The 'Login' component is commented out in 'App.js'. If you don't need it, delete it. If you do need it, move it to the page where you need it.
8. You can import the 'Login' component on the page you want the user to log in. At the moment the logic is set up to support authorization with Google. If you want to add others (email, username and password, github) You will have to implement this on your own.
9. Clicking on the "Continue with Google" button should open a pop-up that logs you in. If this doesn't work, check your firebase keys and if you have google authentication enabled. Once you are logged in, it will automatically update the state in the 'authSlice' reducer with your information (display name, email and access token). If you need any of these, you can get them with a useSelector hook in the component where you need them.
10. You can check if the user is signed in by checking the state of the 'authSlice'. If user is false (empty), the user isn't signed in.
11. You are free to style the buttons or the login component as you see fit. You can (probably a good idea) move the log out button somewhere else, depending on your project. as long as you import all the necessary things and don't change the function/logic, it should work.

### Folder Structure And Advice

1. You can adjust the folder structure if you have other preferances.
2. The "redux" folder contains an example reducer (counter). You can delete this.
3. You can use whichever CSS library you wish, or just plain CSS/SASS (preferably modules).
4. You may modify the boilerplate (e.g. delete dummy text in App.js, the counter, the the logo.svg, etc.)
5. V1 of this project is due in 3 weeks. Remeber to KISS (Keep It Simple, Stupid). You need to think of v1 as a conceptual boundary of constraints; anything *outside those boundaries must be saved for a future version*.

<!---
*** WHEN YOU ARE UP AND RUNNING, DELETE EVERYTHING ABOVE ME EXCEPT THE VERY TOP LINE. ***
*** RENAME THE TOP LINE WITH YOUR PROJECT NAME. ***
-->

## Sprint Progress

Go to the [milestones tab](../../milestone/1) to track your progress.

## Project Overview

### Description

#### DELIVERABLE
A hosted web-application (osrs-events) that allows for the following functionality:

##### MAIN SYSTEM
- User authentication
- Ability for users to create groups
- Admin privelages for group creators
- Ability for users to apply to join groups, and for group admins to approve invitations
- Ability for a group admin to invite/challenge another group to an event type (Bingo), as well as accept pending challenges
- Once challenge is accepted, whatever game is being played goes into "pregame" phase

-- Actual events to come in v2


#### MILESTONES (Edited):
* Sprint 1: 10% - App online with user registration/authentication set up
* Sprint 2: 40% -  Communities set up with community applications
* Sprint 3: 100% - MAIN SYSTEM section complete - communities, administrative tools, roles, community applications, event invitations. 



### Mockups
![image2](https://user-images.githubusercontent.com/48227232/181344546-d2285498-8887-404f-8367-a6490795ad85.jpeg)
![image1](https://user-images.githubusercontent.com/48227232/181344536-6144343d-a036-4a29-99c2-3f875ddd4ff7.jpeg)
![image0](https://user-images.githubusercontent.com/48227232/181344507-0bb929b7-02b6-4e85-a5ac-6eb40e010b4e.jpeg)
