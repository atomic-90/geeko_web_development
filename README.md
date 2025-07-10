# Geeko Dev Django Project

A full-stack Django web application with custom user authentication, file uploads, contact forms, discussion threads, and Docker deployment.

##Features

- Custom User model with registration, login, logout
- File upload and storage system
- Contact form with database storage
- Discussion and reply threads with AJAX support
- Role-based content (staff vs normal users)
- Fully containerized with Docker
- SQLITE3 DB support

## Project Structure

geekodev/
├── Dockerfile
├── manage.py
├── Project/
│ ├── models.py
│ ├── views.py
│ ├── templates/
│ └── …
├── db.sqlite3
├── requirements.txt
└── …

## Setup Instructions

# open in a virtual environment (in terminal)

source env/bin/activate (for mac commands)

# Install dependencies

pip install -r requirements.txt

# Run migrations

python manage.py makemigrations
python manage.py migrate

# Run development server

python manage.py runserver

# Create Super user (optional) - already created

username : admin
password : admin
email : admin@admin

## Docker support

docker build -t myapp

docker volume create myapp-storage

docker run -ti -e
DATABASE_URL="mysql://myappdbuser:myappdbpass@host.docker.internal:3306/
myappdb" -v myapp-storage:/app/storage -p 8000:8000 myapp

## License

Copyright Geeko(c) 2025 [Neel Rajadhyaksha]

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"),  
to deal in the Software without restriction, including without limitation  
the rights to use, copy, modify, merge, publish, distribute, sublicense,  
and/or sell copies of the Software, and to permit persons to whom  
the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included  
in all copies or substantial portions of the Software.

**THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND**,  
express or implied, including but not limited to the warranties of  
merchantability, fitness for a particular purpose and noninfringement.  
In no event shall the authors or copyright holders be liable  
for any claim, damages or other liability, whether in an action of contract,  
tort or otherwise, arising from, out of or in connection with the software  
or the use or other dealings in the software.
