Docker is a platform to manage the lifecycle of your containers. It is just one tool among many in the container ecosystem, there are other containerisation platforms and tools such as podman, LXC/LXD, CRIO etc. 

The core technology behind docker is containerisation, which allows you to create lightweight and portable isolated environments where your applications can run easily anywhere with a container runtime.IN

# ⏰ Check it’s time for Containerisation?

1.  🤔 Do you need to run your app in different environment or on different operating system/hardware architectures?
2. 🚀 Do you want to easily move your application between different environments (e.g. from development to production)?
3. 🔒 Do you need to ensure that your application is isolated from other applications running on the same infrastructure with minimal system resource?
4. 🔒 Do you need to ensure that your application is isolated from other applications running on the same infrastructure?
5.  🔄 Do you need to ensure that your application runs consistently across different environments and configurations?
6. ⏰ Do you want to reduce the time and effort required to set up and manage your application environment?
7. ☁️ Do you need to ensure that your application can be easily and reliably deployed to cloud infrastructure, regardless of the cloud provider let to be AWS, Azure, Google Cloud, Digital Ocean, Heroku or anything else..
8. 💪 Do you need to ensure that your application is highly available and fault-tolerant?
9. 👥 Are planning to work as team for the project and scale your application in future?
10. 🆕 Do you want to be able to easily roll out updates or changes to your application?

These are some question you should ask yourself before containerising an app, there is no need to containerise everything. 💡

> Containerising stateful applications like databases, it is generally not recommended. This is because stateful applications typically require persistent data storage, which can be more challenging to manage within a containerised environment. Containers are designed to be stateless.
> 

# **🛠️ Prerequisites**

1. Linux
2. Basic knowledge of programming
3. Familiarity with command-line interface (CLI) and Git
4. Familiarity with cloud platforms
5. Understanding of networking and security

# 📥 **Installation and Setup**

## 🐧 Linux

```bash
curl https://get.docker.com | bash
```

## 🪟 Windows

[https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)

## 🍎 Mac

