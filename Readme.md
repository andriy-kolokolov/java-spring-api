# Java Spring API Project

This is a Java Spring API project that provides various endpoints for user authentication and access control. It includes features for user registration, login, and secured access to specific routes.

## Table of Contents

- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
    - [User Registration](#user-registration)
    - [User Login](#user-login)
    - [Secured Endpoint](#secured-endpoint)
- [Contributing](#contributing)

## Getting Started

### Prerequisites

Before running the project, make sure you have the following installed:

- Java Development Kit (JDK)
- Maven

### Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/java-spring-api.git
```
Navigate to the project directory:
```bash
cd java-spring-api
```

Build the project using Maven:
```bash
mvn package
```
Run the application:
``` bash
java -jar target/java-spring-api.jar
```
### Usage
To use the API, make HTTP requests to the provided endpoints using tools like cURL or Postman.

# API Endpoints

## User Registration
**Description:** Register a new user with the system.<br>
**URL:** ```/auth/signup``` <br>
**Method:** ```POST```
### Request Body:

```json
{
    "username": "example_user",
    "email": "user@example.com",
    "password": "password123"
}
```

#### Response:

``` json
{
    "message": "User registered successfully"
}
```

## User Login
**Description:** Authenticate a user and get an access token.<br>
**URL:** ``` /auth/signin```<br>
**Method:** ```POST```
### Request Body:
``` json
{
    "username": "example_user",
    "password": "password123"
}
```
### Response:
``` json
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "tokenType": "Bearer"
}
``` 

## Secured Endpoint
**Description:** An example of a secured endpoint that requires authentication.
**URL:** ```/secured/user```<br>
**Method:** ```GET```<br>
### Request Headers:

``` makefile
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
``` 
### Response:
```json
{
    "message": "Hello, example_user! This is a secured endpoint."
}
```

## Contributing
Contributions are welcome! If you find any issues or want to add new features, please submit a pull request.