Bind mount: lets you change the container instantly whenever you change a file on your Mac
1. Write a first message on my website:
   a. Build a home for my website
        hkim9771852@c4r8s1 ~ % mkdir -p website_files
   b. Write a message in it
       hkim9771852@c4r8s1 ~ % echo '<h1>Finally Success!</h1>' > website_files/index.html
   c. Map the message to the portal
       hkim9771852@c4r9s3 ~ % docker run -d \
      -p 8080:80 \
      --name my-bind-server \
      -v /Users/hkim9771852/website_files:/usr/share/nginx/html \
      nginx:alpine
   d. execute it on the server
      hkim9771852@c4r9s3 ~ % exec my-bind-server ls /usr/share/nginx/html
      Output: index.html
2. Change the first message on my website:
  a. remove old container(old message by force)
     hkim9771852@c4r8s1 ~ % docker rm -f my-bind-server
  b. repeat part (b) to part (d) from step 1(change the message) 
  c. Refresh the page of the website!


6. Before changing the container:
   Message on the website: Finally Success!


7. After changing the container:
   Message on the website: Execution of Bind Mount: success!