[https://docs.docker.com/desktop/install/mac-install/](https://docs.docker.com/desktop/install/mac-install/)

# **💡 Learning Session**

## 1. How **docker works?**

### **🎓 Topics to Learn**

1. Basic idea of containerisation technology
2. Containerisation vs Virtualisation
3. Networking, Sockets, Namespaces, Cgroups & Union FIlesystems (Optional)

### **🧑🏻‍💻 Learn from**

*📽️* Videos

[Working of Containers | IBM Technology](https://www.youtube.com/watch?v=0qotVMX-J5s)
[Docker Concepts | Engineer Man](https://www.youtube.com/watch?v=6aBsjT5HoGY)

[Container vs Virtual Machines | IBM Technology](https://youtu.be/cjXI-yxqGTI)

[What are containers made from? | Docker [⚠️ Long Video]](https://www.youtube.com/watch?v=sK5i-N34im8)

[Computer Networking Full Course | Kunal Kushwaha [⚠️ Long VIdeo]](https://youtu.be/IPvYjXCsTg8)

[Namespaces | KodeKloud](https://www.youtube.com/watch?v=j_UUnlVC2Ss)

[cgroups | Sysadmincasts Videos](https://youtu.be/NtK3poD_0X0)

[Union FIlesystem | Ryan Hay](https://youtu.be/hhQ6uc2bp2s)

*📄* Articles

[what-is-docker? | DevOps Cube](https://devopscube.com/what-is-docker/)

[Computer Networking | AWS](https://aws.amazon.com/what-is/computer-networking/)

## 2. 📦 Containerise and 🏃‍♀️run app using Docker

### 2.1 Create a Docker file

A [Dockerfile](https://docs.docker.com/engine/reference/builder/) is a simple text file that contains a list of commands that the Docker client calls while creating an image. It's a simple way to automate the image creation process.

```bash
FROM python:3.9-slim-buster
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["flask", "run", "--port=80"]
```

*📽️* Videos
[https://youtu.be/WmcdMiyqfZs](https://youtu.be/WmcdMiyqfZs)
🔖 Dockerfile Templates Repository
[https://github.com/devopshobbies/docker-templates](https://github.com/devopshobbies/docker-templates)

### 2.2 Build Docker Image

Read-only templates that contain the application code and dependencies required to run the application. Docker images are created using a Dockerfile. 

It allows developers to package their application along with its dependencies, libraries, and configurations into a single image. This image can then be easily shared and deployed on any machine that has Docker installed.

```bash
docker build -t website:1.0 .
```

**Note**: Dockerfile should be named **`Dockerfile`**, and it should be located in the current directory.

### 2.3 Push to Container Registry(Optional)

A container registry is similar to a container repository, in that it allows us to push code like we would with version control systems such as Github. Docker Hub is one of the most popular container registries.

**Note:** If you are using GitHub, I recommend using the GitHub Container Registry. It can be easily integrated with GitHub Actions, making it easier to build your DevOps pipeline.

```bash
docker image tag <app name>:latest <registry host>/<repository name>/<app name>:<version>
docker image tag website:1.0 ghcr.io/user-name/website:1.0
```

```bash
docker push <registry host>/<repository name>/<app name>:<version>
docker push website:1.0
```

*📽️* Videos
[Container Registry Explained](https://www.youtube.com/watch?v=76rX4s73MrM)

*📄* Articles

[How to Publish a Docker Image to GitHub's Container Registry?](https://dev.to/github/publishing-a-docker-image-to-githubs-container-repository-4n50)
[Push container images to AWS container registry](https://docs.aws.amazon.com/AmazonECR/latest/userguide/docker-push-ecr-image.html)

[Push container images to Azure](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-get-started-azure-cli)

[Push container to Google Cloud Container Registry](https://cloud.google.com/container-registry/docs/pushing-and-pulling)

[Push container images to Digital Ocean Container Registry](https://docs.digitalocean.com/products/container-registry/how-to/set-up-ci-cd/)

[Push container images to Heroku](https://devcenter.heroku.com/articles/container-registry-and-runtime)

### 2.4 Pull from Container Registry(Optional)

Note: This step is required if you want to run someone's image or an image you pushed on your computer or another platform. 

It is not necessary to pull from the registry; you can take the build from the Dockerfile and run the created image. However, this is not the best practice and can take time to build.

```bash
docker pull <registry host>/<repository name>/<app name>:<version>
```

```bash
docker pull website:1.0
```

### 2.5 Run Container

```bash
docker run -d <registry host>/<repository name>/<app name>:<version>
# My app needs to listen on port 80(-p) and run in the background(-d).
docker run -d -p 80:80 website:1.0
```

*📽️* Videos

[Running Containers | Learn Linux TV](https://www.youtube.com/watch?v=VevE65N3BOs)

*📄* Articles

[Run Docker Containers | Linux Handbook](https://linuxhandbook.com/run-docker-container/)

### 2.6 Check running Containers

You can check the running containers with “docker ps” command

```bash
docker ps
```

*📽️* Videos

[Docker lifecycle and PS command | Hitesh Choudhary](https://youtu.be/HH02ex0r4Ow)

*📄* Articles

[Examples of the Docker ps Command | Linux handbook](https://linuxhandbook.com/docker-ps-command/)

> You can run a multi-container application in a single file using Docker Compose, which is a simple orchestration tool.
> 

## Projects you need try

1. [Run a static website using nginx in container](https://typeofnan.dev/how-to-serve-a-static-app-with-nginx-in-docker/)
2. [Containerise and run a stateless flask app](https://www.freecodecamp.org/news/how-to-dockerize-a-flask-app/)
3. ****[Build and Dockerize a Full-stack React app with Node.js, MySQL and Nginx](https://www.section.io/engineering-education/build-and-dockerize-a-full-stack-react-app-with-nodejs-and-nginx/)****

## **🔖 Resource Pool**

[https://labs.play-with-docker.com](https://labs.play-with-docker.com/)

[https://awesome-docker.netlify.app/#docker-images](https://awesome-docker.netlify.app/#docker-images)

[https://www.youtube.com/watch?v=gAkwW2tuIqE](https://www.youtube.com/watch?v=gAkwW2tuIqE)

[https://www.youtube.com/watch?v=3c-iBn73dDE&pp=ygUGZG9ja2Vy](https://www.youtube.com/watch?v=3c-iBn73dDE&pp=ygUGZG9ja2Vy)

[https://www.youtube.com/watch?v=bKFMS5C4CG0](https://www.youtube.com/watch?v=bKFMS5C4CG0)

[https://www.youtube.com/watch?v=SIF9qQB_b_c](https://www.youtube.com/watch?v=SIF9qQB_b_c)

## **🚀 Project Pool**

[https://github.com/dockersamples](https://github.com/dockersamples)

[https://dev.to/ankit01oss/7-github-projects-to-supercharge-your-docker-practices-2i80](https://dev.to/ankit01oss/7-github-projects-to-supercharge-your-docker-practices-2i80)

## **🫂 Communities (Optional)**

[https://community.cncf.io/kochi/](https://community.cncf.io/kochi/)
