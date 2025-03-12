# Dockerized Node.js App

This project demonstrates how to containerise a simple Node.js application using Docker. The app is built using Express.js and is designed to be run inside a Docker container for easy deployment and portability.

## What This Project Does

- The application is a basic Node.js app built with the Express framework
- It sends a simple "Hello from Dockerised Node.js app!" message when accessed
- The project was packaged into a container using Docker

## Steps Taken in This Project

### 1. Set up a Node.js Application
- I created a basic Node.js application using Express.js.
- The app listens on port 3000 and returns a simple message to the user.

### 2. Dockerized the Node.js App
- I used the `node:alpine` Docker image as a base to minimize the size of the Docker image.
- The Dockerfile was written to:
  - Set the working directory inside the container to `/app`.
  - Copy the `package.json` and `package-lock.json` files.
  - Install all the necessary Node.js dependencies using `npm install`.
  - Copy the rest of the project files into the container.
  - Expose port 3000 for the application.
  - Start the application using `node server.js`.

### 3. Built and Ran the Docker Image
- I built the Docker image using the following command:
  ```bash
  docker build -t node-docker-app .
- Then i ran the container using:
  ```bash
  docker run -p 3000:3000 node-docker-app


### 4. Access the App
- To verify that it worked, I navigated to http://localhost:3000 via microsoft edge and got the output "Hello from Node.js!"

  
![Screenshot 2025-03-12 162950](https://github.com/user-attachments/assets/d981503d-a735-47e7-91ad-8f7412a25d8f)
