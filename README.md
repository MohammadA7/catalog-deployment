# Catalog-deployment
This is a udacity project to deploy your catalog application, and this file is a description
on how the project is deployed in detaild steps.

## Summary of software deployment
The application was deployed on AWS light stall configration steps:
1- Changed SSH default port
2- Configered firewall to allow specific ports
3- Created user and added it to sudoers group 
4- Forced Public key authentication
5- Installed and configure apache2 to serve to two virtual hosts (frontend and backend), also to act as reverse proxy in front of the backend
6- Installed and configure redis to limit requests rate
7- Installed and configure PostgresSQL

## Access details
* IP: 18.184.86.204
* URL of the web application: http://18.184.86.204/login
* SSH port 2200
