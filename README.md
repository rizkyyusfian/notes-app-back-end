# notes-app-back-end

Simple web service API for learning backend using Hapi.js framework. 
The API provides various endpoints to perform CRUD (Create, Read, Update, Delete) operations on notes. It allows users to add, view, edit, and delete notes. 
This web service is a practice module from Dicoding.
notes data is stored in-memory storage. no database is used in this web service.

## API Structure

1. **Add Note**
   - Endpoint: `POST /notes`
   - Description: Allows users to add a new note with a title and content.
   - Request Body:
     ```
     {
       "title": string,
       "tags": string,
       "body": string,
     }
     ```
   - Response: Returns the newly created note object with a unique ID.

2. **Get All Notes**
   - Endpoint: `GET /notes`
   - Description: Retrieves all the notes available in the app.
   - Response: Returns an array of all notes with their respective titles and contents.

3. **Get Note by ID**
   - Endpoint: `GET /notes/{id}`
   - Description: Retrieves a specific note by its unique ID.
   - Response: Returns the note object with the given ID, including its title and content.

4. **Edit Note**
   - Endpoint: `PUT /notes/{id}`
   - Description: Allows users to update the title and/or content of a note with a specific ID.
   - Request Body:
     ```
     {
       "title": string,
       "tags": string,
       "body": string,
     }
     ```
   - Response: Returns the updated note object.

5. **Delete Note**
   - Endpoint: `DELETE /notes/{id}`
   - Description: Allows users to delete a note with a specific ID.
   - Response: Returns a success message indicating that the note has been deleted.

## Technologies Used

- Hapi.js: The Node.js framework used to build the Restful API.

## Installation

1. Clone this repository.
2. Install dependencies: `npm install`.
3. Start the server: `npm start`.

## Usage

1. Access the API in your browser or API client by visiting `http://localhost:3000`.
2. Use the provided endpoints to add, retrieve, edit, and delete notes as per your requirements.

## Contribution

Contributions are welcome! If you find any issues or have suggestions for improvement, please feel free to submit a pull request and do a fork for any purpose.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use and modify the code as per the terms of the license.
