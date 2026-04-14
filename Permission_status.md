1. Check permission status
   a) Checking permission status of each directory
```bash
   hkim9771852@c4r10s1 ~ % ls -l
   Output:
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Desktop
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Documents
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Downloads
    drwx------@ 78 hkim9771852  hkim9771852  2496 Apr  9 16:24 Library
    drwx------   3 hkim9771852  hkim9771852    96 Apr  9 16:05 Movies
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Music
    drwx------   5 hkim9771852  hkim9771852   180 Apr  9 16:07 OrbStack
    drwx------+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Pictures
    drwxr-xr-x+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Public
    drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  9 18:22 first_dir
    b) Creating a new directory && new text file
    hkim9771852@c4r10s1 ~ % mkdir second_dir
    c) Checking permission status of each directory(again...)
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Desktop
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Documents
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Downloads
    drwx------@ 78 hkim9771852  hkim9771852  2496 Apr  9 16:24 Library
    drwx------   3 hkim9771852  hkim9771852    96 Apr  9 16:05 Movies
    drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Music
    drwx------   5 hkim9771852  hkim9771852   180 Apr  9 16:07 OrbStack
    drwx------+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Pictures
    drwxr-xr-x+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Public
    drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  9 18:22 first_dir
    drwxr-xr-x   2 hkim9771852  hkim9771852    64 Apr  9 19:56 second_dir
    -rw-r--r--   1 hkim9771852  hkim9771852     0 Apr  9 20:00 second.txt
```
3. Change permission status
   a) Change permission status of text file
   ```bash
      hkim9771852@c4r10s1 ~ % chmod 755 second.txt
   ```
   b) Change permission status of a directory
   ```bash
      hkim9771852@c4r10s1 ~ % chmod 777 second_dir
   ```
   c) Check the updated status of each directory(and file)
   ```bash
      drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Desktop
      drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Documents
      drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Downloads
      drwx------@ 78 hkim9771852  hkim9771852  2496 Apr  9 16:24 Library
      drwx------   3 hkim9771852  hkim9771852    96 Apr  9 16:05 Movies
      drwx------+  3 hkim9771852  hkim9771852    96 Apr  9 16:05 Music
      drwx------   5 hkim9771852  hkim9771852   180 Apr  9 16:07 OrbStack
      drwx------+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Pictures
      drwxr-xr-x+  4 hkim9771852  hkim9771852   128 Apr  9 16:05 Public
      drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  9 18:22 first_dir
      -rwxr-xr-x   1 hkim9771852  hkim9771852     0 Apr  9 20:00 second.txt
      drwxrwxrwx   2 hkim9771852  hkim9771852    64 Apr  9 19:56 second_dir
   ```
      Note: notice that the code for permission status(second.txt) changed
            from -rw-r--r--  to -rwxr-xr-x and that for second_dir changed
            from drwxr-xr-x to drwxrwxrwx
            
      

    
