# Week 1 — App Containerization

## Required Home Work and Tasks

I went over all the required videos on youtube 

### Debugging
I learnt how to debug my error adequately before asking for help

- I learnt how to read and understand HTTP Response Status codes [Study link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) 
- Though I am not experienced with python but I went over an article about Python Break points.

Python breakpoint() is a new built-in function introduced in Python. Python code debugging has always been a painful process because of the tight coupling between the actual code and the debugging module code.
 Its helpful to use in debugging so that you can easily hook other third-party debuggers on the fly. It also provides an easy option to disable the debugger and runs the program normally.
 [Source](https://www.digitalocean.com/community/tutorials/python-breakpoint)
 
 - I also learnt how to ask for help while providing adequate information

### Running Cruddur App on a Container
I wrote a dockerfile for my backend python application folder

![backend dockerfile](/assets/backend_dockerfile.jpg)

I moved to my frontend application folder
i run the the installation command to install all dependencies on the react app

``` npm install ```

I then wrote a dockerfile for my frontend react application

![frontend dockerfile](/assets/frontend_dockerfile.jpg)

I created a docker compose yaml file at the root folder of my project, leveraging the Docker Compose tool to run all containers with one command

Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

![docker-compose file](/assets/docker-compose.jpg)

I composed up my dockerfiles using the docker vscode extension 

![docker extension](/assets/docker-extension.jpg)

I confirmed that my containers are running and that the ports are open

![container running](/assets/container-running.jpg)

![full application](/assets/application.png)

### Container Security and Best Practices
I was able learn what Synk open-source security for docker is.
I scanned Dockerfiles of my Cruddur App for vulnabilities using Synk.io and it turned out I had vulnerabilities in my frontend dockerfile due to the fact that it doesn't run on the most updated version of NodeJS

![Vulnerabilities](/assets/vun.png)

![Vulnerabilities](/assets/vun-rec.png)

I was able to reduce the vulnerability of my frontend Dockerfile by updating it to the lastest version

![reduced vulnerability](/assets/fixed-vun.jpg)

more imformation about how to use SYNK can be found at this [link](https://docs.snyk.io/)

### Write a Flask Backend Endpoint for Notifications
I was able to implement notification functionality on my Cruddur app
I  created a new GET path in my OpenAPI yaml file

![openAPI](/assets/openAPI-notification.jpg)

then I created a Route in my backend app.py file and also a mock response data

![openAPI](/assets/notification-api.jpg)

![openAPI](/assets/notification-api2.png)


### React Page for Notifications
I implemented the notification feature on my app frontend

![frontend](/assets/react-notif.png)

![frontend](/assets/frontend-notification.jpg)

### Run Postgres Container

I wrote added scripts to create Postgres and DynamoDB local in my docker compose file

![docker copose file](/assets/dynamo-dockercompose.jpg)

I then write a script in my gitpod yaml file to install Postgres in Gitpod on start up

![docker copose file](/assets/postgres-install.jpg)

I installed a postgres extension, created containers from my docker compose file and connected to postgres container 

![docker copose file](/assets/postgres-connected.jpg)
