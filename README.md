This exercise covers:

* Directory navigation (`pwd`, `cd`)
* File and directory management (`mkdir`, `touch`, `cp`, `mv`, `rm`)
* File content manipulation (`echo`, `cat`)
* File inspection (`ls -la`)
  
## 1. Check Current Directory
Code: pwd
**Description:**
Prints the current working directory.
**Output:**
/Users/hkim9771852
__________________________________________
## 2. List Directory Contents
Code: ls -la
**Description:**
Lists all files and directories (including hidden ones) in long format, showing permissions, ownership, size, and timestamps.
**Output:**
total 16
drwxr-x---+ 20 hkim9771852  hkim9771852   640 Apr  3 18:55 .
drwxr-xr-x  11 root         admin         352 Apr  3 18:15 ..
-r--------   1 hkim9771852  hkim9771852     7 Apr  3 18:15 .CFUserTextEncoding
drwx------+  2 hkim9771852  hkim9771852    64 Apr  3 18:16 .Trash
drwxr-xr-x   5 hkim9771852  hkim9771852   160 Apr  3 18:16 .docker
drwxr-xr-x  10 hkim9771852  hkim9771852   320 Apr  3 18:55 .orbstack
drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  3 18:16 .ssh
drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  3 18:16 .vscode
-rw-------   1 hkim9771852  hkim9771852    44 Apr  3 18:54 .zsh_history
drwx------   6 hkim9771852  hkim9771852   192 Apr  3 18:55 .zsh_sessions
drwx------@  4 hkim9771852  hkim9771852   128 Apr  3 18:44 Applications
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Desktop
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Documents
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Downloads
drwx------@ 80 hkim9771852  hkim9771852  2560 Apr  3 18:39 Library
drwx------   3 hkim9771852  hkim9771852    96 Apr  3 18:15 Movies
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Music
drwx------   4 hkim9771852  hkim9771852   160 Apr  3 18:55 OrbStack
drwx------+  4 hkim9771852  hkim9771852   128 Apr  3 18:16 Pictures
drwxr-xr-x+  4 hkim9771852  hkim9771852   128 Apr  3 18:15 Public
________________________________________________
## 3. Create a New Directory
Code: mkdir dictation
**Description:**
Creates a new directory named `dictation`.
_______________________________________________
## 4. Navigate into Directory
Code: cd dictation
**Description:**
Changes the current working directory to `dictation`.
________________________________________________________
## 5. Create a New File
Code: touch Baking.txt
**Description:**
Creates an empty file named `Baking.txt`.
_______________________________________________________
## 6. Write Content to File
Code: echo "Hello"> Baking.txt
**Description:**
Writes the text `"Hello"` into `Baking.txt`.
* If the file already exists, it will be overwritten.
_____________________________________________________
## 7. Display File Contents
Code: cat Baking.txt
**Description:**
Displays the contents of `Baking.txt`.
**Output:**
Hello
_____________________________________________________
## 8. Copy a File
Code: cp Baking.txt Baking-copy.txt
**Description:**
Creates a copy of `Baking.txt` named `Baking-copy.txt`.
_____________________________________________________
## 9. Rename a File
Code: mv Baking-copy.txt Baking-renamed.txt
**Description:**
Renames `Baking-copy.txt` as `Baking-renamed.txt`.
____________________________________________________
## 10. Delete a File
code: rm Baking-renamed.txt
**Description:**
Deletes the file named `Baking-renamed.txt`.
____________________________________________________
## 11. Verify Final Directory Contents
Code: ls -la
**Description:**
Confirms the remaining files in the directory.
**Output:**
total 0
drwxrwxrwx 1 root root 4096 Apr  6 23:08 .
drwxrwxrwx 1 root root 4096 Apr  6 23:07 ..
-rwxrwxrwx 1 root root    6 Apr  6 23:08 Baking.txt
drwxrwxrwx 1 root root 4096 Apr  2 23:54 notes
_______________________________________________________
## 12. Testing permission
Step 1: Create one file and one directory
Code: cd /tmp
      touch firstfile.txt
      mkdir firstfolder
