# BDAT1001_Final_Project-Grp-10
An ASP.NET Core web app with user data protected by authorization
Microsoft.VisualStudio.Web.CodeGeneration.Design package must be installed for this project. Please run the following code in the powershell to install the package.

dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design


When we are setting up the files in a new machine, we need to set the password by using the Managing user secret tool. To do that please follow the following steps.
1. Right click the main contact_manager file from the solution exoplorer
2. Select the option that says "Manage user secret"
3. Please set following code there or else please set the seed_User_password.
{
  "SeedUserPW": "Password@123"
}

Note: ( If the necessary migration files are not set)

In order to set the migrations, please run the following commands in the powershell. 

dotnet ef database drop -f      (To delete the database)
Then manually delete the Initial.cs and userID_status.cs migration files from the migrations (Navigate through solution explorer.)
Run the following commands accordingly in the powershell to set the migration files
dotnet ef migrations add initial 
dotnet ef database update
dotnet ef migrations add userID_Status
dotnet ef database update
