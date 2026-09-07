\# CodeAlpha Web Server using Docker



\## Project Overview



This project demonstrates how to deploy and manage a web server inside a Docker container using Nginx.



A custom HTML webpage is served through Nginx, which runs inside a Docker container.



This project was completed as part of the CodeAlpha DevOps Internship.



\## Task



\*CodeAlpha DevOps Internship — Task 4: Web Server using Docker\*



\## Objectives



\- Learn Docker containerization basics

\- Deploy a web server inside a Docker container

\- Manage the Docker container lifecycle

\- Monitor the container status and logs

\- Troubleshoot basic container issues

\- Build a custom Docker image

\- Serve a custom webpage using Nginx



\## Technologies Used



\- Docker

\- Nginx

\- HTML

\- Git

\- GitHub



\## Project Structure



```text

CodeAlpha\_WebServer\_Docker/

│

├── Dockerfile

├── index.html

└── README.md

```



\## Dockerfile



The project uses the official Nginx Docker image as the base image.



The custom `index.html` file is copied into the default Nginx web directory.



```dockerfile

FROM nginx:latest



COPY index.html /usr/share/nginx/html/index.html



EXPOSE 80

```



\## Build the Docker Image



Run the following command from the project directory:



```bash

docker build -t codealpha-web-server .

```



This creates a Docker image named `codealpha-web-server`.



\## Run the Docker Container



Run the following command:



```bash

docker run -d -p 8080:80 --name codealpha-web-server codealpha-web-server

```



The container runs Nginx in the background.



\### Port Mapping



```text

Host Port 8080 → Container Port 80

```



\## Access the Web Server



Open a web browser and visit:



```text

http://localhost:8080

```



The custom CodeAlpha webpage will be displayed.



\## Docker Container Management



\### Check Running Containers



```bash

docker ps

```



\### Stop the Container



```bash

docker stop codealpha-web-server

```



\### Start the Container



```bash

docker start codealpha-web-server

```



\### Restart the Container



```bash

docker restart codealpha-web-server

```



\### View Container Logs



```bash

docker logs codealpha-web-server

```



\### Check Container Status



```bash

docker inspect --format="{{.State.Status}}" codealpha-web-server

```



A successfully running container returns:



```text

running

```



\## Testing and Verification



The Docker container was successfully started and verified using:



```bash

docker ps

```



The Nginx web server was accessed through:



```text

http://localhost:8080

```



The custom webpage was successfully displayed in the browser.



Container logs were checked using:



```bash

docker logs codealpha-web-server

```



The logs confirmed that Nginx started successfully and processed HTTP requests.



\## Result



The web server was successfully deployed inside a Docker container using Nginx.



The custom webpage is accessible through:



```text

http://localhost:8080

```



\## Conclusion



This project provided practical experience with Docker containerization, Nginx web server deployment, Docker image creation, container lifecycle management, logging, monitoring, and basic troubleshooting.



The project demonstrates a simple containerized web server deployment following basic DevOps practices.



\## Author



\*Muhammad Abubakar\*



\## Internship



\*CodeAlpha DevOps Internship\*



