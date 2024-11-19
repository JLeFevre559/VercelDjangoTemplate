# VercelDjangoTemplate
A template for a simple hello world app on Vercel that includes fixes for static file issues from the Django template hosted by Vercel.
The most important piece of this template is the build.sh file, and you could move that into an already existing django deployment on vercel to fix problems individually. 

Instructions to deploy this template:
 1. Clone this repository
 2. Move the application folder into your desired project
 3. Rename 'example' to your preferred app name in the following locations:
    * application/example (rename folder)
        * /apps.py
    * application/vercel_app
        * /urls.py
        * /settings.py
4. Check that your local version runs
    * cd to application
    * (Optional - Recommended) start a virtual environment
    * run "pip install -r requirements.txt"
    * run "python manage.py runserver"
    * visit 127.0.0.1:8000 and ensure that the icon appears in the top bar
5. Push to repo
6. Go to your vercel dashboard
7. Add new project
8. Select repository
    * Import 3rd party repository if you are not the owner, or your vercel account is not connected to your github account
9. Framework preset: other
10. Set root directory to /application
11. Deploy
12. Check your project deployment to ensure the icon is showing in the top bar
    * This indicates that static files are working. Enjoy creating your project!


## Notes:
* Replace the favicon files in static/images
* The current database setup uses a local database for test purposes, but you will need to connect to your own database.
    * Add your database info in a .env in /application 
    * Upload your .env info to Vercel
* Don't forget to generate a secure django key and store it in your .env