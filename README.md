# Resume Matcher – Docker Build & Deployment

Containerized 3 Tier React.js Resume Matcher app.

## 📺 Walkthrough
[![Docker Build & Deployment Walkthrough](https://youtube.com)](https://youtube.com)


---

## 🐳 Multi-stage Dockerfile
The Dockerfile uses a **multi-stage build**:

- Stage 1: Builder (Alpine) – Node.js 20 Alpine, installs build tools and libraries.  
- Stage 2: Runtime (Debian Slim) – Node.js 20 Slim, copies built output, exposes port 3000.

<div align="center">
  <img src="images/docker/Dockerfile/dockerfile1.png" width="400"/>
  <img src="images/docker/Dockerfile/dockerfile2.png" width="400"/>
</div>

---

## 📂 .dockerignore
The `.dockerignore` file excludes unnecessary files to keep the build context small.

<div align="center">
  <img src="images/docker/Dockerignore/dockerignore1.png" width="400"/>
  <img src="images/docker/Dockerignore/dockerignore2.png" width="400"/>
</div>

---

## ⚙️ Docker Compose
The `docker-compose.yml` orchestrates a three-service stack: web, db, nginx.

<div align="center">
  <img src="images/docker/Dockercompose/dockercompose1.png" width="400"/>
  <img src="images/docker/Dockercompose/dockercompose2.png" width="400"/>
</div>

---

## 🚀 Containers are Running
Built and started containers with:

docker-compose up --build
docker-compose up

Verified container startup, healthchecks, logs, and exposed ports.

<div align="center">
<img src="images/docker/Containerrunning/containerrunning1.png" width="300"/>
<img src="images/docker/Containerrunning/containerrunning2.png" width="300"/>
<img src="images/docker/Containerrunning/containerrunning3.png" width="300"/>
<img src="images/docker/Containerrunning/containerrunning4.png" width="300"/>
<img src="images/docker/Containerrunning/containerrunning5.png" width="300"/>
<img src="images/docker/Containerrunning/containerrunning6.png" width="300"/>
</div>

---

## 📝 Notes

Multi-stage builds keep images small.

Alpine vs Debian Slim trade-offs.

Healthchecks ensure service readiness.




