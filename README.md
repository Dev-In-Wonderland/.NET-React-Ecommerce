# .NET-React-Ecommerce
Functional structure of e-commerce with React as frontend and .NET as backend

### Adding an Admin User to the Database

Given the schema details, the SQL query to insert an Admin user into the `Users` table will need to include values for all required fields. Assuming `Fund`, `Type`, `Status`, and `CreatedOn` are mandatory, and considering best practices for password storage (hashing the password before storing it), here's a more detailed approach:

1. **Prepare the SQL Insert Statement**: Based on the schema, prepare a statement that includes all necessary fields. If `Type` is used to differentiate user roles, ensure to set it appropriately for an admin. For the sake of this example, let's assume `Type` = 'Admin', `Status` = 1, and you have a mechanism to hash the password. Here's a hypothetical SQL query:

   ```sql
   INSERT INTO [EMedicine].[dbo].[Users]
       ([FirstName], [LastName], [Password], [Email], [Fund], [Type], [Status], [CreatedOn])
   VALUES
       ('admin', 'admin', 'admin', 'admin', 0, 'admin', 1, GETDATE());
   ```
   
`GETDATE()` sets the current date and time for the `CreatedOn` field.

2. **Execute the Query**: Use your database management tool (such as SQL Server Management Studio for SQL Server databases) to execute this insert statement. Ensure you have the necessary permissions to insert data into the database.

### Setting up the .NET Backend

1. **Review Database Connection Settings**: Before running your .NET solution, review the application's configuration files (e.g., `appsettings.json`) to ensure that the database connection string is correctly set up to connect to your `EMedicine` database.
   
2. **Run the Solution**: Follow the previously described steps to build and run your .NET solution from Visual Studio.

### Setting up the React Frontend

Proceed as previously outlined to set up the React frontend. With your backend running, ensure the frontend can communicate with it, especially for login functionality. Given the updated user schema, make sure your login component is prepared to handle authentication correctly, using the `Email` and `Password` fields for login credentials.

### Testing Admin User Login

After setting up both backend and frontend:

1. **Log in Using the Admin Credentials**: With the frontend application running, attempt to log in using the `Email` and `Password` you set for your Admin user. This will help verify that the Admin user has been successfully added and can log in.

2. **Verify Admin Access**: Once logged in, ensure the Admin user has access to the expected areas of the application, aligning with the `Type` = 'admin' role.

By following these detailed steps, tailored to your database schema and project setup, you should be able to successfully add an Admin user to your database and integrate this functionality into your .NET and React projects.
