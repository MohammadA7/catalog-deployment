# Catalog-deployment
This is a udacity project, its required to deploy 
your catalog application on AWS or Google cloud,
and this file is a description on how the project is 
deployed in detailed steps.

## Summary of host configuration for deployment
1. Changed SSH default port
2. Configured firewall to allow specific ports
3. Created user and added it to sudoers group 
4. Forced Public key authentication
5. Setup some swap memory to avoid OOM error
and configured the Linux kernel vm.swappiness to 10 
to avoid moving unnecessary data to swap memory also set 
vm.vfs_cache_pressure to 50 for performance reasons
for [more details](https://gist.github.com/Nihhaar/ca550c221f3c87459ab383408a9c3928)
6. Installed PostgreSQL and created a user
for the application which has access to its database  

### Apache2 Installation and configuration:
Apache2 was installed and configured to serve to two virtual
hosts (front-end and back-end), the front-end virtual 
host is listening on any request on port 80, and the
back-end virtual host is listening on port 8080 only on 
localhost, so whenever a request comes to the front-end virtual
host with `/api` path the reverse proxy will redirect 
the request to the back-end virtual host.

### Redis Installation and configuration:
Redis was installed and configured the Linux kernel 
overcommit memory setting it to 1
to fix background saving fails with a fork() error
for [more reference](https://redis.io/topics/faq).


## Access details
* IP: 18.184.86.204
* URL of the web application: http://18.184.86.204
* SSH port 2200

## List of third party resources 
A list of third party resources used
* Udacity course Configuring Linux Web Servers
* [mod_wsgi](https://modwsgi.readthedocs.io/en/develop/user-guides/quick-configuration-guide.html)
documentation
* [Flask](http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/) documentation
* [Passing env varibles to mod_wsgi](http://ericplumb.com/blog/passing-apache-environment-variables-to-django-via-mod_wsgi.html)
* [PostgreSQL](https://www.postgresql.org/docs/) documentation
* [Redis](https://redis.io/topics/admin) administration guide
