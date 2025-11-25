# 🐳 Go Dockerized Application

This is a simple **Go web server** containerized using Docker for easy deployment. The server listens on **port 8080** and responds with a greeting message.

## Project Structure

```
go-app/                 # Root folder
├── Dockerfile           # Multi-stage Docker build
├── go.mod               # Go module file
├── main.go              # Go source code
└── README.md            # Documentation
```

## Application Code

```go
package main

import (
	"fmt"
	"log"
	"net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintln(w, "Hello from My Go Docker App!")
}

func main() {
	http.HandleFunc("/", handler)
	port := ":8080"
	fmt.Println("Server is running on port", port)
	log.Fatal(http.ListenAndServe(port, nil))
}
```

## How It Works

* Handles **GET /** requests
* Sends the message: `Hello from My Go Docker App!`
* Runs locally or inside Docker container

## Running Locally

```bash
git clone https://github.com/ahmed-elshenawii/go-app.git
cd go-app
go run main.go
```

* Open in browser: `http://localhost:8080`

## Running with Docker

```bash
docker build -t ahmedelshenawy1/go-app:latest .
docker run -p 8080:8080 ahmedelshenawy1/go-app:latest
```

* Access in browser: `http://localhost:8080`

## Docker Hub Image

* Public Image: [Docker Hub Link](https://hub.docker.com/r/ahmedelshenawy1/go-app)
* Pull it directly:

```bash
docker pull ahmedelshenawy1/go-app:latest
```

## Submission Links

* **GitHub Repository**: [https://github.com/ahmed-elshenawii/go-app](https://github.com/ahmed-elshenawii/go-app)
* **Docker Hub Image**: [https://hub.docker.com/r/ahmedelshenawy1/go-app](https://hub.docker.com/r/ahmedelshenawy1/go-app)
