# textsearch
Django Text Search with PostgreSQL
A simple text search application using Django and PostgreSQL with a frontend built using HTML, CSS, and JavaScript. This app uses the Faker library to generate fake data and imports additional dummy data from the URL dummyjson.com/products. The search feature includes typo tolerance using PostgreSQL's trigram similarity, allowing you to find results even with slight misspellings (e.g., searching for "amzon" will return results for "amazon").

Features
PostgreSQL for powerful text search capabilities
Faker Library to generate and insert random fake data
Dummy Data Import from dummyjson.com/products
Trigram Similarity to handle typographical errors in searches
Frontend built with HTML, CSS, and JavaScript
Setup Instructions
Install PostgreSQL
Download and install PostgreSQL if you haven’t already, and open pgAdmin.

Create Database and Table

Open pgAdmin, create a new database (e.g., search).
Set a password for your PostgreSQL user and ensure it's configured in your Django settings.
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/django-textsearch.git
cd django-textsearch
Install Dependencies
Make sure to have a virtual environment, then install dependencies:

bash
Copy code
pip install -r requirements.txt
Configure Database
Update DATABASES settings in settings.py to use PostgreSQL, including your database name, user, and password.

Run Migrations
Apply migrations to set up initial database schema:

bash
Copy code
python manage.py makemigrations
python manage.py migrate
Insert Fake Data
Run the scripts.py file to populate the database with fake data:

bash
Copy code
python scripts.py
Start the Server
Launch the Django development server:

bash
Copy code
python manage.py runserver
Access the Application
Open your browser and go to http://127.0.0.1:8000 to use the text search functionality.

Notes
Ensure pg_trgm extension is enabled in PostgreSQL to use trigram similarity:

sql
Copy code
CREATE EXTENSION pg_trgm;
Trigram similarity enables the application to return accurate search results even when queries contain typographical errors.

Technologies Used
Django for backend development
PostgreSQL for database with text search capabilities
Faker Library and DummyJSON API for dummy data
HTML, CSS, JavaScript for frontend
