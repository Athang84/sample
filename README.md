# School Database project

## Project Overview
This is a simple backend API to manage school students. It uses **Node.js** with basic crud operations.

## Folder Structure
- **controller** : Contains the logic for handeling API requests and responses.
- **database** : Contains database connection setup.
- **middleware** : Contains Middleware functions used for handeling requests.
- **index.js** : The main entry point for the application.

## API Endpoints

### 1.**GET /users**
  - Description : Fetches all student data.
  - Response :
    ```json
    [
      {
        "id" : 1,
        "name" : "xyz",
        "class" : "10-A",
        "roll_no" : 1,
        "school_id" : 1
      },
      ...
    ]
    ```
### 2.**POST /users**
   - Description: Adds a new student record.
   - Request Body:
     ```json
      [
        {
          "id" : 1,
          "name" : "xyz",
          "class" : "10-A",
          "roll_no" : 1,
          "school_id" : 1
        }
      ]
      ```
   - Response:
     ```json
     {
       "message" : "user added succesfully",
     }
     ```
### 3.**PUT /users/:id**
   - Description: Updates an existing student record based on ID.
   - Request Body: 
     ```json
      [
        {
          "id" : 1,
          "name" : "xyz",
          "class" : "10-A",
          "roll_no" : 1,
          "school_id" : 1
        }
      ]
      ```
  - Response :
    ```json
     {
       "message" : "user data updated succesfully",
     }
     ```      
### 4.**DELETE /students/:id**
   - Description: Deletes a student record based on ID.
   - Response:
     ```json
     {
       "message" : "user data updated succesfully",
     }
     ```       

## Database

- Type: The database used is PostgreSQL.
- Schemas :
  ```pg
    CREATE TABLE School (
    id SERIAL PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    registration_number VARCHAR(100) NOT NULL UNIQUE,
    address VARCHAR(255) NOT NULL
    );
    
    CREATE TABLE Users (
        id SERIAL PRIMARY KEY,
        student_name VARCHAR(255) NOT NULL,
        class VARCHAR(50) NOT NULL,
        roll_no INT NOT NULL,
        school_id INT REFERENCES School(id)
    );
  ```
