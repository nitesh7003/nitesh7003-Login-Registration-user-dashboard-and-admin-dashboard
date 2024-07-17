Program Structure Overview
Controllers:

AccountController: Handles user registration, login, and logout. Uses sessions to store user role information (User or Admin).
AdminController: Manages admin-specific functionalities like AdminDashboard.
Data:

ApplicationDbContext: Manages database interactions. Includes a Users table to store user information.
Models:

User: Represents a user with properties like Name, Email, and Password.
LoginModel: A model used for login containing Email and Password.
Views:

Account/Login.cshtml: Form for user login.
Account/Register.cshtml: Form for user registration.
Admin/AdminDashboard.cshtml: Dashboard view for admin functionalities.
_Layout.cshtml:

Defines the layout of the application's pages, including navigation links (Home, Privacy, Admin Dashboard, User Dashboard), which are conditionally displayed based on the user's role stored in session.
Program.cs:

Configures services like MVC, DbContext for database access, and session management.
Sets up routing for different controllers and actions.
Key Functionalities
Registration: Allows users to register with a name, email, and password.
Login: Validates user credentials and sets session variables based on whether the user is an admin or a regular user.
Session Management: Ensures that session variables (UserRole) are correctly utilized to show/hide admin-specific functionalities in the navigation bar.
Admin Dashboard: A dedicated view accessible only to users with admin privileges, demonstrating how role-based access can be implemented.
This setup helps manage user authentication and authorization through simple yet effective use of ASP.NET Core MVC, session handling, and database interactions.
