Here is the GitHub Markdown file for the experiment:

```markdown
# **Experiment No.: 7**

## **Aim**
Develop a simple containerized application using Docker.

---

## **Description**
This experiment demonstrates how to containerize a simple Python application using Docker. The application is a Python script that prints "Hello World." We will create a Docker image for this application, run it in a container, and verify the output.

---

## **Steps to Implement**

### 1. **Choose an Application**
We will create a Python script `hello.py` that prints `Hello World`.

### 2. **Write the Python Script**
Create a file named `hello.py` with the following content:


```
# hello.py
print("Hello World")
```

### 3. **Write a Dockerfile**
Create a file named `Dockerfile` in the same directory as `hello.py` with the following content:

```dockerfile
# Use the official Python image as the base image
FROM python:3.9

# Copy the Python script into the container
COPY hello.py /app/

# Set the working directory to /app
WORKDIR /app

# Run the Python script when the container starts
CMD ["python", "hello.py"]
```

### 4. **Build the Docker Image**
Run the following command in the terminal to build the Docker image:

```bash
docker build -t myimage .
```

- `-t myimage` tags the image with the name `myimage`.
- `.` specifies the current directory as the build context.

### 5. **Run the Docker Container**
Run the container using the following command:

```bash
docker run --name mycontainer myimage
```

- `--name mycontainer` gives the container a name for easy identification.
- `myimage` is the image created in the previous step.

### 6. **Verify the Output**
Check the logs of the container to verify the output:

```bash
docker logs mycontainer
```

The logs should display:

```
Hello World
```

---

## **Experiment Summary**
This experiment covered the following:
1. Writing a basic Python script.
2. Creating a `Dockerfile` to containerize the application.
3. Building a Docker image and running it as a container.
4. Verifying the container's output using Docker logs.

This simple example provides a foundation for understanding Docker's core concepts and prepares for more complex applications involving multi-container setups, networking, and data persistence.

---

## **Files**
1. `hello.py` - The Python application.
2. `Dockerfile` - The configuration file to build the Docker image.

---

## **Commands Summary**
1. Build the Docker image:
    ```bash
    docker build -t myimage .
    ```

2. Run the Docker container:
    ```bash
    docker run --name mycontainer myimage
    ```

3. View container logs:
    ```bash
    docker logs mycontainer
    ```

---

## **Output**
When the container runs successfully, the following output is displayed:

```
Hello World
```
```
