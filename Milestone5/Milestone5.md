# Milestone Project 5: React Front End
**No updates were made to the design report, other than what was requeste for submission***

## Screencast for the Milestone Project
***https://www.loom.com/share/55681236f9364b969bf15e8b8b1cbb3e?sid=9e6e2931-ebcc-4696-afea-1081a623fc76***

## URL to the GIT Repository
***https://github.com/Eli9Saavedra/CST391/tree/main/MilestoneProjects/ReactApp/jersey-inventory-frontend***


## Introduction
For my application, I created a React Frontend for the Jersey Inventory and made a nice easy user interface. Every feature for the CRUD operations worked perfectly and smooth. Hope you enjoy the screencast as this has been my favorite project in this class.

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


# Milestone 3: Rest API using Express Framework
***No updates were made to the design reort***

## REST API Documentation
```
{
	"info": {
		"_postman_id": "73117616-3a2f-4442-8c09-e8131dc133f6",
		"name": "JerseyCollection",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "28918997"
	},
	"item": [
		{
			"name": "Create New Jersey",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n  \"name\": \"Lionel Messi\",\r\n  \"number\": \"10\",\r\n  \"team\": \"Argentina\",\r\n  \"sport\": \"Soccer\",\r\n  \"league\": \"FIFA Nationa Team\"\r\n}\r\n",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/jerseys",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"jerseys"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get All Jersyes",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "http://localhost:5000/jerseys",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"jerseys"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Jersey By ID",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "http://localhost:5000/jerseys/2",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"jerseys",
						"2"
					]
				}
			},
			"response": []
		},
		{
			"name": "Update Jersey",
			"request": {
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n  \"name\": \"Jimmy Butler\",\r\n  \"number\": \"10\",\r\n  \"team\": \"Miami Heat\",\r\n  \"sport\": \"Basketball\",\r\n  \"league\": \"NBA\"\r\n}\r\n",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/jerseys/1",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"jerseys",
						"1"
					]
				}
			},
			"response": []
		},
		{
			"name": "http://localhost:5000/jerseys/4",
			"request": {
				"method": "DELETE",
				"header": [],
				"url": {
					"raw": "http://localhost:5000/jerseys/4",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"jerseys",
						"4"
					]
				}
			},
			"response": []
		}
	]
}
```


