# Deployment
## Steps
- Sign up for Heroku
- Once in you can click on Create New App
- On the Dashboard, go to "Deploy" and connect to your Github Repository
- Enable Auto Deploy
- Then click Deoply Branch
- It will take a while to download gems and other dependencies
- Once done you can click on Open App

## Error Logs
- To find this you can click on the More tab next to Open App
- Click on view logs to check out the logs for potential issues

## Critical Place
-  Making sure Auto Deploy is enabled makes sure that your webapp is updated automatically as soon as there are changes in your master branch

# Replicating via Docker

## Install Prerequisites
- Download and Install Docker Desktop
  - https://www.docker.com/products/docker-desktop
  - Have up in running once installed 

## Clone Repos 
- clone repository in visual studio code
  - https://github.com/Move-Health/move

## Run
- Docker compose up --build for first time running
- Docker compose up for regular compose
