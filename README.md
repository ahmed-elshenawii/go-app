📌 Go Dockerized Application

This project is a simple Go web server containerized using Docker.
The application listens on port 8080 and returns a greeting message.

It includes:

main.go — The Go source code

go.mod — Dependency/module configuration

Dockerfile — Multi-stage Docker build

Full instructions to build, run, and push the Docker image

Public Docker Hub image link

🏗 Project Structure
.
├── main.go
├── go.mod
├── Dockerfile
└── README.md

🚀 Application Behavior

The server responds to requests on:

GET /


Response:

Hello from My Go Docker App!

🐳 Docker Image

Public image on Docker Hub:

👉 https://hub.docker.com/r/ahmedelshenawy1/go-app

To pull the image:

docker pull ahmedelshenawy1/go-app:latest

🔧 Build the Docker Image Locally

Build using Docker:

docker build -t go-app .


Or build with your Docker Hub tag:

docker build -t ahmedelshenawy1/go-app:latest .

▶ Run the Application in Docker

Run the container:

docker run -p 8080:8080 ahmedelshenawy1/go-app:latest


Then open your browser and visit:

http://localhost:8080


Expected output:

Hello from My Go Docker App!

📤 Push the Image to Docker Hub

Make sure you're logged in:

docker login


Then push:

docker push ahmedelshenawy1/go-app:latest
