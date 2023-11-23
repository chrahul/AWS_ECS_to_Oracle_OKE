Certainly! Below is the same information formatted in Markdown for use in a GitHub README or any Markdown file:

```markdown
# Custom Nginx Docker Image

This Dockerfile example uses the official Nginx image to create a container serving a custom static web page.

## Dockerfile

```Dockerfile
# Use the official Nginx image as the base image
FROM nginx:latest

# Copy the custom HTML file to the Nginx default HTML directory
COPY custom-index.html /usr/share/nginx/html/index.html

# Expose port 80 for incoming traffic
EXPOSE 80

# The CMD instruction sets the default command for the container
CMD ["nginx", "-g", "daemon off;"]
```

## Custom HTML File (`custom-index.html`)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Custom Static Web Page</title>
</head>
<body>
    <h1>Hello, this is a custom static web page!</h1>
</body>
</html>
```

## Building the Docker Image

To build the Docker image, save the Dockerfile and the custom HTML file in the same directory, and run the following command in the terminal:

```bash
docker build -t custom-nginx .
```

Replace `custom-nginx` with your preferred image name.

## Running the Docker Container

After building the image, you can run a container using the following command:

```bash
docker run -p 8080:80 custom-nginx
```

Now, you should be able to access your custom static web page by navigating to `http://localhost:8080` in your web browser.
```

Copy and paste this Markdown content into your README.md or any other Markdown file in your GitHub repository.
