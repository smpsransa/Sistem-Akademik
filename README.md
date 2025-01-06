# Sistem-Akademik
To run your Laravel project from C:\Users\Hype GLK\Documents\GitHub\Sistem-Akademik\backend while using Laragon's web server, you can create a symbolic link (symlink) in Laragon's www directory that points to your Laravel project directory. This way, Laragon will serve your project as if it were inside its www folder.

Follow these steps to create the symlink:

Open Command Prompt as Administrator:

Search for cmd in the Start menu.
Right-click on Command Prompt and select Run as administrator.
Navigate to Laragon's www directory:

cd C:\laragon\www
Create the symbolic link:

mklink /D backend "C:\Users\Hype GLK\Documents\GitHub\Sistem-Akademik\backend"
Explanation:
mklink is the command to create a symbolic link.
/D specifies that the link is a directory.
backend is the name of the symlink that will be created in C:\laragon\www.
"C:\Users\Hype GLK\Documents\GitHub\Sistem-Akademik\backend" is the target directory of your Laravel project.
After creating the symlink, you should see a folder named backend in C:\laragon\www. This folder is actually a link to your Laravel project directory.

Verify the Setup:
Start Laragon if it is not already running.
Open your web browser and navigate to http://localhost/backend.
You should see your Laravel project's homepage, indicating that it is being served correctly by Laragon.

Additional Notes:
Ensure that you have configured your .env file properly in the Laravel project, especially the APP_URL and database connection settings.
If you make changes to your Laravel project, they will be reflected immediately since the symlink points to the actual project directory.
By following these steps, you can run your Laravel project using Laragon without moving your project files into Laragon's www directory.

