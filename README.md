# NewWeb Blazor Application

## Overview
This is a Blazor-based web application built on `.NET 8`. The application includes an **Admin Area** for managing users, roles, and companies. It leverages **ASP.NET Core Identity** for authentication and role-based authorization.

## Features
- **User Management**: Add, edit, lock/unlock users.
- **Role Management**: Assign and update roles for users.
- **Company Management**: Manage company details associated with users.
- **Blazor Integration**: Modern UI with Blazor components.
- **Entity Framework Core**: Database operations using EF Core.
- **ASP.NET Core Identity**: Secure authentication and role-based authorization.

## Technologies Used
- **.NET 8**
- **Blazor**
- **Entity Framework Core**
- **ASP.NET Core Identity**
- **Microsoft SQL Server**

## Project Structure
NewWeb/ ├── Areas/ │   ├── Admin/ │   │   ├── Controllers/ │   │   │   └── UserController.cs │   │   ├── Views/ │   │   │   └── RoleManagement.cshtml ├── DataAccess1/ │   ├── Data/ │   │   └── ApplicationDbContext.cs │   ├── Repository/ │   │   ├── IRepository/ │   │   └── Repository/ ├── Models/ │   ├── ApplicationUser.cs │   ├── RoleManagementVM.cs │   ├── Company.cs ├── Utility/ │   └── SD.cs


### Key Files
- **`UserController.cs`**: Handles user and role management logic.
- **`ApplicationDbContext.cs`**: Configures the database context and models.
- **`RoleManagementVM.cs`**: ViewModel for managing roles and companies.
- **`SD.cs`**: Static details for role definitions and constants.

## Setup Instructions
1. **Clone the Repository**:
   git clone <repository-url> cd NewWeb
   
2. **Configure the Database**:
   - Update the connection string in `appsettings.json`:
      "ConnectionStrings": {
   "DefaultConnection": "Server=YOUR_SERVER;Database=NewWebDb;Trusted_Connection=True;MultipleActiveResultSets=true"
 }
 
3. **Apply Migrations**:
   Run the following commands to create the database:
   dotnet ef migrations add InitialCreate dotnet ef database update
   
4. **Run the Application**:
   Start the application using:
   dotnet run
   
5. **Access the Application**:
   Open your browser and navigate to:
   http://localhost:5000

## Role Management
- **Admin Role**: Full access to the application.
- **Company Role**: Limited access to company-specific data.
- **Employee Role**: Basic access for employees.
- **Customer Role**: Basic access for customer.
### Adding Roles
Ensure roles are seeded in the database. You can add roles programmatically in the `ApplicationDbContext` or via the Admin interface.

## API Endpoints
### User Management
- **Get All Users**: `GET /Admin/User/GetAll`
- **Lock/Unlock User**: `POST /Admin/User/LockUnlock`

### Role Management
- **Assign Role**: Managed via the `RoleManagement` view.

## Contributing
1. Fork the repository.
2. Create a feature branch:
   git checkout -b feature/your-feature
3. Commit your changes:
   git commit -m "Add your message"
4. Push to the branch:
   git push origin feature/your-feature
   5. Open a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
For questions or support, please contact:
- **Email**: vinhtung1410@gmail.com
- **GitHub**: [Your GitHub Profile](https://github.com/VinhTung1410)

   
   
