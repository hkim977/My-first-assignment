1. Pull an image from a web-server
   ```bash
   hkim9771852@c4r8s1 ~ % echo "FROM nginx:alpine" > Dockerfile
   nginx:program
   ```
3. Create a new container image
```bash
hkim9771852@c4r8s1 ~ % docker build -t my-web .
  Breakdown: docker build - start creating a new container image
             -t - short for tag, gives image a friendly name
             my-web: name of my image
             . : tells Docker to look for the Dockerfile in the current directory
  Summary: build an image called my-web using a Dockerfile located in this folder.
Output:
   => [internal] load build definition from Dockerfile                       0.1s
   => => transferring dockerfile: 49B                                        0.0s
   => [internal] load metadata for docker.io/library/alpine:latest           2.6s
   => [internal] load .dockerignore                                          0.1s
   => => transferring context: 2B                                            0.0s
   => [1/1] FROM docker.io/library/alpine:latest@sha256:25109184c71bdad752c  1.0s
   => => resolve docker.io/library/alpine:latest@sha256:25109184c71bdad752c  0.1s
   => => sha256:25109184c71bdad752c8312a8623239686a9a2071e8 9.22kB / 9.22kB  0.0s
   => => sha256:59855d3dceb3ae53991193bd03301e082b2a7faa56a 1.02kB / 1.02kB  0.0s
   => => sha256:a40c03cbb81c59bfb0e0887ab0b1859727075da7b9cc576 611B / 611B  0.0s
   => => sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6 3.86MB / 3.86MB  0.6s
   => => extracting sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8  0.1s
   => exporting to image                                                     0.0s
   => => exporting layers                                                    0.0s
   => => writing image sha256:a40c03cbb81c59bfb0e0887ab0b1859727075da7b9cc5  0.0s
   => => naming to docker.io/library/my-web                                  0.0s
```

5. Connect my computer's port to the container's port
   ```bash
   hkim9771852@c4r8s1 ~ % docker run -p 8080:80 --name my-running-app my-web
   62320af1313a404d3ccd72568976a6563b934739c8c4f22bdc81752c7bfd206f
   What the code does: Telling Docker this: "Take the 'my-web' app I just built, give it a cool nickname,
   run it in the background so it doesn't clutter my screen, and open a 'tunnel' so I can visit it in my browser.
   Code breakdown:
       docker run: Pushing the start button
       Port 8080: Front door of my building
       Port 80(container): room inside the building
       --name my-running-app: give my running app a nickname
   ```
  ```bash
  Output: 
       /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
      /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
      /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
      10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
      10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
      /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
      /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
      /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
      /docker-entrypoint.sh: Configuration complete; ready for start up
      2026/04/10 10:39:19 [notice] 1#1: using the "epoll" event method
      2026/04/10 10:39:19 [notice] 1#1: nginx/1.29.8
      2026/04/10 10:39:19 [notice] 1#1: built by gcc 15.2.0 (Alpine 15.2.0) 
      2026/04/10 10:39:19 [notice] 1#1: OS: Linux 6.17.8-orbstack-00308-g8f9c941121b1
      2026/04/10 10:39:19 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 20480:1048576
      2026/04/10 10:39:19 [notice] 1#1: start worker processes
      2026/04/10 10:39:19 [notice] 1#1: start worker process 30
      2026/04/10 10:39:19 [notice] 1#1: start worker process 31
      2026/04/10 10:39:19 [notice] 1#1: start worker process 32
      2026/04/10 10:39:19 [notice] 1#1: start worker process 33
      2026/04/10 10:39:19 [notice] 1#1: start worker process 34
      2026/04/10 10:39:19 [notice] 1#1: start worker process 35
```
7. Check web-server(via the website)
   Method: Type http://localhost:8080 in safari
   Result: Welcome to nginx!
          If you see this page, nginx is successfully installed and working. 
          Further configuration is required for the web server, reverse proxy, 
          API gateway, load balancer, content cache, or other features.
          
          For online documentation and support please refer to nginx.org.
          To engage with the community please visit community.nginx.org.
          For enterprise grade support, professional services, additional security features 
          and capabilities please refer to f5.com/nginx.
    
          Thank you for using nginx.
      


