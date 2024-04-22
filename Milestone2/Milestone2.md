# **Milestone Project 2**

## Introduction
For my application, I decided I am going to change it to have a inventory system of jerseys. The applicaiton will have where you an Create, Read, Update, and Delete Jerseys. You won't need to sign in, as you will have straight access to the features of being able to see hwo many jerseys you have and insert or remove them.

## Functionality Requirements
![User Stories](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Milestone2/Images/Images/User%20Stories.png)

## ER Diagram
![ER Diagram](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Milestone2/Images/Images/ER%20Diagram.png)

## Sitemap
![Sitemap](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Milestone2/Images/Images/Sitemap.png)

## Wireframes
![Wireframe 1](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Milestone2/Images/Images/Wireframe%20(1).png)

## UML
![UML](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Milestone2/Images/Images/UMLs.png)

## Risks
    - Time Management
    - Understanding of JavaScript Tools
    - Following the requirements from the rubric

# Jersey Management REST API
The Jersey Management API provides a simple and efficient way to manage a sports jersey catalog. Users can interact with the database to retrieve information about jerseys, add new jerseys, update details, or remove jerseys from the catalog. The API adheres to RESTful principles, ensuring a clear and predictable structure for clients.

## Here Are The API Endpoints

### List All Jerseys
Endpoint: /jerseys
Method: GET
Description: Retrieves a list of all jerseys in the database.
Example Request: [GET http://localhost:5000/jerseys](http://localhost:5000/jerseys)
Response: Returns a JSON array of jersey objects.

### Get a Single Jersey by ID
Endpoint: /jerseys/{id}
Method: GET
Description: Retrieves detailed information about a specific jersey identified by its unique ID.
Example Request: [GET http://localhost:5000/jerseys/2](http://localhost:5000/jerseys/2)
Response: Returns a JSON object representing the jersey with the specified ID.

### Create a New Jersey
Endpoint: /jerseys
Method: POST
Description: Adds a new jersey to the catalog. The request body should include jersey details.
Example Request: [POST http://localhost:5000/jerseys](http://localhost:5000/jerseys)
Request Body
```
{
  "name": "Lionel Messi",
  "number": "30",
  "team": "PSG",
  "sport": "Soccer",
  "league": "Ligue 1"
}

```
### Update an Exisitng Jersey
Endpoint: /jerseys/{id}
Method: PUT
Description: Updates the details of an existing jersey. The request body should contain the attributes that need to be updated.
Example Request: [PUT http://localhost:5000/jerseys/1](http://localhost:5000/jerseys/1)
Request Body:
```
{
  "name": "Lionel Messi",
  "number": "10",
  "team": "PSG",
  "sport": "Soccer",
  "league": "Ligue 1"
}

```

### Delete a Jersey
Endpoint: /jerseys/{id}
Method: DELETE
Description: Removes a jersey from the catalog based on its ID.
Example Request: [DELETE http://localhost:5000/jerseys/4](http://localhost:5000/jerseys/4)
Response: Confirmation that the jersey has been deleted.
