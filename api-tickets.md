# Guidelines for Creating a Jira Ticket

1. Title
    - Keep it concise and descriptive.
        Example: "Develop POST /user endpoint to create user"
2. Description
    - Provide a detailed explanation of the task.
        - Purpose: Explain why the API is needed.
            - Example: "This API endpoint will allow the frontend to create new users in the system."
        - Scope: Define the scope of the API work
            - Example: "The endpoint should validate inputs and store user data in the database."
        - Background: Add relevant links or context, such as technical documentation or designs. 

3. Acceptance Criteria 
    - Specify clear conditions for task completion        
        Example:
            
            1. API endpoint accepts valid JSON payload.
            
            2. Returns appropriate HTTP status codes (e.g., 201 for success, 400 for bad request).
            
            3. Data is correctly stored in the database.

            4. Unit tests are written and passed.

            5. Endpoint adheres to authentication and authorization rules.      

4. Attachments
    - Upload any supporting documents or images
        Examples:
            
            1. API contract (e.g., OpenAPI/Swagger specification).

            2. ERD diagrams.

            3. Wireframes or UI screenshots for related features.

5. Subtasks (Optional)            
    - Break the task into smaller, manageable parts
        
        Examples:

            1. "Write input validation logic for /user endpoint."

            2. "Integrate endpoint with the database layer."

            3. "Write unit and integration tests."            
6. Priority
    Set an appropriate priority level.
        Examples: Blocker, High, Medium, Low.

7. Assignees
    Assign the task to the responsible developer or team.          

8. Labels and Components
    Add relevant tags for better tracking.
        Examples: API, Backend, User Management

9. Dependencies
    Link related tickets or dependencies.
        Examples:
            
            1. "Depends on user schema implementation in DB."

            2. "Blocked by authentication middleware setup."


### Example Jira Ticket
- Title: Develop POST /user endpoint to create user

- Description: The /user API endpoint is required to allow the frontend application to create new user accounts. It should validate incoming requests, save data into the database, and ensure appropriate responses are sent back to the client. Authentication and authorization rules must also be implemented.

##### Acceptance Criteria:

1. The endpoint accepts the following fields:
    - username (string, required)
    - email (string, required, must be valid email format)
    - password (string, required, minimum 8 characters)

2. Returns:
    - 201 Created on success.
    - 400 Bad Request for validation errors.
    - 401 Unauthorized for unauthenticated requests.

3. Ensures the password is securely hashed before storage.

4. Unit tests cover validation, error handling, and success cases.

5. Integration tests verify database insertion.

##### Attachments: 
    - API Contract Link, Database Schema
##### Priority: 
    - High
##### Labels: 
    - API, Backend, User Management
##### Dependencies: 
    - Blocked by user schema migration (JIRA-1234)
##### Assignee: 
    - Jane Doe