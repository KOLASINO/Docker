# Docker
Did you know it is possible to create a docker image without using a docker file. However, it is important to note that Dockerfile provides a structured way to define how your Docker image should be constructed, making image creation efficient, consistent, and manageable. 

The images below show how I created a docker image with a Dockerfile.

1. I created a directory by running this command "mkdir learn-docker" in PowerShell.

2. I switched to the new directory by running this command cd learn-docker.

3. I used VS code as my editor.

4. In the learn-docker folder In VS code, I created a file named app.js, and wrote a line of JavaScript console.log ("hello Docker!");

5. In VS code, I added a Docker file in the LEARN-DOCKER folder and inputted the following variable:
 FROM node:alpine
 COPY ./ app
 WORKDIR /app
 CMD node app.js

✅ The "FROM" instruction is the first line in a Dockerfile, it specifies the base image for the new image being built, in this case, it says to use the official Node.js image with the Alpine Linux distribution as the base.

✅The COPY ./ app instruction is used within a Dockerfile to copy files or directories from the host machine (where the Docker build is happening) into the image being created.

✅The WORKDIR /app instruction sets the working directory inside the Docker image.

✅The CMD node app.js instruction specifies the default command to run when a container based on the image starts.

6. In the CLI, I ran docker build -t kola-docker. (the -t stands for tag)

7. To confirm if the image was created successfully, I ran "docker images"
8. ![image](https://github.com/KOLASINO/Docker/assets/135536416/a444dc5e-8c2a-4e87-b2d1-fd4fc617514a)
9. ![image](https://github.com/KOLASINO/Docker/assets/135536416/00b1690a-abb4-40cf-88bb-cda28b4821d2)
![image](https://github.com/KOLASINO/Docker/assets/135536416/1a33b7e0-3225-4323-b216-abd0dd9d04d2)

