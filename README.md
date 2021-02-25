# Serve-a-static-page-with-nginx
Nginx is a reverse proxy application used very commonly. Create a new nginx image that serves  simple static web page(for example a web page that prints “Hello Farnoosh)
# Create a simple .html file to serve with nginx
Make sure you have an html file in your directory
# Create a Dockerfile
use nginx:stable as base image
FROM nginx:alpine
COPY . /usr/share/nginx/html
# Build the Docker Image for the HTML Server
#docker build -t html-server-image:v1 .
#to check: docker images
# Copy .html file in Dockerfile to correct path so nginx can serve it
# Run the Docker Container
#docker run -d -p 80:80 html-server-image:v1
# Test the Port with cURL
#curl localhost:80
# Example of index.html
```html
     <!DOCTYPE html>
                  <html>
                     <head>
                  <body>
                <p> Hello Farnoosh</p>
        </body>
    </head>
  </html>
```
