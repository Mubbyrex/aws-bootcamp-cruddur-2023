# Week 1 — App Containerization

## Required Home Work and Tasks

I went over all the required videos on youtube 

### Debugging
I learnt how to debug my error adequately before asking for help

- I learnt how to read and understand HTTP Response Status code [Study link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) 
- Though I am not experienced with python I also went over an article about Python Break points is.

Python breakpoint() is a new built-in function introduced in Python. Python code debugging has always been a painful process because of the tight coupling between the actual code and the debugging module code.
 Its helpful to use in debugging so that you can easily hook other third-party debuggers on the fly. It also provides an easy option to disable the debugger and runs the program normally.
 [Source](https://www.digitalocean.com/community/tutorials/python-breakpoint)
 
 - I also learnt how to ask for help while providing adequate information

### Running Cruddur App on a Container
I wrote a dockerfile for my backend python application

![backend dockerfile](/assets/backend_dockerfile.jpg)

I move to my frontend app
i run the the installation command to install all dependencies on the react app

``` npm install ```

I then wrote a dockerfile for my frontend react app

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
I scanned Dockerfiles of my Cruddur App for vulnabilities using Synk.io and it returned out I had vulnerabilities in my frontend dockerfile due to the fact that it doesn't run on the most updated version of NodeJS

![Vulnerabilities](/assets/vun.png)

![Vulnerabilities](/assets/vun-rec.png)

I was able to reduce the vulnerability of my frontend Dockerfile by updating it to the lastest version

![reduced vulnerability](/assets/fixed-vun.jpg)

more imformation about how to use SYNK can be found at this [link](https://docs.snyk.io/)

### Write a Flask Backend Endpoint for Notifications
I was able to implement notifivation functionality on my Cruddur 
I 
created a new GET path in my OpenAPI yaml file

![openAPI](/assets/openAPI-notification.jpg)

then I created a Route in my backend app.py file and also a mock response

![openAPI](/assets/notification-api.jpg)

![openAPI](/assets/notification-api2.png)


### React Page for Notifications
implentend the notification feature on my app frontend

![frontend](/assets/react-notif.png)

![frontend](/assets/frontend-notification.jpg)

