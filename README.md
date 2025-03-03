# Flask_Sandro_Casanova_Pol_Cerrillo
This repository contains the necessary configuration to deploy a Flask application inside a Docker container. It also includes an SSH server for remote access.
##📥 1️⃣ Clone the Repository
First, download the project from GitHub:
```bash
git clone https://github.com/your_user/Developer_Sandro_Casanova_Pol_Cerrillo_UF2_m09.git
cd Developer_Sandro_Casanova_Pol_Cerrillo_UF2_m09
```
##🏗️ 2️⃣ Build the Docker Image
Run the following command to create the Docker image with Flask and SSH:
```bash
docker build -t polcerrillo/flask-app .
```
##🚀 3️⃣ Run the Container
Now, start the container with the appropriate exposed ports:
```bash
docker run -dit -p 5000:5000 -p 2222:22 --name flask-container polcerrillo/flask-app
```
###📌 Explanation of the parameters:

-dit → Keeps the container running in the background.
-p 5000:5000 → Exposes the Flask application on port 5000.
-p 2222:22 → Exposes the SSH server on port 2222.
--name flask-container → Assigns a name to the container.

##🌍 4️⃣ Access the Flask Application
Once the container is running, you can access the Flask application via your browser:
```bash
http://localhost:5000
```
If the container is running on a remote server, replace localhost with the server's IP.

##🔑 5️⃣ Connect to the Container via SSH
The container also includes an SSH server. You can connect to it using:
```bash
ssh root@localhost -p 2222
```
📌 Default password: developerpassword
⚠️ It is recommended to change this after the first login.

##📌 Notes
✅ Make sure you have Docker installed on your system.
✅ To stop the container, use:
```bash
docker stop flask-container
```
✅ To remove it completely:
```bash
docker rm flask-container
```
## DockerHub Public
[![Docker Hub](https://img.shields.io/badge/Docker%20Hub-0db7ed?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/polcerrillo/flask_sandro_casanova_pol_cerrillo_uf2_m09/tags)

###🔄 Your Flask application is now running in Docker! 🚀
