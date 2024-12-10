---

# Simple Web App with Docker

This project demonstrates how to containerize a simple web application with HTML, CSS, and a Dockerfile using the Nginx web server.

---

## Features
- Static web app with **HTML**, **CSS**, and a **GIF**.
- Dockerized using **Nginx** for efficient serving of static content.
- Lightweight image built with `nginx:alpine`.

---

## Prerequisites
- **Docker** installed on your system.
- Basic understanding of Docker commands.

---

## Project Structure
```
.
├── Dockerfile        # Docker configuration file
├── index.html        # HTML file for the web app
├── style.css         # CSS file for styling
├── docker.gif        # GIF used in the web app
```

---

## Dockerfile
```dockerfile
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/
COPY style.css /usr/share/nginx/html/
COPY docker.gif /usr/share/nginx/html/

```

---

## Usage

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Build the Docker Image
```bash
docker build -t simple-web-app .
```

### 3. Run the Docker Container
```bash
docker run -d -p 8080:80 simple-web-app
```

### 4. Access the Web App
Open your browser and visit:
```
http://localhost:8080
```

---

## Stopping the Container
To stop the container, find its ID using:
```bash
docker ps
```
Then stop it:
```bash
docker stop <container-id>
```

---

## Cleaning Up
### Remove the Container
```bash
docker rm <container-id>
```

### Remove the Image
```bash
docker rmi simple-web-app
```

---

## Example Web App Preview
This app displays a simple page styled with CSS and an embedded GIF.

---

## License
This project is licensed under the [MIT License](LICENSE).

---
