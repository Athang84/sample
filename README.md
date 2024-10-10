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
### 2. POST /students
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