**Description:**
Creates one file and one directory for testing permission

Step 2: Check permissions before changing them
Code: ls -l
**Description:**
This command shows current permissions
**Output:**
-rwxrwxrwx 1 root root    6 Apr  6 23:08 Baking.txt
-rwxrwxrwx 1 root root    0 Apr  6 23:13 firstfile.txt
drwxrwxrwx 1 root root 4096 Apr  6 23:13 firstfolder
drwxrwxrwx 1 root root 4096 Apr  2 23:54 notes

Step 3: Change permissions
Code: chmod 600 firstfile.txt
      chmod 700 firstfolder
**Description:**
   600 means only owner can read/write file
   700 means only owner can access directory

Step 4: Check permissions after changing them
Code: ls -l
**Description:**
This command shows updated permissions
**Output:**
-rw------- 1 hyun_jee_kim hyun_jee_kim    0 Apr  6 23:31 firstfile.txt
drwx------ 2 hyun_jee_kim hyun_jee_kim 4096 Apr  6 23:31 firstfolder
_________________________________________________________________
## 13. Docker
   a. check version of Docker:
      Code: docker --version
      **Description:**
      This command confirms whether the docker is installed or not
      **Output:**
      Docker version 29.3.1, build c2be9cc
  b. check Docker info:
     Code: docker info
      **Description:**
      This command shows info of Docker
      **Output:**
      Client:
      Version:    29.3.1
      Context:    desktop-linux
      Debug Mode: false
      Plugins:
      agent: Docker AI Agent Runner (Docker Inc.)
      Version:  v1.34.0
      Path: C:\Program Files\Docker\cli-plugins\docker-agent.exe
  c. Docker Basic operations
      i) Check images
         Code: docker images
         **Description:**
         This command is used to create blueprint to make one or more Docker containers.
          **Output:**                                      
          IMAGE           ID             DISK USAGE   CONTENT SIZE   EXTRA
          docker/welcome-to-docker:latest
                          c4d56c24da4f       22.2MB         6.03MB    U
          python:latest   ffebef43892d       1.63GB          432MB    U
      ii) check running containers
          Code: docker ps
          **Description:**
          This command is used to check running containers
          **Output:** 
          CONTAINER ID   IMAGE     COMMAND     CREATED      STATUS         PORTS     NAMES
          531e1c33ad86   python    "python3"   3 days ago   Up 4 minutes             sad_tesla
      iii) check all containers
           Code: docker ps -a
           **Description:**
           This command is used to check all running containers
           **Output:** 
           CONTAINER ID   IMAGE                             COMMAND                   CREATED      STATUS                       PORTS                  NAMES
            531e1c33ad86   python                            "python3"                 3 days ago   Up 6 minutes                                        sad_tesla
            b48e95953001   python                            "python3"                 3 days ago   Exited (0) 3 days ago                               happy_poitras
            19e36c73244f   python                            "python3"                 3 days ago   Exited (255) 6 minutes ago                          awesome_taussig
            6401b5ca0638   docker/welcome-to-docker:latest   "/docker-entrypoint.…"   3 days ago   Exited (255) 6 minutes ago   0.0.0.0:8088->80/tcp   welcome-to-docker
            
    d. Run hello-world
       Code: docker run hello-world
       **Description:**
       This command is used to confirm that Docker can successfully run containers
       **Output:**
       Hello from Docker!
       This message shows that your installation appears to be working correctly.
       
    e. Run ubuntu container
       Code: docker run -it ubuntu bash
       **Description:**
       This command is used to run ubuntu
       i) inside container
          Code: echo hello
          **Description:**
          This command is used to print hello in the terminal
          **Output:**
          hello
          
      f. Create Flask app
         Code: echo from flask import Flask > app\app.py
               echo app = Flask(__name__) >> app\app.py
               echo @app.route("/") >> app\app.py
               echo def home(): >> app\app.py
               echo    return "Docker mission success" >> app\app.py
               echo app.run(host = "0.0.0.0", port = 5000) >> app\app.py
               type app\app.py
              **Description:**
              **Output:**
              from flask import Flask
              app = Flask(__name__)
              @app.route("/")
              def home():
                    return "Docker mission success"
              app.run(host = "0.0.0.0", port = 5000)
              
        g. create dockerfile
           Code: echo FROM python:3.12 > Dockerfile
                 echo WORKDIR  /app >> Dockerfile
                 echo COPY app/app.py  . >> Dockerfile
                 echo RUN pip install flask >> Dockerfile
                 echo CMD ["python", "app.py"] >> Dockerfile
           **Description:**
           Creates dockerfile
           
        h. build an image
           code: docker build -t myflask .
           **Description:**
           Docker build tells Docker to create an image, -t myflask names my image as myflask and . tells Docker
           to look for the Dockerfile in my current folder.
            **Output:**
            [internal] load build definition from   0.0s
             => => transferring dockerfile: 143B        0.0s
             => [internal] load metadata for docker.io  1.7s
             => [auth] library/python:pull token for r  0.0s
             => [internal] load .dockerignore           0.0s
             => => transferring context: 2B             0.0s
             => [1/4] FROM docker.io/library/python:3.  7.9s
             => => resolve docker.io/library/python:3.  0.0s
             => => sha256:32314f4c8cf88755 250B / 250B  0.5s
             => => sha256:45d437fd4e 25.72MB / 25.72MB  6.1s
             => => sha256:50cff32ed7ce 6.09MB / 6.09MB  4.0s
             => => extracting sha256:50cff32ed7ce0b0de  0.7s
             => => extracting sha256:45d437fd4e78c768f  1.7s
             => => extracting sha256:32314f4c8cf88755b  0.0s
             => [internal] load build context           0.1s
             => => transferring context: 228B           0.1s
             => [2/4] WORKDIR /app                      0.4s
             => [3/4] COPY app/app.py  .                0.1s
             => [4/4] RUN pip install flask             7.6s
             => exporting to image                      2.7s
             => => exporting layers                     1.7s
             => => exporting manifest sha256:953b0e18b  0.0s
             => => exporting config sha256:d09c4aaa376  0.0s
             => => exporting attestation manifest sha2  0.0s
             => => exporting manifest list sha256:1d03  0.0s
             => => naming to docker.io/library/myflask  0.0s
             => => unpacking to docker.io/library/myfl  1.6s
      i. Run the container && open browser
         Code: docker run -p 5000:5000 myflask, http://localhost:5000
         **Output:**
         Docker mission success
      j. Verify that the container is running:
          Code: docker ps
          **Output:**
          CONTAINER ID   IMAGE     COMMAND     CREATED      STATUS             PORTS     NAMES
          531e1c33ad86   python    "python3"   4 days ago   Up About an hour             sad_tesla
      k. Compare attach & exec
         Code: docker attach 531e1c33ad86, docker exec -it 531e1c33ad86 bash
         Explanation: Attach - reconnects to main running process, exec - opens a new shell
      l. Test docker's volume
        i)create volume:docker volume create myvolume
          **Output:** myvolume
        ii) run volume container && exit: docker run -it -v myvolume:/data ubuntu bash,echo hello > /data/test.txt, exit
        iii) re-run container: docker run -it -v myvolume:/data ubuntu bash, cat /data/test.txt
             **Output:** hello, exit
      m. remove the container
         Code: docker rm b7613c8dc632
         **Description:** removes the container that has the container_id
      n. Check the other images that still exist
         Code: docker images
         **Description:** checks other images that haven't been deleted yet
         **Output:**
                                     
          IMAGE                   ID             DISK USAGE
          docker/welcome-to-docker:latest
                                  c4d56c24da4f       22.2MB
          hello-world:latest      452a468a4bf9       25.9kB
          myflask:latest          1d03520e359e       1.62GB
          python:latest           ffebef43892d       1.63GB

Troubleshooting example:
1. Flask app not staying active: check if the container within the Flask desktop application is active
2. Error in creating a dockerfile: check the spellings of commands in the command prompt(especially the 'COPY app/app.py' command)
         
        
         
                        
                        
