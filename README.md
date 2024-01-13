Welcome to the README.md of 

To get started pull the main branch (or the alternative ExpressServer branch)

Once pulled and opened in a continer, start by running npm install

this *should* install all the required modules. 
if you are run into issues make sure the package.json shows 
{
  "name": "23s1-wdc-ug064-wdc-3",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "node ./bin/www"
  },
  "dependencies": {
    "bcrypt": "^5.1.0",
    "cookie-parser": "~1.4.4",
    "debug": "~2.6.9",
    "express": "~4.16.1",
    "express-session": "^1.17.3",
    "morgan": "~1.9.1",
    "mysql": "^2.18.1"
  }
}

if npm install fails and the json is wrong, either copy and paste the
above into package.json or you can also install modules manually

(in any order)
npm install
npm install express-session
npm install bcrypt
npm install mysql
npm install express
npm install ... /*continue

once all the correct modules are up and running appropriately run 
service mysql start 
and wait a moment
then run mysql

in the mysql command line you can source the database via 
DROP DATABASE ClubHub; 	/*make sure any old databases are dropped
SOURCE /workspaces/23S1_WDC_UG064_WDC/db/db.sql;
USE ClubHub;

/* There are optional queries to run before running the webpage to 
/* provide the Admin user ClubManager permissions to Club A for 
/* troubleshooting purposes, and this may be something that interestes
/* you. Queries located in db/queries.sql

The ClubHub database should now be connected to the webapp

run 
npm start
and wait for the localhost (or whatever you may be using) port to open 

// Welcome to ClubHub! \\

\\ Watch the video for a tour around the website! //
