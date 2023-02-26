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



