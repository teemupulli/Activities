# Activity 1


### Setup

- Copy the files in the `src` directory.
- Install the required dependencies using the following command:
```sh
  npm install
```
- Start the server, use the following command:
```
npm run dev
```

### Testing the  API in Postman

**Prerequisites:**
- You should have your Dog API server running on a specific port (e.g., 4000).
- Make sure Postman is installed on your computer.

1. **Launch Postman**: Open the Postman application on your computer.

2. **Create a New Request**: Click on the "New" button in Postman to create a new request.

3. **Name Your Request**: Give your request a name to identify it. For example, you can name it "Dog API - Create a New Dog."

4. **Choose the HTTP Method**: Select "POST" from the HTTP method dropdown. This indicates that you are making a POST request to create a new dog.

5. **Enter the Request URL**: In the URL field, enter the URL of your Dog API endpoint. For the "POST /dogs" endpoint, enter the full URL, including the port number. It might look like `http://localhost:4000/dogs` or any URL where your API is hosted.

6. **Set Request Headers (if necessary)**: If your API expects specific headers, you can set them under the "Headers" tab. For creating a new dog, you may not need any additional headers.

7. **Provide Request Data**: Since you want to create a new dog, switch to the "Body" tab. Here, you can provide the data for the new dog in JSON format. Specifically, for your model where each dog has a name, your JSON data might look like:

   ```json
   {
     "name": "Max"
   }
   ```

8. **Send the Request**: Click the "Send" button to send the POST request to your Dog API.

9. **View the Response**: Postman will display the response from your Dog API. You should receive a response with a status code (e.g., 201 Created) and a representation of the newly created dog, including the `name` you provided.

10. **Verify the Dog was Added**: To ensure the dog was successfully added, you can make a GET request to retrieve all dogs from your API. Use a GET request to the appropriate endpoint, such as `http://localhost:4000/dogs` if that's where your dogs are stored.



