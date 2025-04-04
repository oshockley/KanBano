# KanBano
## Description
This Kanban board provides a secure environment for users to manage their work tasks. The application ensures that users are authenticated through a secure login page using JSON Web Tokens (JWT). The system tracks user sessions and ensures the security of work tasks by restricting access based on user authentication.

## Features
- Secure login page with username and password input
- Authentication using JSON Web Tokens (JWT)
- JWT stored securely in the client's local storage for authenticated requests
- Redirect to the Kanban board page after successful login
- Error handling for incorrect login credentials
- Automatic logout and redirection to the login page after session expiry
- Access to the Kanban board is restricted to authenticated users only
- Logout functionality that removes the JWT from local storage

## Technologies Used
- **Frontend**: React, Axios, HTML/CSS
- **Backend**: Node.js, Express
- **Database**: Sequelize, PostgreSQL (or any preferred SQL database)
- **Authentication**: JSON Web Tokens (JWT)
- **Session Management**: JWT stored in local storage

## Getting Started

### Prerequisites
1. **Node.js** and **npm** installed.
2. **PostgreSQL** or another SQL database setup.
3. A **JWT_SECRET** key for secure JWT generation.

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/oshockley/KanBano.git
    cd KanBano
    ```

2. Install backend dependencies:

    ```bash
    cd server
    npm install
    ```

3. Install frontend dependencies:

    ```bash
    cd client
    npm install
    ```

4. Set up environment variables:
    - Create a `.env` file in the `server` folder and add the following:
      ```
      JWT_SECRET=your_random_secret_key
      ```

5. Set up the database:
    - Run migrations and seed data using Sequelize (or your preferred ORM tool).

    ```bash
    cd server
    npx sequelize-cli db:migrate
    npx sequelize-cli db:seed:all
    ```

### Running the Application

1. Run the backend server:

    ```bash
    cd server
    npm start
    ```

2. Run the frontend development server:

    ```bash
    cd client
    npm start
    ```

3. Visit the application at `http://localhost:3000`.
