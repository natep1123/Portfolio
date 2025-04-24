# [Pet-Rescue-API](https://github.com/natep1123/Pet-Rescue-API)

_A RESTful API platform to mimic adopting a dog online with user authentication built with Node/Express._

## **Project Structure**

The folder structure adheres to best practices for a well-organized backend service:

- `controllers`: Handles incoming requests and sends responses, encapsulating the core logic.
- `models`: Defines data schemas and manages database interactions.
- `routes`: Configures API endpoints, routing requests to the appropriate controllers.
- `middlewares`: Contains custom middleware, including authentication and request validation.
- `.env`: Stores environment variables like database credentials and JWT secrets.
- `app.js`: The main entry point, setting up the Express app and integrating components.
- `db.js`: Establishes and manages the database connection.
- `package.json`: Lists dependencies and scripts required to run the project.

## Graded by Hatchways Code Reviewer

### _Score: 96/100_

### Comments:

- The code is well-structured, with clear separation between routes, middleware, and database connections. This makes it easy to read and maintain.
- The use of pagination in the listAdoptableDogs, listRegisteredDogs, and listAdoptedDogs endpoints is a great feature for handling large datasets, improving the user experience by displaying data in chunks rather than overwhelming users with long lists. The ability to filter by status adds additional flexibility.
- The relationship between the Dog model and the User model via ownerId and adoptedBy is well-implemented. This ensures that the dogs are properly linked to the users, allowing for meaningful queries (e.g., listing dogs by a specific user or adopted dogs).
- There's no validation for the username and password fields (e.g., checking for minimum length, strength of password, or valid characters). It would be beneficial to add validation middleware to ensure that the data meets the expected criteria before it’s processed. For example, checking that the password is sufficiently strong (including special characters, numbers, etc.) and the username follows a certain pattern.
- When registering a new dog, there’s no check to see if a dog with the same name and ownerId already exists. This could potentially lead to the creation of duplicate dog entries for the same owner. Consider adding validation or a uniqueness check before creating a new dog.
