# TASK-1 DAY-1

#  Node.js CI/CD Pipeline Demo using GitHub Actions & Docker

This is a simple **Node.js web application** built using Express.js.  
It demonstrates how to automate the process of building and deploying Docker containers using **GitHub Actions CI/CD pipeline**.


---


## Tools Used

- **Node.js** with Express
- **Docker** for containerization
- **GitHub Actions** for CI/CD automation
- **DockerHub** to host built images

---

## What I Did

- Created a simple Express.js server
- Wrote a `Dockerfile` to containerize the app
- Set up `.github/workflows/main.yml` for CI/CD pipeline
- Stored DockerHub credentials in GitHub Secrets
- Changed the branch name into master into main 
- On every push to the `master` branch:
- GitHub Actions builds the Docker image 
- Tags it with the branch name
- Pushes it to DockerHub automatically 

---

## GitHub Secrets Required

- `DOCKER_USERNAME` – Your DockerHub username
- `DOCKER_PASSWORD` – Your DockerHub password or access token

---

##  Run Locally Using Docker

You can pull the image from DockerHub and run it:

```bash
docker pull srilakshmiyannam/nodejs-demo-app:master
docker run -p 3000:3000 srilakshmiyannam/nodejs-demo-app:master


# Then visit: http://localhost:3000


