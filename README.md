Build a REST API in Python

This project demonstrates how to build a fully functional REST API in Python using Flask and SQLAlchemy. It covers everything from the basics of APIs to integrating a database and testing endpoints with Postman.

What is an API?

An API (Application Programming Interface) allows communication between a client (front-end) and a server (back-end).
This project implements a REST API (Representational State Transfer), which organizes resources into unique URIs and supports standard CRUD operations:

POST → Create data

GET → Read data

PUT → Update data

DELETE → Delete data

All interactions are handled with JSON payloads for cross-language compatibility.

⚙️ Tech Stack

Python 3

Flask → Lightweight framework for API routes

Flask-SQLAlchemy → ORM to manage database models

SQLite → Database backend

Postman → API testing

🛠️ Setup Instructions

Clone the repo

git clone https://github.com/your-username/build-rest-api-python.git
cd build-rest-api-python


Create a virtual environment

python3 -m venv api_env
source api_env/bin/activate


Install dependencies

pip install -r requirements.txt


Run the app

python app.py


Your API will be live at:

http://127.0.0.1:5000

📂 Project Structure
├── app.py              # Main Flask application
├── requirements.txt    # Dependencies
├── instance/
│   └── travel.db       # SQLite database (auto-generated)
└── README.md           # Documentation

🧩 Database Model

The project uses a simple Destinations table:

Field	Type	Description
id	Integer	Primary key
destination	String	City or location name
country	String	Associated country
rating	Float	Rating score (1.0 - 5.0)
🔑 API Endpoints
Method	Endpoint	Description
GET	/	Welcome message
GET	/destinations	Fetch all destinations
GET	/destinations/<id>	Fetch destination by ID
POST	/destinations	Add a new destination
PUT	/destinations/<id>	Update destination by ID
DELETE	/destinations/<id>	Delete destination by ID
🧪 Testing with Postman

Open Postman and enter the API base URL:

http://127.0.0.1:5000


Test requests:

GET /destinations → Returns all data in JSON.

POST /destinations with body:

{
  "destination": "Paris",
  "country": "France",
  "rating": 4.8
}


PUT /destinations/1 → Update entry with ID 1.

DELETE /destinations/1 → Remove entry with ID 1.