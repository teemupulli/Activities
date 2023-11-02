# Pets API

In this activity, we will accomplish the following tasks:

**Basic Server**

Create an Express API server that listens on port 3001 and implements five endpoints:
   - `POST /pets` to add a new pet.
   - `GET /pets` to retrieve the list of pets.
   - `GET /pets/:id` to retrieve a single pet by ID.
   - `PUT /pets/:id` to update a single pet by ID.
   - `DELETE /pets/:id` to delete a single pet by ID.

When a user adds a new pet, they will provide the following information in JSON format:

   ```json
   {
     "name": "Buddy",
     "species": "Dog",
     "age": 1,
     "color": "Brown",
     "weight": 3
   }
   ```

`Unique IDs should be automatically generated` and assigned to each pet when they are saved in the array of pets.

**Middleware**

Implement a logging middleware to record the time of each request.

**Test Endpoints with Postman**:

1. **Open Postman**: Launch the Postman application on your computer.

2. **Create a New Collection**:
   - In the left sidebar of Postman, click on "Collections."
   - Click the "New Collection" button and give your collection a name, e.g., "My Express API Testing."

3. **Create a Request for `GET /pets`**:
   - Within your new collection, click "Add Request."
   - Name your request, for example, "GET All Pets."
   - Choose the HTTP method as "GET."
   - In the request URL, enter the URL of your API's "GET /pets" endpoint, e.g., `http://localhost:3001/pets`.
   - Click the "Send" button.

4. **Create a Request for `POST /pets`**:
   - Add another request to your collection and name it "Add a New Pet."
   - Choose the HTTP method as "POST."
   - In the request URL, enter the URL of your API's "POST /pets" endpoint (`http://localhost:3001/pets`).
   - In the request body (under the "Body" tab), provide the data for creating a new pet in JSON format e.g. 
      
    ```json
    {
    "name": "Fluffy",
    "species": "Cat",
    "age": 2,
    "color": "White",
    "weight": 2
    }
    ```
   - Click the "Send" button to send the POST request.

5. **Create a Request for `GET /pets/:id`**:
   - Add a request and name it "Get Pet by ID."
   - Choose the HTTP method as "GET."
   - In the request URL, replace `:id` with an actual pet ID, e.g., `http://localhost:3001/pets/1` to get a specific pet by ID.
   - Click the "Send" button.

6. **Create a Request for `PUT /pets/:id`**:
   - Add a request named "Update Pet by ID."
   - Choose the HTTP method as "PUT."
   - In the request URL, replace `:id` with an actual pet ID, e.g., `http://localhost:3001/pets/1`.
   - In the request body (under the "Body" tab), provide the data for updating an existing pet in JSON format:
  
    ```json
    {
    "name": "Max",
    "species": "Dog",
    "age": 4,
    "color": "Black",
    "weight": 12
    }
    ```

   - Click the "Send" button.

7. **Create a Request for `DELETE /pets/:id`**:
   - Add a request and name it "Delete Pet by ID."
   - Choose the HTTP method as "DELETE."
   - In the request URL, replace `:id` with an actual pet ID, e.g., `http://localhost:3001/pets/1` to delete a specific pet by ID.
   - Click the "Send" button.



