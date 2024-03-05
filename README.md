# Running a Python app using Docker

- Step 1: Install Docker
- Step 2: Create a Dockerfile
- Step 3: Build Docker Image
- Step 4: Run Docker Container

--- 

### 1. Create a Dockerfile
  
```
# Use a slim Python 3.9 image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any dependencies
RUN pip install -r requirements.txt

# Define environment variable
ENV NAME World

# Command to run the application
CMD ["python", "app.py"]

```

## 2. Build Docker Image

```
docker build -t my_image_name .
```

## 3. Run Docker Container

```
docker run my-python-app
```


---

# Running linux shell using Docker

- Step 1: Create a Dockerfile
- Step 2: Build Docker Image
- Step 3: Run Docker Container
  
--- 

### Step 1. Create a Dockerfile

```
FROM ubuntu:latest

# Set working directory
WORKDIR /app

CMD ["bash"]

```

### Step 2. Build Docker Image

```
docker build -t my_image_name .
```

### Step 3. Run Docker Container

```
docker run -it my-bash-image
```
---
## More Commands

```
# To list all Docker images

docker images

# To list all running Docker containers

docker ps

# To stop a running container

docker stop <container_id_or_name>

# To remove a container

docker rm <container_id_or_name>

# To remove an image

docker rmi <image_id_or_name>

```
