# 🐳 Go Dockerized Application

A simple **Go web server** containerized using Docker for easy deployment.
The server listens on **port 8080** and responds with a greeting message.

---

## 📁 Project Structure

```
go-app/                 
├── Dockerfile           # Multi-stage Docker build
├── go.mod               # Go module file
├── main.go              # Go source code
└── README.md            # Project documentation
```

---

## 💻 Application Code

```go
package main

import (
	"fmt"
	"log"
	"net/http"
)

// handler responds to HTTP requests with a greeting message
func handler(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintln(w, "Hello from My Go Docker App!")
}

func main() {
	http.HandleFunc("/", handler)      // Set handler for root route
	port := ":8080"
	fmt.Println("Server is running on port", port)
	log.Fatal(http.ListenAndServe(port, nil)) // Start HTTP server
}
```

> ✅ This Go web server handles **GET /** requests and prints a greeting message.
> It can run locally or inside a Docker container.

---

## 🚀 Running Locally

1. Clone the repository:

```bash
git clone https://github.com/ahmed-elshenawii/go-app.git
cd go-app
```

2. Run the application:

```bash
go run main.go
```

3. Open your browser:

```
http://localhost:8080
```

---

## 🐳 Running with Docker

1. Build the Docker image:

```bash
docker build -t ahmedelshenawy1/go-app:latest .
```

2. Run the container and map port 8080:

```bash
docker run -p 8080:8080 ahmedelshenawy1/go-app:latest
```

3. Open in browser:

```
http://localhost:8080
```

---

## 📦 Docker Hub Image

* Public Image: [https://hub.docker.com/r/ahmedelshenawy1/go-app](https://hub.docker.com/r/ahmedelshenawy1/go-app)

* Pull directly:

```bash
docker pull ahmedelshenawy1/go-app:latest
```

---

## 📌 Submission Links

* **GitHub Repository**: [https://github.com/ahmed-elshenawii/go-app](https://github.com/ahmed-elshenawii/go-app)
* **Docker Hub Image**: [https://hub.docker.com/r/ahmedelshenawy1/go-app](https://hub.docker.com/r/ahmedelshenawy1/go-app)
