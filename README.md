Ref [https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/#nginx](http://localhost:3000) site.<br>
Ref [https://github.com/testdrivenio/django-on-docker](http://localhost:3000) site.

## docker-compose.yml
The  file describes the services that make your app.
Eexample of those services could be a 
web server[inbuilt django wsgior gunicorn],
database server [eg:postgres].
redis server
[NB:] Each of these services are containers which are been called to be executed in it respective container 
The compose file also describes which Docker images these services use,
how they link together, any volumes they might need to be mounted inside the containers.
Finally, the docker-compose.yml file describes which ports these services expose.

This uses the build in development server to run your application on port 8000.
Do not use this in a production environment. For more information


## Dockerfile
The Dockerfile defines an application’s image content via one or more
build commands that configure that image. Once built, you can run the image in a container

This Dockerfile starts with a Python 3 parent image.
The parent image is modified by adding a new code directory.
The parent image is further modified by installing the Python requirements defined in the requirements.txt file.



## entrypoint.sh
verify that Postgres is healthy before applying the migrations and running the Django development server: