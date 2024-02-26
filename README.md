# .NET-React-Ecommerce
Functional structure of e-commerce with React as frontend and .NET as backend

### Adding an Admin User to the Database

1. **Identify the Database Schema**: Before adding a row for the Admin user, it's crucial to understand the database schema. This involves knowing the specific table where user information is stored (e.g., `Users` table) and the required fields for creating a new user (e.g., `username`, `password`, `role`).

2. **Prepare the SQL Query**: With the schema in mind, prepare an SQL INSERT statement to add a new row to the user table. For an Admin user, you might need to set a specific role or permission level that differentiates it from regular users. For example:
   ```sql
   INSERT INTO Users (username, password, role) VALUES ('admin', 'encrypted_password_here', 'admin');
   ```
   Make sure to replace `'encrypted_password_here'` with a securely hashed password.

3. **Execute the Query**: Use the database management tool or the project's database access layer to execute this query. This might involve using a database client directly or running a script within the project that interacts with the database.

### Setting up the .NET Backend

1. **Open the .NET Solution in Visual Studio**: Launch Visual Studio, then open the solution file (`.sln`) for your .NET project. This solution file contains the project configuration and references necessary for building and running your backend.

2. **Build the Solution**: Before running, ensure that the solution builds successfully. Go to the `Build` menu and select `Build Solution`. This process compiles the code and checks for any compilation errors.

3. **Run the Project**: Once the build is successful, you can run the project by clicking on the `Debug` menu and selecting `Start Without Debugging`. This launches the application, starting the backend server on a designated port.

### Setting up the React Frontend

1. **Open the Frontend Project in Visual Studio Code**: Navigate to the folder containing the frontend project and open it in Visual Studio Code. This IDE is optimized for web development and provides an excellent environment for working with React projects.

2. **Install Dependencies**: Open the integrated terminal in Visual Studio Code (using `Ctrl+`` or navigating through the menu `View` -> `Terminal`). In the terminal, run:
   ```bash
   npm install
   ```
   This command installs all the dependencies listed in your project's `package.json` file. It's crucial for ensuring that all the necessary libraries and frameworks are available for your project.

3. **Start the Development Server**: After the installation completes, start the development server by running:
   ```bash
   npm start
   ```
   This command compiles your React application and serves it, usually on `http://localhost:3000`. Your default web browser might automatically open this URL.

### Testing the Integration

After setting up both the backend and frontend:

1. **Verify Backend Connectivity**: Ensure that the frontend application can communicate with the backend server. This might involve checking environment variables or configuration files that specify the backend URL.

2. **Login as Admin**: Test the login functionality by entering the credentials of the Admin user you added to the database. This step is crucial to verify that the integration works and the Admin user has the expected access and permissions.

By following these more technical and detailed instructions, you'll have a thorough setup and testing process for adding an Admin user to your application and ensuring both the backend and frontend components are correctly configured and integrated.
