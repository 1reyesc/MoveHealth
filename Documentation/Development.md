# Environment Replication Manual
# Environment Variables
- Windows OS
- VSCode as Text Editor
# Backend Dependencies 
### Ruby 3.0
-  You can install ruby using this installer: https://rubyinstaller.org/downloads/archives/
- After going to the link you can look for one that says  Ruby+Devkit 3.0.0-1 (x64) and download and install that
### Rails 
- For this project, we need rails version 6.0.3.3 or above
-  In the terminal in VSCode you can type "gem install rails" to install rails
-  To verify the status you can run "rails -v" after to check if rails is installed and what version
### NodeJS and NVM
- We need Node version 18.17.1
-  To install NodeJS you will need to go to https://nodejs.org/en
-  Then click download Node.js(LTS)
-  To install NVM you can follow this guide: https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/
-  After installing NVM you can run "nvm install 18.17.1" in the terminal
-  Then run "nvm use 18.17.1" and do "node -v" to verify the correct node version is correct.
### Yarn
- We need Yarn version 1.22.19
- In the terminal of VSCode you can run "npm install -g yarn@1.22.19"
- Afterwards, run "yarn -v" to verify the version.
### Curl for Windows
- This is needed for Windows OS
- Download from here: https://curl.se/download.html
- Find the .zip file and download and unzip the folder
- Keep the folder in a safe space where you won't accidentally delete it

### PostgreSQL
- Database that is used for this project
- Download from here: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
- Find the most recent version and install the Windows x86-64 one
- Follow the install wizard.
- You will need to keep track of the password you create to open your server
- Set the Port to 5432
- Once you reach Stackbuilder you can cancel out and stop.

# Next Steps
## Installing Curb
- After getting ruby, rails, node, and yarn set up you can move onto setting up curb
- To do so you will run this in the Terminal: gem install curb -v '1.0.6' -- --with-curl-lib="your path to lib" --with-curl-include="your path to include"
- Inside this command are placeholder paths that you will need to fill in that are specific to your computer
- To locate the path you will need to locate your Curl folder that you installed.
- Inside of it you will need to note the path to the lib folder and paste that into the first placeholder path
- Next you will need to note the path to the include folder and paste that into the second placeholder path
- After getting the correct paths setup you can run the command
- It might take a while which is normal

## Bundle Install
- After successfully installing curb, in the Terminal you can run: bundle install
- This will install all the other dependencies for this project

## Running dev
- Before you can start up the rails application you will need to do a command: npm run dev
- To successfully run this command you will need to do two things
- First, locate the package.json file
- Once located find scripts and in the "dev" row you want to make sure it is: "cross-env NODE_OPTIONS=--openssl-legacy-provider bin/webpack-dev-server"
- <img src="https://github.com/1reyesc/MoveHealth/blob/master/Auxiliary%20Files/crossenv.png" width="350">  
- Second, run this command in the terminal: yarn add cross-env --dev
- Let it run and then run the command: npm run dev

## Setting up Database
### Things needed
-  move_development folder containing the sql script for importing database
-  PostgreSQL installed
### Steps
- Once you have PostgreSQL installed and you have the move_development folder you will need to import the database and connect the project to it
- Open up pgAdmin 4 app through Windows
- Once open you can right click Databases and create a new one called move_development
- Once created right click move_development and click Query Tool
- In top left you will find a file opener click it
- It will open up a file explorer you will need to locate the move_development folder 
- Once located open it up and select the move_development file
- Once loaded in you can click on the play button and it will run the script


## Running Rails
-  Once you imported the database you will now need to point it in your database.yml file in the config folder of the project
-  Make sure it looks like this:
-  <img src="https://github.com/1reyesc/MoveHealth/blob/master/Auxiliary%20Files/databaseyml.png" width="350">  
- Create a .env file in your root:
- <img src="https://github.com/1reyesc/MoveHealth/blob/master/Auxiliary%20Files/env.png" width="350">  
-  Then add the local_DATABASE_PASSWORD variable and set it to your Database Password
-  After that you can run command: npm run rails
-  Go to localhost:3000 and you should be able to view the webapp
  





