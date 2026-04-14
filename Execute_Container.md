1. Execute hello-world
   ```bash
    hkim9771852@c4r10s1 ~ % docker run hello-world
   ```
   ```bash
    Output:
        Unable to find image 'hello-world:latest' locally
        latest: Pulling from library/hello-world
        4f55086f7dd0: Pull complete 
        Digest: sha256:452a468a4bf985040037cb6d5392410206e47db9bf5b7278d281f94d1c2d0931
        Status: Downloaded newer image for hello-world:latest
        
        Hello from Docker!
        This message shows that your installation appears to be working correctly.
        
        To generate this message, Docker took the following steps:
         1. The Docker client contacted the Docker daemon.
         2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
            (amd64)
         3. The Docker daemon created a new container from that image which runs the
            executable that produces the output you are currently reading.
         4. The Docker daemon streamed that output to the Docker client, which sent it
            to your terminal.
        
        To try something more ambitious, you can run an Ubuntu container with:
         $ docker run -it ubuntu bash
        
        Share images, automate workflows, and more with a free Docker ID:
         https://hub.docker.com/
        
        For more examples and ideas, visit:
         https://docs.docker.com/get-started/
   ```
3. Check images
  ```bash
  hkim9771852@c4r10s1 ~ % docker images
  REPOSITORY    TAG       IMAGE ID       CREATED       SIZE
hello-world   latest    e2ac70e7319a   2 weeks ago   10.1kB
  ```

5. Running an Ubuntu container
   ```bash
   hkim9771852@c4r10s1 ~ % docker run -it ubuntu bash
   Meaning: docker run- start a new container, -it- open the container,
            ubuntu - use the ubuntu image, bash - start a bash shell inside the container
   ```
   ```bash
   Output:
       Unable to find image 'ubuntu:latest' locally
      latest: Pulling from library/ubuntu
      689b91d88a0f: Pull complete 
      Digest: sha256:84e77dee7d1bc93fb029a45e3c6cb9d8aa4831ccfcc7103d36e876938d28895b
      Status: Downloaded newer image for ubuntu:latest

      root@dc1a8f2c3a5a:/# ls (list files and directories in the current directory)
      bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
      boot  etc  lib   media  opt  root  sbin  sys  usr
   ```
   ```bash

      hkim9771852@c4r10s1 ~ % docker run -dit --name my-ubuntu ubuntu sleep 300
      Explanation: Runs detached mode of container in the background
      Output: b75f7738e579cb7932b74fbf54d17880ffe487e1d513cb4b06b7326397eed086
   ```
   ```bash

      hkim9771852@c4r10s1 ~ % docker ps
      CONTAINER ID   IMAGE     COMMAND       CREATED         STATUS         PORTS     NAMES
      b75f7738e579   ubuntu    "sleep 300"   2 minutes ago   Up 2 minutes             my-ubuntu
   ```
   ```bash

      hkim9771852@c4r10s1 ~ % docker exec -it my-ubuntu bash
      Explanation: Opens a bash shell inside the container(can run Linux command)
   ```
   ```bash

      hkim9771852@c4r10s1 ~ % docker run -it --name test ubuntu bash
      root@00a13ce8fe54:/# echo "test-exit"
      test-exit
      root@00a13ce8fe54:/# exit
      exit

      hkim9771852@c4r10s1 ~ % docker ps -a
      CONTAINER ID   IMAGE         COMMAND                  CREATED          STATUS                      PORTS     NAMES
      00a13ce8fe54   ubuntu        "bash"                   29 seconds ago   Exited (0) 12 seconds ago             test
      2a475d15d4a0   ubuntu        "sleep 300"              2 minutes ago    Up 2 minutes                       ubuntu2
   ```
