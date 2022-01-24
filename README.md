# To-Do List Challenge

The **To-Do List Challenge** is to build a web application that allows users to maintain a list of tasks. [Google Keep](https://keep.google.com/) is one example of a To-Do List that you can use as a reference while completing this challenge. 

## Outline

This challenge is presented as a series of milestones. Each milestone adds more functionality and increased level of complexity. 

* **Milestone 1** - Front-end with a mock API.
* **Milestone 2** - Back-end with a datastore to replace the mock API.
* **Milestone 3** - Security to support user accounts.
* **Milestone 4** - Infrastructure to deploy to a public cloud.

## Deliverables

First start by forking this repository, it will be your primary deliverable. As you develop please push commits as frequently as you like but importantly as you complete each milestone please mark it with a git [tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging) so it can be reviewed later. 

**Important:** Please replace this README with your own that describes how-to to do the following:

* Setup your computer with the software and tools required.
* Build and run the application locally.
* Deploy it to a cloud if you've done that as well.

## Milestone 1 (Front-end with Mock API)

Your goal is to develop the front-end of the application. It should connect to a mock API providing you the basic CRUD functionality for tasks. There should be no concept of a security layer or user accounts. Every visitor of the site should be interacting with the same mock data. 

### Functional Requirements

* List Tasks
  * The home page should display a list of Tasks (faciliated by the Mock API).
  * Tasks should be ordered by their timestamp.
  * From here you could create, update or delete Tasks.
* Create / Update Tasks 
  * A Task should have at least these attributes: 
    * `id`: unique number
    * `description`: text for the task
    * `completed`: an indicator if the task is done
    * `timestamp`: created and last updated timestamp
* Delete
  * Tasks can be deleted

### Non-functional Requirements
* Use [mockapi.io](https://mockapi.io/) to create a mock `/tasks` endpoint to facilitate CRUD operations.
* It shall be client-side only, no server-side code or datastore (other than the mock).
* It does not need to be [cross browser compatible](https://medium.com/@sarahelson81/what-is-cross-browser-compatibility-and-why-we-need-it-b41423c3501a).
* It does not need to be [responsive](https://medium.com/swlh/everything-you-need-to-know-about-responsive-web-design-54c2059a7e99).
* Updated README

## Milestone 2 (Back-end with a Datastore)

Your goal is to replace the Mock API with your own back-end and persistent datastore. There should be no noticable changes to the front-end UI/UX, the only difference should be that you're consuming a different API end-point.

### Functional Requirements

* Implement your own API to support CRUD operations for Tasks.
* It should be possible to interact with this API outside of the front-end.

### Non-Functional Requirements

* It should have a back-end that receives and processes requests.
* It should have persistent storage in some form - RBMS, NoSQL, etc.
* Updated README

## Milestone 3 (User Accounts)

Your goal is to introduce a Security layer with User Accounts so each User has their own private Task list. You will need to implement User creation, login and logout flows. You will need to enhance the back-end API and protect that as well.

You may leverage third-party identity providers or social logins like Okta, Firebase, OneLogin, etc. 

Please make sure to update the README detailing how a developer should setup the identity provider and this codebase to run it locally. 

### Functional Requirements
 
* User Creation
  * A User should have at least these attributes: 
    * `username`: unique text
    * `password`: text
  * A User's username should be unique, no duplicates are allowed.
  * There are no complexity requirements for the username or password.
* User Login / Logout
  * Only authenticated Users should be allowed access to the Task list. 
  * Unauthenticated Users should be presented with a login page and the option to create an account.
* API Protection
  * Just as you will secure the front-end with protected routes, the API should also be protected.
  * A User should only be allowed to access to their data. They should only see Tasks that they own. 

### Non-Functional Requirements

* Users should only be allowed access to the data that they created.
* User passwords should be handled securely.
* Updated README

## Milestone 4 (Cloud Deployment)

Your goal is to build the infrastructure and code to deploy this application to a public cloud. You do not need to connect it to any particular domain. The purpose is to demonstrate accessbility over the public internet so an auto-generated domain based on the technology of choice is sufficent. 

Along with the infrastructure you will be required to provide a diagram that illustrates layout of the environment and how code is deployed to it. It must describe the Topology of the front-end, back-end and data store. 

Please make sure to update the README detailing how a developer can successfully deploy it. 

### Functional Requirements

* Infrastructure as code that provide a public facing environment with this application deployed.

### Non-Functional Requirements

* Updated README