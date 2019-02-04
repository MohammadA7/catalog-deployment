# Catalog-deployment
This is a udacity project, its required to deploy your catalog application on AWS or Google cloud, and this file is a description
on how the project is deployed in detailed steps.

## Summary of software deployment
The application was deployed on AWS light stall configuration steps:
1. Changed SSH default port
2. Configured firewall to allow specific ports
3. Created user and added it to sudoers group 
4. Forced Public key authentication
5. Installed and configure apache2 to serve to two virtual hosts (frontend and backend), also to act as a reverse proxy in front of the backend
6. Installed and configure Redis to limit requests rate
7. Installed and configure PostgreSQL

## Access details
* IP: 18.184.86.204
* URL of the web application: http://18.184.86.204
* SSH port 2200
