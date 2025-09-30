📘 README: User Management API
🛠 Overview
This project is a simple Express.js router module that provides a RESTful API for managing user data. It supports basic CRUD operations — Create, Read, Update, and Delete — using an in-memory array.
🚀 Features
- GET / → Retrieve all users
- GET /:email → Retrieve a user by email
- POST / → Add a new user via query parameters
- PUT /:email → Update user details by email
- DELETE /:email → Delete a user by email
 Installation
npm install express

📂 File Structure
CRUD_NODEJS_EXPRESS-main/
├── routes/
│   └── users.js          # Contains all user-related API routes (GET, POST, PUT, DELETE)
├── index.js              # Entry point of your Express server
├── package.json          # Project metadata and dependencies
├── package-lock.json     # Exact version lock for installed packages
└── README.md             # Documentation for your project



🔄 API Endpoints
1. GET /
Returns all users.
Example Response:
[
  {
    "firstName": "John",
    "lastName": "wick",
    "email": "johnwick@gamil.com",
    "age": 22
  }
]
<img width="816" height="424" alt="get" src="https://github.com/user-attachments/assets/ae2d2261-66c5-4c88-83fa-da4b7db0f6ef" />



2. GET /:email
Returns user(s) matching the given email.
Example:
GET /johnwick@gamil.com

<img width="799" height="593" alt="getMail" src="https://github.com/user-attachments/assets/33a35b48-99e3-45fe-be7d-dc207faa7dca" />

3. POST /
Adds a new user using query parameters.
Example:
POST /?firstName=Jane&lastName=Doe&email=jane@example.com&age=25
<img width="762" height="565" alt="post" src="https://github.com/user-attachments/assets/fb9039f4-3642-45a6-8103-53779d59cd5c" />


6. PUT /:email
Updates user details by email using query parameters.
Example:
PUT /johnwick@gamil.com?firstName=Johnny&age=30
<img width="792" height="468" alt="put" src="https://github.com/user-attachments/assets/044403df-67c7-4045-ae94-061e51e0256c" />


8. DELETE /:email
Deletes a user by email.
Example:
DELETE /johnwick@gamil.com
<img width="789" height="497" alt="delete" src="https://github.com/user-attachments/assets/c9ab812b-faae-41c8-83db-d891082be5f0" />


⚠️ Notes
- Data is stored in-memory; restarting the server will reset the user list.
- Query parameters are used for POST and PUT — consider switching to req.body for production use.

📤 Export
This router is exported using:
module.exports = router;


You can import and use it in your main server file like:
const userRouter = require('./src/component/userRouter');
app.use('/users', userRouter);



Let me know if you want to add Swagger documentation, switch to req.body, or connect this to a database like MongoDB — we can level it up together!
