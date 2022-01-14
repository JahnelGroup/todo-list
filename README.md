# To-Do List Challenge

The **To-Do List Challenge** is to build a web application that allows users to maintain a list of tasks. [Google Keep](https://keep.google.com/) is one example of a To-Do List that you can use as a reference while completing this challenge. 

## Challenge Outline

This challenge is presented as a series of milestones. Each milestone adds more functionality and increased level of complexity. Finish as many milestones as you can or what was requested.

* **Milestone 1** - Front-end with a mock API.
* **Milestone 2** - Back-end with a datastore to replace the mock API.
* **Milestone 3** - Security to support user accounts.
* **Milestone 4** - Infrastructure to deploy to a public cloud.
* **Milestone 5** - Advanced features and workflows.

## How-To and Deliverables

First start by forking this repository, it will be your primary deliverable for the challenge. As you complete each milestone please mark them with a git [tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging) so it can be reviewed later. 

**Important:** You will replace this README with your own that describes how-to:

* Setup your computer with the software and tools required
* Build an run the application locally
* Deploy it to a cloud if you've done that as well

## Milestone 1 (Front-end with Mock API)

Your goal is to develop the front-end of the application. It will connect to a mock API providing you the basic CRUD functionality for tasks. There will be no concept of a security layer or real user accounts - every visitor of the site will be interacting with the same mock data. 

### Functional Requirements

* List Tasks
  * The home page should display a list of Tasks sourced from the mock.
  * Tasks should be ordered by their timestamp.
  * From here you could create, update or delete Tasks.
* Create / Update Tasks 
  * A Task should have at least these attributes: id, description, timestamp, and an done indicator.
* Delete
  * Tasks can be deleted

### Non-functional Requirements
* Use [mockapi.io](https://mockapi.io/) to create a mock `/tasks` endpoint to facilitate CRUD operations.
* It shall be client-side only, no server-side code or datastore (other than the mock).
* It does not need to be [cross browser compatible](https://medium.com/@sarahelson81/what-is-cross-browser-compatibility-and-why-we-need-it-b41423c3501a)
* It does not need to be [responsive](https://medium.com/swlh/everything-you-need-to-know-about-responsive-web-design-54c2059a7e99)

## Milestone 2 (Back-end with a Datastore)

Your goal is to replace the Mock API with your own back-end and persistent datastore. There should be no noticable changes to the front-end UI/UX, the only difference should be that you're consuming a different API end-point.

### Functional Requirements

* Implement an API to support CRUD operations for Tasks.
* It should be possible to interact with this API outside of the front-end.

### Non-Functional Requirements

* It must have a back-end that receives and processes requests 
* It must have persistent storage in some form - RBMS, NoSQL, etc.

## Milestone 3 (User Accounts)

Your goal is to introduce a Security layer with User Accounts so each User has their own private Task list. You will need to implement User creation, login and logout flows. You will need to enhance the back-end API and protect that as well.

Do not leverage any third-party identity providers or social logins like Okta, Google, Facebook, etc. Your app must manage the entire flow and the user data.

### Functional Requirements
 
* User Creation
  * A User should have at least these two attributes: username and password.
  * A User's username should be unique, no duplicates are allowed.
  * There are no complexity requirements for the username or password.
  * There should be no confirmation flows (i.e, EMail). 
* User Login / Logout
  * Only authenticated Users should be allowed access to the system. 
  * Unauthenticated Users should be presented with a login page and the option to sign-up.
* API Protection
  * Just as you will secure the front-end with protected routes, the API should also be well protected.
  * A User should only be allowed to access to their data, they should only see Task's that they own. 

### Non-Functional Requirements

* Do not use any third-party authentication providers
* User's should only be allowed access to the data they created.
* User passwords must be hashed when stored in the datastore. 

## Milestone 4 (Cloud Deployment)

Your goal is to build the infrastructure and code to have this application deployed to a public cloud (AWS, GCP, Azure, etc).

TBD...
