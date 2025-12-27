<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Deploy an App with Docker

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-eb)

**Author:** Aaron 
**Email:** justaaron1981@yahoo.com

---

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-compute-eb_c4df13c84)

---

## Introducing Today's Project!

### What is Docker?

Docker is Docker is an open-source platform that enables developers to build, deploy, run, update, and manage applications within isolated environments called containers. It addresses the "it works on my machine" problem by ensuring consistency across different environments, from development to production. I used Docker in this project to set up containers based on container images and set up our own container image.

### One thing I didn't expect...

One thing I didn't expect in this project was that i would have to use docker in visual studio code for windows 

### This project took me...

This project took me approximately 2hours The most challenging part was translating it to windows. It was most rewarding to see how docker works

---

## Understanding Containers and Docker

### Containers

Containers are tools for packaging applications in away that's easy for developers to run. They are useful because it helps developers/engineers working together in a team together to share their work in a more efficient way

A container image is a template or a blueprint for creating container image for creating containers. Containers spawned/created from the same container image will behave in the same way. Which helps with developers in a team having a unified experience when they're running the same application.

### Docker

Docker is a platform for creating and managing containers. Docker makes working with containers easy Docker Desktop is a software for using docker. Docker desktop makes using Docker it self easy too.

The Docker daemon is the 'engine' for docker that receives commands we send through clients e.g. clientents in the docker desketop or text commands sent in the terminal and actually creates/manages/controls thel containers

---

## Running an Nginx Image

Nginx is a web server/or a software that helps with server  that helps with serving content. Nginx is often refered to as a proxy server, which means it helps with distributing traffic to your application accross the instances running your application

The command I ran to start a new container was ' docker run' we also set the flags '-d -p 80:80 nginx' which means we're running the container in the background (-d)and we're matching port 80 in our host computer to the container's port 80 (-p 80:80)

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-compute-eb_6245f5bb10)

---

## Creating a Custom Image

the dockerfile is a set of instructions that tells docker how to build your custom container image

My Dockerfile tells Docker three things. First, our custom container i mage uses the latest version of Nginx image container at it's base. Then, I modified on this base by saying I want  the Ngnix web server to serve our custom index HTML

The command I used to build a custom image with my Dockerfile was Dockerbuild. The '.' at the end of the command means that Docker can find the directory I.E. the compute folder on my desktop.

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-compute-eb_4c741d1913)

---

## Running My Custom Image

There was an error when I ran my custom image because I tried to map my port 80 with the new container's port 80, but a container was already running and using port 80. I resolved this by stopping the container so that I can start a new one.

In this example, the container image is the container is the template for creating a new container running Nginix server that serving my custom index.html file. The container is the actual software that's running Nginx server with those specifications with those customisations.

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-compute-eb_74b5c3d619)

---

## Elastic Beanstalk

Elastic Beanstalk is an AWS that helps deploying applications to the cloud it abstracts a way a lot of the work with setting up cloud infastructure when deploying applications

Deploying my custom image with Elastic Beanstalk took me 10 minutes. This includeds the time it took to launch the elastic beanstalk application

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-compute-eb_26d5573b23)

---

## Deploying App Updates

---

---
