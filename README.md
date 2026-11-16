# 🔐 User Authentication & Data Association App

A full-stack web application built using **Node.js, Express.js, MongoDB, and EJS** that demonstrates user authentication, protected routes, and data association between users and their posts.

Users can register, log in securely, manage their profiles, upload profile pictures, and create and interact with posts. The application uses MongoDB relationships to associate posts with their respective users.

## ✨ Features

### 🔑 User Authentication
- User registration with name, username, email, and password.
- User login with email and password.
- Password hashing using Bcrypt before storing credentials.
- JWT-based authentication using cookies.
- Protected routes accessible only to authenticated users.
- Logout functionality with cookie removal.

### 👤 User Profile Management
- Personalized user profile pages.
- Display user information and associated posts.
- Upload and update profile pictures.
- Protected profile access.

### 📝 Post Management
- Create posts associated with the logged-in user.
- Display posts on the user's profile.
- Edit existing posts.
- Delete posts.
- Like and unlike posts.

### 🔗 Data Association
- Establish relationships between User and Post models using Mongoose references.
- Associate multiple posts with a single user.
- Retrieve related post documents using Mongoose `populate()`.
- Maintain relationships between users and their posts.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime used to execute the backend application. |
| Express.js | Backend framework used for routing, middleware, and handling HTTP requests. |
| MongoDB | NoSQL database used to store user accounts and post information. |
| Mongoose | ODM used to define schemas, models, and relationships between users and posts. |
| EJS | Template engine used to dynamically render HTML pages with server-side data. |
| JavaScript (ES6+) | Handles application logic and backend functionality. |
| HTML5 | Structures the application's web pages and forms. |
| CSS3 | Provides styling and layout for the user interface. |
| JSON Web Token (JWT) | Handles user authentication through signed tokens. |
| Bcrypt | Hashes passwords before storing them in the database and verifies login credentials. |
| Cookie Parser | Reads and manages authentication cookies in incoming requests. |
| Multer | Handles profile picture uploads. |
| Git & GitHub | Used for version control and source code management. |

## 🔄 How It Works

### 1. Registration
- Users submit their registration details.
- The application checks whether the email is already registered.
- Passwords are hashed using Bcrypt.
- User information is stored in MongoDB.
- A JWT is generated and stored in a cookie.

### 2. Login
- Users enter their email and password.
- The application retrieves the corresponding user from MongoDB.
- Bcrypt compares the submitted password with the stored password hash.
- Upon successful authentication, a JWT is generated and stored in a cookie.

### 3. Protected Routes
- Authentication middleware checks for the JWT cookie.
- The token is verified using JWT.
- Authenticated user information is attached to the request.
- Protected pages and operations become accessible.

### 4. Data Association
- Each post references the user who created it.
- User documents maintain references to their associated posts.
- Mongoose `populate()` retrieves the related post documents.
- This allows users to view their own posts on their profile.

## 📂 Project Structure

```text
Data-Association-login-page/
│
├── config/
│   └── multerconfig.js
│
├── models/
│   ├── user.js
│   └── post.js
│
├── public/
│   └── images/
│
├── views/
│   ├── index.ejs
│   ├── login.ejs
│   ├── profile.ejs
│   ├── edit.ejs
│   └── profilepicupload.ejs
│
├── app.js
├── package.json
└── package-lock.json
```

*Note: The structure is representative. Update it if your actual folders or filenames differ.*

## 🚀 Getting Started

Follow these steps to run the project locally.

### Prerequisites

- Node.js
- MongoDB
- npm

### 1. Clone the Repository

```bash
git clone https://github.com/Prajot-Dviwedi/Data-Association-login-page.git
```

### 2. Navigate to the Project Directory

```bash
cd Data-Association-login-page
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure MongoDB

Make sure your MongoDB server is running and configure the MongoDB connection string in your database connection configuration.

### 5. Start the Application

```bash
node app.js
```

### 6. Open in Browser

```text
http://localhost:3000
```

## 📚 Key Concepts Practised

Through this project, I explored and practised:

- Backend development using Node.js and Express.js.
- User authentication and authorization.
- Password hashing and verification using Bcrypt.
- JWT generation and verification.
- Cookie-based authentication.
- Express middleware and protected routes.
- MongoDB database operations using Mongoose.
- One-to-many data relationships.
- Mongoose references and document population.
- CRUD operations.
- File uploads using Multer.
- Server-side rendering using EJS.

## 👨‍💻 Author

**Prajot Dviwedi**

GitHub: [Prajot-Dviwedi](https://github.com/Prajot-Dviwedi)

---

*Built as a backend development project to practise authentication, database relationships, and server-side application development.*
