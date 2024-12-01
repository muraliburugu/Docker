Here’s the complete setup with proper instructions, file contents, and structure.

---

# **Experiment No.: 7**

## **Aim**
Develop a simple containerized application using Docker.

---

## **Description**
In this experiment, we will create a simple Python application that prints `Hello World` and containerize it using Docker. The steps include writing the Python script, creating a `Dockerfile`, building a Docker image, running the container, and verifying the output.

---

## **Project Structure**
The project directory should have the following structure:

```
python-project/
├── Dockerfile
└── hello.py
```

---

## **Steps to Implement**

### **1. Write the Python Script**

Create a file named `hello.py` with the following content:

```python
# hello.py
# This script prints a simple message to the console

print("Hello World")
```

---

### **2. Write the Dockerfile**

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

---

### **3. Build the Docker Image**

Run the following command in the terminal to build the Docker image:

```bash
docker build -t myimage .
```

- `-t myimage`: Tags the image with the name `myimage`.
- `.`: Specifies the current directory as the build context.

---

### **4. Run the Docker Container**

Start the container with the following command:

```bash
docker run --name mycontainer myimage
```

- `--name mycontainer`: Names the container `mycontainer`.
- `myimage`: Refers to the image created in the previous step.

---

### **5. Verify the Output**

To verify the output, check the container logs using:

```bash
docker logs mycontainer
```

You should see the following output:

```
Hello World
```

---



## **Summary**

This experiment demonstrated:
1. Writing a simple Python application.
2. Creating a `Dockerfile` to define a containerized environment.
3. Building a Docker image.
4. Running the application in a container.
5. Verifying the output.

This lays the groundwork for containerizing more complex applications and deploying them efficiently.
