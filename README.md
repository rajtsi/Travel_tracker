**Project Setup Instructions**

Download the ZIP File:
Download the ZIP file containing the project to your system.

Ensure Node.js is Installed:
Make sure Node.js is installed and working on your system.

Install Dependencies:
Run npm install to install all required modules. These are listed in the package.json file.

Setup PostgreSQL:
Install PostgreSQL on your system.
Create a database named world with postgres as the owner.
Inside the world database, create a table named countries with the following schema:

CREATE TABLE countries (
  id SERIAL PRIMARY KEY,
  country_code CHAR(2),
  country_name TEXT
);
Upload the contents of the countries.csv file to this table. Ensure the first row is treated as the header.
You can also add any missing countries and country codes as needed.

Create another table named visited_countries in the same world database with the following schema:
CREATE TABLE visited_countries (
  id SERIAL PRIMARY KEY,
  country_code CHAR(2)
);

Update Password:
Open index.js and replace the PostgreSQL password with your own password.

Run the Project:
In the project directory, run the following command to start the project with nodemon:
nodemon index.js


At first You will get this  after opening localhost at port 3000, where no any country is marked as visited and Total count is 0.   
![1st screen](https://github.com/user-attachments/assets/58e6f635-3ec3-4790-bcfa-c3ddf9498c7b)
and visited_countries table in world database will be empty.
![Database initially](https://github.com/user-attachments/assets/b404fd98-83df-4f78-8766-eeec02f6f741)


Now add the name of the countries you visited and you will see that colour of that country changes and count of the countries increases.
![2nd screen](https://github.com/user-attachments/assets/dbe8d574-06cd-4eb1-9441-652c70d7822a)
And these countries will also be added in visited_countries table in Postgre 
![After adding](https://github.com/user-attachments/assets/a7540587-a8fb-4316-8eac-9bac40549e66)


If you will try to add a country already added it will show a message saying that Country has already been added ,try again

Here I tried to add India again and got 
![adding county_again](https://github.com/user-attachments/assets/6cf45c40-bc1c-499c-954c-93de2909168c)








