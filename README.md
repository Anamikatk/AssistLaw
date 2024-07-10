# AssistLaw
## Legal Document Assistant using AI.

- Legal documentation is complex and time-consuming, especially for individuals and small businesses without legal resources.
- Legal language and jargon are often difficult for non-lawyers to understand, leading to errors and misunderstandings.
- AI-powered solution to simplify legal documentation in India for individuals and small businesses.
- The solution aims to automatically draft legal documents in plain language and easy-to-understand terms.
- It is designed to be user-friendly, accessible, and cost-effective.

**Impact**: The proposed solution can greatly benefit individuals and small businesses in India, who often face challenges with legal documentation due to limited access to legal resources. By simplifying legal documentation, this solution can potentially save time, reduce errors, and increase access to justice. 

**Data**: We have made use of [LawRato](https://lawrato.com/legal-documents) for the dataset of legal documents.

## Technologies Used

- ![flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)

- ![react](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

- ![python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)

- ![postgresql](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

- ![tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## Setup
- `Python` and `NodeJS`should be installed on your machine before running this application
- Clone the repository into your system, and enter the repository in your terminal:
```
git clone https://github.com/AbhxyDxs/AssistLaw_v2.0.git
cd AssistLaw_v2.0/
```

#### Frontend - Client Side

Open a new terminal in root folder and navigate to the client folder

```
cd client/
```

Install all the required dependencies

```
npm i
```

To run the frontend

```
npm start
```

Once the above command is executed, the frontend will be running at ```localhost:3000```.  
You can visit http://localhost:3000/ to view the website.

#### Backend - Server Side

Open a new terminal in root folder and navigate to the server folder 

```
cd server
```

Create a `Virtual Environment` to install all the dependencies

```
python -m venv assistlaw
```

Now Activate the virtual environment

For Windows:  
```
assistlaw\Scripts\activate
```

For Linux:  
```
source assistlaw/bin/activate
```

Install all the required dependencies

```
pip install -r requirements.txt
```
We're going to host our database for the server on [Render](https://render.com/).  
It is a fully-managed cloud platform where you can host static sites, backend APIs, databases, cron jobs, and all your other apps in one place.  

To create a database on Render and creating a Environment file, follow the given steps

1. Visit the official [Render](https://render.com/) website and create an Account or Log in. 
2. Next, click `New PostgreSQL` in the PostgreSQL section to create a new database service. 
3. Give an appropriate name to the DB instance and database.
4. Give user name and select a region (default `Oregon(US West)` is fine).
5. Select <b>Free</b> option in the Instance type and hit <b>Create Database</b> button at the bottom.

A new empty PostgreSQL database service will then be created. You can view all the services on your Render Dashboard.
> The PostgreSQL database service will remain free on render only upto 3 months.


Next, create a `.env` file in the root directory containing the credentials of your database.  
Sample .env file looks like:
```
DATABASE_HOST=your_database_host
DATABASE_NAME=your_database_name
DATABASE_USER=your_database_username
PASSWORD=your_database_password
DATABASE_PORT=your_database_port
```

> ```DATABASE_HOST``` in ```.env``` should be of form ```<Hostname>.<region>-postgres.render.com```.  
> For example, if the region of database is ```Oregon (US West)```  
> then hostname can be 
```
<Hostname>.oregon-postgres.render.com
```
  

You can get all this database credentials by visiting the PostgreSQL database service you created on your render dashboard.

Once the .env file is setup, next run the `createdatabase.py` script using the following command in the terminal:
```
python createdatabase.py  
```

Running the createdatabase.py script will create the entire database for you.

To run the backend

```
python app.py
```

