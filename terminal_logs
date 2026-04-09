    Terminal :    
    1. Check current location 
    (base) hkim9771852@c4r10s1  ~ % pwd  
    /Users/hkim9771852
    

    2. List all files and directories
    (base)hkim9771852@c4r10s1  ~ %   % ls -a
    .			.ssh			Library
    ..			.vscode			Movies
    .CFUserTextEncoding	.zsh_sessions		Music
    
    
    3. Create folder
    (base) hkim9771852@c4r10s1  ~ % mkdir first_dir
    (base) hkim9771852@c4r10s1  ~ % ls
    Library		Music		Pictures	first_dir

    4. Move into a directory
    (base) hkim9771852@c4r10s1  ~ % cd first_dir
    (base) hkim9771852@c4r10s1 first_dir % pwd (print working directory)
    /Users/hkim9771852/first_dir

    5. Copy folder
     hkim9771852@c4r10s1 first_dir % mkdir first_subdir
    hkim9771852@c4r10s1 first_dir % cp -r first_subdir first_subdir_copy
    Note: cp -r - copy all subfolders and files inside the current working directory
    (base) hkim9771852@c4r10s1 first_dir % ls 
        first_subdir             first_subdir_copy

    6. Change the name of the folder
    (base) hkim9771852@c4r10s1 first_dir % ls 
        first_subdir             first_subdir_copy                   
    (base) hkim9771852@c4r10s1 first_dir % mv first_subdir_copy first_subdir_revised
    Note: mv - changes the name of the folder
    (base) hkim9771852@c4r10s1 first_dir % ls
    first_subdir       first_subdir_revised
    

    7. Create file and move file into another directory
    
    hkim9771852@c4r10s1 first_dir % touch first.txt
    hkim9771852@c4r10s1 first_dir % ls
    first.txt		first_subdir		first_subdir_revised
    hkim9771852@c4r10s1 first_dir % mv first.txt first_subdir
    hkim9771852@c4r10s1 first_dir % ls
    first_subdir		first_subdir_revised
    

    8. Delete folder or file
    hkim9771852@c4r10s1 first_dir % cd first_subdir
    hkim9771852@c4r10s1 first_subdir % ls
    first.txt
    hkim9771852@c4r10s1 first_subdir % rm first.txt
    hkim9771852@c4r10s1 first_subdir % cd ..
    Note: cd .. moves you into the parent directory
    hkim9771852@c4r10s1 first_dir % rmdir first_subdir 
    Note: rmdir = remove directory
    hkim9771852@c4r10s1 first_dir % ls
    first_subdir_revised

    9. Create and view the contents in the file
    hkim9771852@c4r10s1 first_dir % touch hello2.txt
    hkim9771852@c4r10s1 first_dir % vim hello2.txt
    Note: vim command opens a file in a text editor. After opening the file, 
    make sure to do the following: 1. press i(insert mode) 2. type text 3. press ESC 4. Type wq(write & quit)
    hkim9771852@c4r10s1 first_dir % cat hello2.txt
    Note: cat command lets you to view the file
    "Hello World!"
