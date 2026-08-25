# C# & SQL Server Authentication System

This is a Windows Forms desktop application built in C# (.NET Framework) that provides secure User Registration, User Login, and Dashboard navigation with a Session Logout feature.

## What the Application Does
* **User Registration:** Allows new users to create an account with a unique username and matching passwords. Accounts are stored directly in a SQL Server database.
* **User Login:** Authenticates users against stored database credentials and redirects to a main Dashboard upon successful verification.
* **Dashboard & Logout:** Displays the user dashboard after authentication and allows users to securely terminate their session and return to the login interface.

---

## How to Run the Application

### 1. Database Setup
1. Open SQL Server Management Studio (SSMS) or Visual Studio's SQL Server Object Explorer.
2. Open and execute the included `database.sql` script to create the `db_users` database and `tbl_users` table with an initial test user.
3. Test Login Credentials:
   * **Username:** `admin`
   * **Password:** `admin123`

### 2. Connection String Configuration
If your local SQL Server instance name differs from `(localdb)\MSSQLLocalDB`, update the `connectionString` attribute inside `App.config`:

```xml
<connectionStrings>
  <add name="connString" 
       connectionString="Data Source=(localdb)\MSSQLLocalDB;Initial Catalog=db_users;Integrated Security=True;Connect Timeout=30;Encrypt=False;TrustServerCertificate=False" />
</connectionStrings>
