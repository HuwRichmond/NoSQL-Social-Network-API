# NoSQL-Social-Network-API

The application is an API for a social network web application where users can share their thoughts, react to friends’ thoughts, and create a friend list. The application uses Express.js for routing, a MongoDB database, and the Mongoose ODM.

 ## Table of Contents:  
[1. Description](#Description)  
[2. Acceptance Criteria](#Acceptance-Criteria)  
[3. Walkthrough Videos](#Walkthrough-Videos)  
[4. Installation](#Installation)  
[5. Tests](#Tests)  
[6. License](#License)  
[7. Github Repository](#Github-Repository)   
[8. Contact](#Contact)  

## Description:

This is a data set for a social network using a MongoDB database for the website to handle and process large amounts of unstructured data, Express.js for routing, Mongoose ODM, and the moment package to format time stamps.

## User Story:

```md
AS A social media startup
I WANT an API for my social network that uses a NoSQL database
SO THAT my website can handle large amounts of unstructured data
```

## Acceptance Criteria:

```md
GIVEN a social network API
WHEN I enter the command to invoke the application
THEN my server is started and the Mongoose models are synced to the MongoDB database
WHEN I open API GET routes in Insomnia for users and thoughts
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete users and thoughts in my database
WHEN I test API POST and DELETE routes in Insomnia
THEN I am able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list
```

## Walkthrough Videos:

[Recording of app running incomplete with errors](https://drive.google.com/file/d/1LPQ06XR71hNeZcOIvJTst3E0EurotfvV/view)

## Installation:
  
1. To use the application, clone the repository from Github using the Github clone function
2. Install MongoDB and Insomnia
3. Use the following console command in terminal to install npm packages and run the application
```
    - npm i && npm start
```
4. Use Insomnia to view API routes

## Tests:  

Testing API calls with Insomnia  

---
**`/api/users`**
* `GET` all users
* `POST` a new user:
    ```json

    {
        "username": "SampleUser",
        "email": "sample@email.com"
    }
    ```
---
**`/api/users/:userid`**
* `GET` get a user name by the `_id` 
* `PUT` to update a user name by the `_id`
* `DELETE` to delete a user name by the `_id`
---
**`/api/users/:userId/friends/:friendId`**
* `POST` add a friend to the user's friends list
* `DELETE` remove a friend from the user's friends list
---
**`/api/thoughts`** 
* `GET` to show all previous thoughts
* `POST` to add a new thought
    ```json

    {
    "thoughtText": "Sample text for thought goes here",
    "username": "SampleUser",
    "userId": "Sample12345"
    }
    ```
---
**`/api/thoughts/:thoughtId`**
* `GET` retrieve a thought with it's `_id`
* `PUT` update a thought with it's `_id`
* `DELETE` remove a thought with it's `_id`
---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` create a reaction 
    ```json

    {
    "reactionBody":"Thumbs Up",
    "username":"SampleUser"
    }
    ```
---
**`/api/thoughts/:thoughtId/reactions/:reactionId`**
* `DELETE` remove a reaction with it's `reactionId` 

## License: 
   
   ISC

## Github Repository:
 [github.com/HuwRichmond/NoSQL-Social-Network-API](https://github.com/HuwRichmond/NoSQL-Social-Network-API)

## Contact:

Created by Huw Richmond

[Github.com/HuwRichmond](https://github.com/HuwRichmond)

