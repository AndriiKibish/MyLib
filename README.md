MyLib Deployment Instructions

Prerequisites:
Python (3.10 or higher)
Django Django 5.0.1
Database server (e.g., PostgreSQL)
Web server (e.g., Nginx or Apache)

1. Clone the Project:
git clone https://github.com/AndriiKibish/MyLib
cd MyLib

2. Create a Virtual Environment:
python3 -m venv venv
source venv/bin/activate   
# On Windows: .\venv\Scripts\activate

3. Install Dependencies:
pip install -r requirements.txt

4. Configure Database:
Update the DATABASES settings in settings.py to match your database configuration.

5. Apply Migrations:
python manage.py migrate

6. Create Superuser (Optional):
python manage.py createsuperuser

7. Run the Development Server:
python manage.py runserver

8. Access the Application:
Open your web browser and go to http://localhost:8000 to access the development server.

9. Configure Web Server:
For production, configure a web server like Nginx or Apache to serve the Django application. 
Update the server configuration to point to the project's wsgi.py file.

10. Collect Static Files:
python manage.py collectstatic

11. Set Environment Variables:
Set any necessary environment variables, such as DJANGO_SECRET_KEY and DJANGO_DEBUG.

12. Secure Settings (Optional):
Ensure that your settings.py file is configured securely for production, including proper secret key management and debug settings.

13. Run Migrations in Production:
python manage.py migrate --settings=MyLib.production_settings

14. Additional Configuration (Optional):
Configure a production-ready database server.
Set up HTTPS using a certificate from a trusted certificate authority.

15. Restart Web Server:
Restart your web server to apply any changes.

16. Access the Deployed Application:
Open your web browser and go to your deployed application's URL

Congratulations! Your Django project is now deployed and accessible. Make sure to follow best practices for securing your production environment.
